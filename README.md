# HOLUX GR245+ TOOLS

这是一个给 HOLUX GR245+ 老用户提供的工具。我作为使用者之一，深受原厂 HOLUX ezTour for Logger 软件因为 GOOGLE MAP 在中国大陆不支持打开后，需要卡顿一分钟才能进入界面把轨迹导出的痛苦。
并且，也因为地图问题，原厂软件内已无法再查看轨迹。所以现在我都是用它把轨迹导出.GPX格式后，在OMAP中显示。OMAP在中国大陆还是很好用的。

所以这个小工具就做了最基本的事情，当然开发期间为了研究一些MTK3318指令，也做了一些附加扩展。

## 它目前可以做到如下功能：
- **导出 .BIN**：可以把 HOLUX GR245+ logger 的数据导出为 .BIN 格式，可以导出 GR245+ 完整的 4MB 大小，也可以根据实际轨迹存贮情况导出有效的大小；
- **导出 .GPX 轨迹**：可以把 .BIN 格式 中的轨迹转成 .GPX 格式；
- **.ITM导出 .GPX 轨迹**：.可以把 HOLUX ezTour for Logger 的 .ITM 工程文件中的 轨迹转成 .GPX，支持 整个目录及子目录下所有.ITM的转换，转换后的.GPX 就放在原 .ITM 目录下，后缀名不一样，文件同名；
- **命令行输入**：支持自己在命令行输入MTK3318 的一些指令，不需要输入$，不需要输入CHECKSUM，以方便试验指令结果

## 不足之处：
- GPS 由于存在漂移，需要在应用层 调用一些平滑算法去平滑路径，这需更专业与深入的知识，我目前对此兴趣不大，所以没有完成，所有导出.GPX中的LOGPOINT都是原始的值；
- 其它一些细微的地方，其实还有蛮多功能我曾经有想过加入的，比如显示设备信息，轨迹直接在GOOGLE MAP 或 BAIDU MAP 等上面在线显示，但他们都不是我的第一需求，而导出为 .GPX 才是我最本质的需求，即然现在我已完成，所以就不再浪费时间

## 软件运行依赖条件：
- Windows 10 64bit
- .NET FRAMEWORK 4.7.2 Runtime

也感谢您的使用与意见。
感谢 gpsbabel, bt747, mtkbabel, 4RIVER 关于 MTK GPS设备 的开发参考。

[https://www.gpsbabel.org/](https://www.gpsbabel.org/)

[https://www.bt747.org/](https://www.bt747.org/)

[https://4river.a.la9.jp/gps/index.htm](https://4river.a.la9.jp/gps/index.htm)

[https://sourceforge.net/projects/mtkbabel/](https://sourceforge.net/projects/mtkbabel/)


=============

A Little Tool for HOLUX GR245+ Users
This is a small utility I made for fellow HOLUX GR245+ users.

## Why I made this:
Honestly, I was really struggling with the official HOLUX ezTour for Logger software. Since Google Maps stopped working properly in China mainland, the software would lag for a whole minute every time I opened it just to export a track. Plus, I couldn't even view my tracks inside the app anymore because of the map issues.
Now, I just export everything to .GPX and view it in OMAP, which still works great here.
So, I built this tool to do the basics. I also added a few extra features while I was experimenting with MTK3318 commands.

## What it can do:
- **Export Data**: It can dump data from your HOLUX GR245+ into a .BIN file. You can grab the full 4MB or just the part with actual data.
- **Convert .BIN to .GPX**: Turns those .BIN files into .GPX tracks.
- **Convert .ITM**: It can also convert tracks from the official software's .ITM project files into .GPX. It even works on whole folders (and subfolders) at once. It saves the new GPX files right next to the original ITM files.
- **Command Line**: You can type in MTK3318 commands directly. No need to worry about typing the $ or calculating the CHECKSUM—it handles that for you so you can just test commands easily.

## A couple of limitations:
- **Raw Data Only**: GPS signals naturally drift. Fixing this usually requires some complex smoothing algorithms, but I didn't feel like diving that deep into the math right now. So, the points in the exported .GPX files are raw values (unsmoothed).
- **Basic Features Only**: I thought about adding other stuff like showing device info or displaying tracks on Google/Baidu Maps online, but exporting to .GPX was my main goal. Since that works now, I didn't want to waste time on features I don't really need.

## System Requirements：
- Windows 10 64bit
- .NET Framework 4.7.2 Runtime

Thanks for checking this out, and let me know what you think.
I'd like to thank gpsbabel, bt747, mtkbabel, and 4RIVER for serving as valuable references for MTK GPS device development.

[https://www.gpsbabel.org/](https://www.gpsbabel.org/)

[https://www.bt747.org/](https://www.bt747.org/)

[https://4river.a.la9.jp/gps/index.htm](https://4river.a.la9.jp/gps/index.htm)

[https://sourceforge.net/projects/mtkbabel/](https://sourceforge.net/projects/mtkbabel/)
