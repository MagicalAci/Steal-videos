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
`````
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
        `````
       
    更改
   >range(2,3):
   为需要的级数，如其就是2级
   >urls.append('https://www.bilibili.com/video/BV1Ts411J7Zi?p='+str(i))
    更换网址
    *其中p=多少是B站上的多少级，不填可以批量下载*
    '
    
