**记录开卡七彩虹512G SSD(主控SM2258XT)过程**<br>

本人在使用淘汰的SSD接硬盘盒当作移动硬盘，不知为什么SSD写保护了，不能删除内容，不能新建内容，这两个操作正常，但只要重新插拔，就会复原。无法格式化，删除所有分区后自动生成“分区(0)”。<br>

**DiskGenius格式化时的错误提示：**<br>
写扇区错误！ 磁盘: HD2:UNITEK(477GB) 起始于 1000214527 扇区 共 1 个扇区。 (Err:5 拒绝访问。) <br>
写扇区错误！ 磁盘: HD2:UNITEK(477GB) 起始于 4096 扇区 共 1 个扇区。 (Err:5 拒绝访问。)<br>
写扇区错误！ 磁盘: HD2:UNITEK(477GB) 起始于 6295564 扇区 共 2 个扇区。 (Err:5 拒绝访问。)<br>
写扇区错误！ 磁盘: HD2:UNITEK(477GB) 起始于 4120 扇区 共 128 个扇区。 (Err:5 拒绝访问。)<br>

固态硬盘要是坏了，在保质期里的可以返厂维修，如果过保了，我们还是有办法自己修复的，方法就是下载量产工具，用量产工具来开卡。<br>
首先要准备一个SATA-USB转接硬盘盒（我使用的ASM235CM）。<br>

手中这块是七彩虹的SL500固态硬盘，主控是SM2258XT，闪存丝印是H25QFT8B3A8R，ID是AD,5E,28,22,10,90（Hynix HY3DV4制程）。<br>
**关于如何找到自己的硬盘的参数**<br>
先使用硬盘进入工厂模式，拆开SSD，使用镊子短接两个ROM孔，短接的过程中插上电，就可以进入工厂模式。<br>
此时任何一个开卡工具就可以搜索到硬盘，大小为1024M。<br>

<img width="494" height="436" alt="image" src="https://github.com/user-attachments/assets/8ebd8b35-1bd3-4f98-962c-c626e3006dfb" /><br>

点击图标，打开参数信息，CH就是闪存的ID<br>
进入网址https://flashinfo.top/<br>
通过id搜索出闪存的型号和制程<br>

<img width="712" height="1141" alt="image" src="https://github.com/user-attachments/assets/d5c05ff0-2dfa-4b82-891e-20a3096da46a" /><br>

再从同网站搜索到主控SM2258XT，制程为3DV4的开卡工具<br>

短接进入开卡工具，打开设定(选择栏第二个)<br>

<img width="1516" height="1152" alt="image" src="https://github.com/user-attachments/assets/4695b40d-cf20-48d2-a7b9-bb83670c5e30" /><br>

首先Flash要选对，推荐直接Auto，Flash频率改为100MHz，勾选忽略Tran ADJ，Pretest选择0，磁盘容量改为默认/自己填，勾选QC程序，最后点击保存配置。<br>
返回第一页点击开卡，等待结束，完成后发现有坏块，我怀疑这是硬盘不能用的罪魁祸首。<br>

<img width="1516" height="1152" alt="image" src="https://github.com/user-attachments/assets/757ff08d-5974-43bf-ac13-2e7e21a554a8" /><br>

最后使用分区工具<br>

<img width="1828" height="651" alt="image" src="https://github.com/user-attachments/assets/97d781c7-e659-4626-8812-b076e5ea2b8f" /><br>

成功修复SSD。<br>
