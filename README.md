# Python Package: YouTuber
Contains several useful features that can be used for youtube related projects.
This package is intended to provide useful features for video editing, including crawling through the YouTube Data API v3 and Selenium.



# Installation
```
pip install youtuber
```

# Quick Start
## 1. Get youtube search result
```python
from youtuber import YoutubeAPI

DEVELOPER_KEY = "enter_your_api_key"
youtuber_v3 = YoutubeAPI(DEVELOPER_KEY)
links = youtuber_v3.get_links('chatGPT', 3) # if you enter 3, you can get 3 video links.
links
['https://www.youtube.com/watch?v=mpnh1YTT66w',
 'https://www.youtube.com/watch?v=ykuDB3xpTTo',
 'https://www.youtube.com/watch?v=GXm7WRtRbhA']
```

## 2. Get comment data
```python
from youtuber import YoutubeCrawler

chrome_driver = r'C:\Program Files\chromedriver.exe'
youtuber_crawl = YoutubeCrawler(chrome_driver)
df = youtuber_crawl.get_comment_df(links, 1) # if you enter 1, only 1 page of comments will be searched.
df
```

# All legal responsibilities associated with the use of the package lie with the user.
The Python package "youtuber" provides code for Python users to easily access data through the YouTube Data API v3 and Selenium. All licenses follow those of the API and dependent packages, and all responsibility for handling data and using the package lies with the user. There is no monetary compensation received for the use of this code, and it should be noted that there is no liability for the use of the code.


<br>

[`YouTube Data API v3`](https://developers.google.com/youtube/v3/getting-started?hl=ko)
is an API that provides access to YouTube data, such as videos, playlists, and channels.