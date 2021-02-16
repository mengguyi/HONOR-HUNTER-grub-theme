HONOR HUNTER笔记本电脑grub主题
=
安装教程：<br>
-
首先将仓库克隆下来<br>
<code>git clone https://github.com/mgy-qyqf/HONOR-HUNTER-grub-theme.git</code>

将“HONOR”文件夹复制到<code>/boot/grub2/themes</code> 或 <code>/boot/grub/themes</code> 下<br>

对于UEFI的电脑：<br>
-
复制<code>zh_CN.mo</code>到<code>/boot/efi/EFI/"你操作系统的名字"/locale</code> 下<br>
修改<code>/etc/grub</code><br>
将<code>GRUB_TERMINAL_OUTPUT="console"</code>注释掉（在前面添加<code>#</code>修改为：<code>#GRUB_TERMINAL_OUTPUT="console"</code>）<br>
添加<code>GRUB_THEME="/boot/grub2/themes/HONOR/theme.txt"</code> 或<br>
<code>GRUB_THEME="/boot/grub/themes/HONOR/theme.txt"</code>（与你放置HONOR文件夹的位置有关）<br>
修改<code>GRUB_TIMEOUT=0</code>为<code>GRUB_TIMEOUT=5</code>或任何大于等于0的数<br>
执行<br>
<code>sudo grub2-mkconfig -o /boot/efi/EFI/"你操作系统的名字，与上面一致"/grub.cfg</code><br>

对于BIOS的电脑：<br>
-
复制<code>zh_CN.mo</code>到<code>/boot/grub/locale</code> 或<code>/boot/grub2/locale</code> 下<br>
修改<code>/etc/grub</code><br>
将<code>GRUB_TERMINAL_OUTPUT="console"</code>注释掉（在前面添加<code>#</code>修改为：<code>#GRUB_TERMINAL_OUTPUT="console"</code>）<br>
添加<code>GRUB_THEME="/boot/grub2/themes/HONOR/theme.txt"</code> 或<br>
<code>GRUB_THEME="/boot/grub/themes/HONOR/theme.txt"</code>（与你放置HONOR文件夹的位置有关）<br>
修改<code>GRUB_TIMEOUT=0</code>为<code>GRUB_TIMEOUT=5</code>或任何大于等于0的数<br>
执行<br>
<code>sudo grub2-mkconfig -o /boot/grub2/grub.cfg</code><br>
或
<code>sudo grub2-mkconfig -o /boot/grub/grub.cfg</code>（与你上面放置HONOR文件夹的位置有关）<br>
