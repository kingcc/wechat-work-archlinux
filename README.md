
Archlinux下企业微信包
===================

## Usage

**1、克隆一下仓库到本地，选择`pkg`下合适的安装包安装（使用`uname -m`检查一下你的cpu架构）**

**2、非Gnome用户？**

  如果你遇到这个情况：

  ```
  X Error of failed request: BadWindow (invalid Window parameter)
  Major opcode of failed request: 20 (X_GetProperty)
  Resource id in failed request: 0x0
  Serial number of failed request: 10
  Current serial number in output stream: 10
  ```

  安装gnome-settings-daemon，然后运行/usr/lib/gsd-xsettings：

  ```sh
  # pacman -S gnome-settings-daemon
  # /usr/lib/gsd-xsettings
  ```


**3、系统语言非中文时，中文全显示成方块**

  需要在

  ```sh
  /opt/deepinwine/tools/run.sh
  /opt/deepinwine/tools/run_v2.sh
  ```

  中将 `WINE_CMD` 那一行修改为

  ```sh
  WINE_CMD="LC_ALL=zh_CN.UTF-8 deepin-wine"
  ```