# Python_pydub
 Python_pydub program
# 长音频文件的分割与转码处理
## 导入pydub库
from pydub import AudioSegment
## 导入语音文件
song = AudioSegment.from_file("example.wav",format = "wav")
## 导出语音文件
通过export()函数输出文件的句柄。
file_handle = song.export(filepath,audio_type)
## 使用pydub库实现音频切片
切割单位为毫秒
first_time = 3000  首部切割时间为3秒
last_time = 3000   尾部切割时间为3秒
song[:first_time]
song[-last_time:]
## 使用pydub库实现语音转码
song = AudioSegment.from_file(filepath,input_type)
song.export(f"{filename}.{output_type}", format=f"{output_type}")
