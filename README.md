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
    
# 特殊说明
此项目爬取的是音频+视频+音频和视频，届时按照需要删除或使用
    
# 需要配置的工具环境
链接：https://pan.baidu.com/s/1C2_Ncy87gS_Ao8-xA5jnTg 
提取码：eb9c 

在我的电脑里配置环境
并更改代码中的目录
`    command = f'D:\\RA_file\\py\\ffmpeg\\ffmpeg-4.3.1-win64-static\\bin\\ffmpeg -i "%s_video.mp4" -i "%s_audio.mp4" -acodec copy -vcodec copy "%s.mp4"' % (
`
其中
>D:\\RA_file\\py\\ffmpeg\\ffmpeg-4.3.1-win64-static\\bin\
需要更改的此时的根目录
