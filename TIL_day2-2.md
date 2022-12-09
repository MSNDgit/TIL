# Subject 과제 - Melon 인기 장르 파악

url = "https://www.melon.com/genre/song_list.htm?gnrCode=GN0100"
header = {'User-Agent': 'Mozilla/5.0 (Windows NT 6.3; Trident/7.0; rv:11.0) like Gecko'}
melon_url = https://www.melon.com/genre/song_list.htm?gnrCode=GN0100
raw = requests.get(melon_url, headers = header)
melon_raw = requests.get(url)

melon_bs = BeautifulSoup(melon_raw.text, "html.parser")

# 멜론의 경우 외부유입을 막아놨기 때문에 위에 header 설정을 잘 해야한다.
# 하지 않을경우 다른경로 유입으로 파악이 불가능하니 검색 전 설정을 잘 해야한다.