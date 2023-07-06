﻿1 代码功能
=
项目中包括 beijing_bus.py 和 xianming.py 两个程序。
xianming.py 实现从**8684**网站上获取北京公交线名。
beijing_bus.py 根据 xianming.py获取的北京公交线名，从*高德地图*网站获取各公交线路运行轨迹经纬度及沿线站名。 

2 运行输入及输出
=
2.1 xianming.py
-
输入：
**all_url**参数为访问的网站，以北京为例，访问网址为'https://beijing.8684.cn/'，其中城市名可更改来获取不同城市的公交线路名，例如：'https://chongqing.8684.cn/'。
输出：
程序运行结束会生成**Network_bus.txt**文本文件，文件中记录了城市包含的公交线路名。

2.2 beijing_bus.py
-
输入：
**path**参数为待读取的公交线名文本文件，由 xianming.py 生成。
**cityname**参数为待访问的城市名（需要用中文书写）。
**fangxiang**参数决定了待获取公交线路的运行方向，0为正向，1为方向，当某公交线路为环线是，方向只有正向。  程序默认方向为正向，当更改方向时，需要更改113行代码中保存文件的文件夹名字（注意，这个文件夹需要在程序运行前建好）。
输出：
程序运行中，由于8684网址上部分线名在高德地图上查询不到数据，故会将查询不到的线名输出。
查询到的数据会输出到**对应线名的csv文件中**，参考代码113行。
未查询到的公交线名会记录到**nodata.txt**文本文件中。

3 程序运行
=
我提供了一份包含北京公交线名的文件：**Network_bus.txt**，可以直接运行beijing_bus.py程序，获得各线路的途径站及经纬度坐标。
xianming.py程序可以直接运行获得指定城市的公交线名。






> Written with [StackEdit](https://stackedit.io/).
