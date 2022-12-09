requests 함수

import requests
from bs4 import BeautifulSoup
# BeautifulSoup 함수로 인터넷 리스트 정리


lotto_url = "https://dhlottery.co.kr/gameResult.do?method=byWin"
lotto_raw = requests.get(lotto_url)

lotto_bs = BeautifulSoup(lotto_raw.text, "html.parser")

result = lotto_bs.find("div", {"class":"nums"})
# print(result)

result_win = result.find("div", {"class":"num win"})
print("<로또 당첨번호>")
for i in result_win.find_all("span"):
    print(i.text)

print("<보너스번호>")
result_bonus = result.find("div", {"class":"num bonus"})
result_bonus_num = result_bonus.find_all("span")[0].text
print(result_bonus_num)
# 파이썬 로또번호 출력




# 주식 인기순위
url = "https://finance.naver.com/sise/"
naver_raw = requests.get(url)

naver_bs = BeautifulSoup(naver_raw.text, "html.parser")

# 구글 F12로 위치 파악 후 자료 검색
result = naver_bs.find("div", {"class":"rgt"})

result_popular = result.find("ul", {"id":"popularItemList"})
print("<인기 검색 종목>")
for i in result_popular.find_all("a"):
    print(i.text)
