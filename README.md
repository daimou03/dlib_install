# dlib_install
安装dlib，进行人脸68关键点检测识别

# 安装教程
博客：https://blog.csdn.net/weixin_58403869/article/details/147673670?spm=1001.2014.3001.5501

微信公众号：https://mp.weixin.qq.com/s/r-NM7R4txNl8NDQlAM4sbw

github 直接在dlib_whl_files文件夹下进行，根据对应python下载对应的dlib库的whl文件

引言
本地设备（win10，amd64位）
在学习计算机视觉，需要安装dlib第三方库，来进行人脸68关键点检测
如图（图片来源百度）
dlib库检测人脸使用方法与简单的疲劳检测应用-CSDN博客

81个人脸关键点检测_81个人脸关键点下载-CSDN博客

先简单了解下Dlib和人脸68关键点
    Dlib 是一个现代的C++工具包，广泛应用于机器学习、图像处理、计算机视觉等领域。它由Davis King开发并维护，旨在简化复杂算法的实现过程，使得开发者能够快速构建高效的应用程序。Dlib不仅提供了丰富的机器学习算法库，还包含了大量用于图像处理的功能。

    Dlib 提取人脸特征点是用 68 个点包围每个部位，如上图，例如第 37 个点到第 42 个点就代表右眼，在图片上这几个点若显示出来就是把右眼那块区域包围着，可以通过这些点之间距离的变化来判断人脸的变化，比如是否眨眼等操作，imutils 通过 OrderedDict 把这些点的索引与其表示的区域直接通过字典形式联系起来，之后再提取某个部位的点时，就不用去查点的索引分布了，例如想提取嘴部特征点，其索引可以通过:

(mStart,mEnd) = face_utils.FACIAL_LANDMARKS_68_IDXS[“mouth”]




Dlib安装

方法一：直接pip安装

pip install dlib


进行安装dlib，会提示报错

  ERROR:CMake must be installed to build dlib
----------------------------------------
  ERROR:Failed building wheel for dlib


原因是：这是因为系统中缺少 cmake 编译工具，我们来到 cmake 的官方下载地址 https://cmake.org/download/，傻瓜式安装后即可，当然 Visual Studio 中的 C++ 组件也是需要安装的

在命令行需要提前安装

pip install cmake
在进行pip安装dlib
pip install dlib

方法2 ：通过安装whl文件来安装dlib
先讲述步骤
#首先安装cmake
pip install cmake
# 在命令行查看python版本
python -V
再根据当前环境进行安装whl文件
#在终端cmd使用cd进入whl文件存放位置
如果是python的版本是3.9，就使用下面命令进行安装
pip install dlib-19.23.0-cp39-cp39-win_amd64.whl
如果是python的版本是3.8，就使用下面命令进行安装
pip install dlib-19.19.0-cp38-cp38-win_amd64.whl.whl
如果是python的版本是3.7，就使用下面命令进行安装
pip install dlib-19.17.99-cp37-cp37m-win_amd64.whl
如果是python的版本是3.6，就使用下面命令进行安装
pip install dlib-19.8.1-cp36-cp36m-win_amd64.whl
打开pycharm 创建py文件，导入dlib
图片
不报错，就是成功了

whl文件获取：
whl文件获取放在下面
关注公众号，回复“dlib安装”，在回复的百度云链接中进行下载


图片

欢迎关注下期，分享如何使用dlib结合计算机视觉opencv实现人脸68关键点识别！！
程序效果图片（原图片来自百度）
图片

谢谢大家！！！这里是daimou03，觉得这篇文章对您有帮助，还请关注，点赞加转发，我们下期再见。
