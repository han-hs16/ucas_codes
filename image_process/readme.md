# 数字图像处理附加作业
韩虎生 202018013229038 计703


- 实现功能
    - 空域常见操作：包括gamma校正、亮度反转、直方图均衡化、拉普拉斯提取高频信息、基于拉普拉斯的高频增强、水平和垂直方向梯度提取、高斯模糊、中值滤波等

    - 频域常见操作：包括快速傅里叶变换、快速傅里叶反变换、理想低/高通滤波、巴斯沃特低/高通滤波、高斯低/高通滤波等

    - 图像恢复常见操作：增加各种噪声、均值滤波、逆谐波滤波、中点滤波、自适应中值滤波(非常慢，运行时请注意)、 带阻滤波器(理想、高斯、巴斯沃特)、陷波滤波器(理想、高斯、巴斯沃特)

    - 小波变换：高斯及拉普拉斯金字塔构建、快速哈尔小波变换及其反变换


- 运行环境
    - 使用Python3.7+PyQt5实现界面以及相应功能
    - 详细环境配置可看packages.txt

- 代码结构
```
    - main.py                       运行入口文件
    - UI文件                        使用PyQt designer实现的界面配置文件
        - entryWindow.ui
        - Ui_frequency.ui
        - Ui_spatial.ui
        - Ui_restoration.ui
        - Ui_wavelets.ui
    - 功能文件
        - ui_entry.py               主界面
        - ui_spatial.py             空域界面文件
        - ui_frequency.py           频域界面文件
        - ui_restoration.py         图像恢复界面文件
        - ui_wavelets.py            小波变换界面文件

        - spatial_method.py         空域功能代码
        - frequency_method.py       频域功能代码
        - restoration_method.py     图像恢复功能代码
        - wavelets_method.py        小波变换功能代码

    - src                           包含测试图片
        
    - packages.txt                  pip导出的环境配置
    - demo_result                   包含程序运行截图，其中带阻、陷波滤波器请参看图片
```


- 注意：
    - 时间关系，没有写的太多输入正则，所以请尽量按正常的输入运行程序，主要包括
    - 做相应操作前，先载入图片
    - 输入的kernel或窗口大小等请按奇数输入
    - 陷波滤波器的输入u0和v0，支持单数值输入，也支持区间输入,以'-'隔开, 比如"20-80"， "20-", 区间后一个不填写表明一直陷波到图像边界
    - 部分按钮有提示文字，鼠标长时间停留即可看到
