### 重装系统

案例：64位win10、联想

1. 准备大于8G的U盘，制作系统启动盘，放置镜像

2. 备份C盘文件

3. 进BIOS关闭安全启动（Security->Secure Boot），切换成UEFI方式

4. 把启动盘插进去调整启动方式在最前面

5. 进入pe，打开diskGenus，把C盘删除分区（硬盘->删除所有分区）或者格式化，注意保存操作

![img](file:///E:\QQ\QQfile\1157932484\Image\C2C\862CE37F1F28230BDE1661B98AB231DB.jpg)

6. 点击win10镜像，按setup.exe，然后一直下一步

7. 选择没有产品密钥安装，随便选一个版本安装，最好是出厂版本，一般是家庭版或家庭中文版，联网就能自动激活

8. 选择自定义

![img](file:///E:\QQ\QQfile\1157932484\Image\C2C\233F3EFC5C5EFCDFF2261199566D127B.jpg)

9. 选择要装的盘，点击下一步

![img](file:///E:\QQ\QQfile\1157932484\Image\C2C\811702FE4981BB7D1F1F0371E0B8A873.jpg)

10. 等待。。。

11. 选择不联网

12. 进入桌面后联网检查更新

13. 激活win系统，点击激活的脚本，选1

![img](file:///E:\QQ\QQfile\1157932484\Image\C2C\A1DD51DA193EEB7CA356C051D6E18F75.jpg)

14. 成功的界面

![img](file:///E:\QQ\QQfile\1157932484\Image\C2C\D6C57DA5C4740784D15FF504AE4D2D0A.jpg)



### 误删引导项解决办法

出现问题：BIOS中EFI下没有引导项

注意：有时候引导自己坏了，EFI文件夹下并不为空（进pe看看有无EFI文件夹），这时可直接修复引导，忽略建立EFI分区过程，跳到步骤3

1. 进pe，打开diskGenus，系统盘新建分区100M，选择调整分区大小

![img](file:///E:\QQ\QQfile\1157932484\Image\C2C\6913E224F0EB080E445F1FD5A7291476.jpg)

![img](file:///E:\QQ\QQfile\1157932484\Image\C2C\C568396DE493D77F8F0F74FE0E9F4EAB.jpg)

![img](file:///E:\QQ\QQfile\1157932484\Image\C2C\5E5E0DEBF34C6DC01030C934CE4D7983.jpg)

2. 删除100M的新分区，使其变成闲置状态，右键100M的柱子，建立新分区

![img](file:///E:\QQ\QQfile\1157932484\Image\C2C\356ADE28E0FDA6B17E0E8FFB98177AA8.jpg)

![img](file:///E:\QQ\QQfile\1157932484\Image\C2C\98F427CD544F154FA4E888948FA2218D.jpg)

3. 打开桌面上的dism++软件，确定

![1570443483416](C:\Users\wangchen\AppData\Roaming\Typora\typora-user-images\1570443483416.png)

4. 选择要修复的系统

![1570443509965](C:\Users\wangchen\AppData\Roaming\Typora\typora-user-images\1570443509965.png)

5. 选择 恢复功能->引导修复

![1570443558740](C:\Users\wangchen\AppData\Roaming\Typora\typora-user-images\1570443558740.png)

6. 成功后如果在diskGenus中看到有EFI分区就完成修复