# 用jTessBoxEditor训练tesseract-ocr字库
## tesseract-ocr的字库训练，用到的软件是jTessBoxEditor，该软件基于JAVA运行，所以你的机器上必须有JAVA运行环境

1. 准备JAVA运行环境，这个应该基本都知道怎么搞， 没有的去官网下载安装即可。[JAVA运行时下载](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html)

2. 下载训练工具jTessBoxEditor，FX的版本可以训练汉字，官网下载地址：[jTessBoxEditor下载](https://sourceforge.net/projects/vietocr/files/jTessBoxEditor/)

3. 先准备好包含文字的图片，如: eng.abc.exp0.png 

4. 将图片转换成TIF文件
    打开一个cmd，cd 到 jTessBoxEditorFX\tesseract-ocr目录，输入
    tesseract   eng.abc.exp0.png   eng.abc..exp0 -l eng batch.nochop makebox
    
5. 打开jTessBoxEditorFX，选中“Box Editor”,进行BOX的调整，调整完成点击“SAVE”

6.  选中“Trainer”,选择“Train with Existing Box”, 点击“Run” 即可生成训练文件
