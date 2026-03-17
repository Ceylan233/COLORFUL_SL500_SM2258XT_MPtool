<font size="5">大一点的字</font>
**记录开卡七彩虹512G SSD(主控SM2258XT)过程**


固态硬盘要是坏了，在保质期里的可以返厂维修，如果过保了，我们还是有办法自己修复的，方法就是下载量产工具，用量产工具来开卡。
首先要准备一个SATA-USB转接硬盘盒（我使用的ASM235CM）。

手中这块是七彩虹的SL500固态硬盘，主控是SM2258XT，闪存丝印是H25QFT8B3A8R，ID是AD,5E,28,22,10,90（Hynix HY3DV4制程）。
关于如何找到自己的硬盘的参数，先使用硬盘进入工厂模式，拆开SSD，使用镊子短接两个ROM孔，短接的过程中插上电，就可以进入工厂模式。
此时开卡工具就可以搜索到硬盘，大小为1024M。

<img width="494" height="436" alt="image" src="https://github.com/user-attachments/assets/8ebd8b35-1bd3-4f98-962c-c626e3006dfb" />

点击图标，打开参数信息，CH就是闪存的ID
进入网址https://flashinfo.top/
通过id搜索出闪存的型号和制程
<img width="712" height="1141" alt="image" src="https://github.com/user-attachments/assets/d5c05ff0-2dfa-4b82-891e-20a3096da46a" />
