HONOR HUNTER笔记本电脑grub主题
=
安装教程：<br>
-
首先将仓库克隆下来<br>
<code>$ git clone https://github.com/mgy-qyqf/HONOR-HUNTER-grub-theme.git
将“HONOR”文件夹复制到/boot/grub2/themes 或 /boot/grub/themes 下<br>

对于UEFI的电脑：<br>
-
复制zh_CN.mo到/boot/efi/EFI/"你操作系统的名字"/locale 下<br>
修改/etc/grub<br>
将GRUB_TERMINAL_OUTPUT="console"注释掉（在前面添加"#"修改为：#GRUB_TERMINAL_OUTPUT="console"）<br>
添加GRUB_THEME="/boot/grub2/themes/HONOR/theme.txt" 或<br>
GRUB_THEME="/boot/grub/themes/HONOR/theme.txt"（与你放置HONOR文件夹的位置有关）<br>
修改GRUB_TIMEOUT=0为GRUB_TIMEOUT=5或任何大于等于0的数<br>
执行<br>
sudo grub2-mkconfig -o /boot/efi/EFI/"你操作系统的名字，与上面一致"/grub.cfg<br>

对于BIOS的电脑：<br>
-
复制zh_CN.mo到/boot/grub/locale 或/boot/grub2/locale 下<br>
修改/etc/grub<br>
将GRUB_TERMINAL_OUTPUT="console"注释掉（在前面添加"#"修改为：#GRUB_TERMINAL_OUTPUT="console"）<br>
添加GRUB_THEME="/boot/grub2/themes/HONOR/theme.txt" 或<br>
GRUB_THEME="/boot/grub/themes/HONOR/theme.txt"（与你放置HONOR文件夹的位置有关）<br>
修改GRUB_TIMEOUT=0为GRUB_TIMEOUT=5或任何大于等于0的数<br>
执行<br>
sudo grub2-mkconfig -o /boot/grub2/grub.cfg<br>
或
sudo grub2-mkconfig -o /boot/grub/grub.cfg（与你上面放置HONOR文件夹的位置有关）<br>
