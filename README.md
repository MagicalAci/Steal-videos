# Steal-videos
Climb the website video with Python

# 需要的库
-requests
-threading
-re
-json
-os
-time
-from lxml import etree
-from queue import Queue

# 使用方法
```
  def main():
   urls = []
    for i in range(2,3):
        urls.append('https://www.bilibili.com/video/BV1Ts411J7Zi?p='+str(i)) 
    for i in range(len(urls)):
        single_data(urls[i],i+2)				   
         time.sleep(2)  
     for x in range(3):
         th = threading.Thread(target=download)		
         th.start() 
  ```
       
      
## 需要更改

   >`range(2,3):`
   为需要的集数，如其就是2集
   
   >`urls.append('https://www.bilibili.com/video/BV1Ts411J7Zi?p='+str(i))`
    更换网址
    *其中p=多少是B站上的第多少集，不填可以批量下载*
    
   >`single_data(urls[i],i+2)	`
    i从0开始，这个是用来命名的，我先在下载的是第二集，所以i+2
    
**特殊说明：此项目爬取的是音频+视频+音频和视频，届时按照需要删除或使用
    
