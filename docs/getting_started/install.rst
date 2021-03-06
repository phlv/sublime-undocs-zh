============
安装
============

Sublime Text在每个平台的安装过程有些不一样。

确认阅读下官方网站的 `使用条件`_ 。Sublime Text不是免费的。

.. _使用条件: http://www.sublimetext.com/buy

32-位还是64-位?
===================

如果你运行的是64-位系统选择64-位版本的，如果是32-位系统选择32-位版本的。

在 **Windows**下,如果你不确定的话，可选择32-位版本。64-位Windows系统也可以运行32-位软件。译者注：建议还是使用32-位版本的，

(译者注：建议还是使用32-位版本的，本人64-位Windows系统使用64-位版本时，貌似Side Bar的菜单有点问题)

**Linux** 下可以运行下面的命令来查看操作系统的类型：

    uname -m

**OS X**, 可以忽略这个选项，OS X下只有一个版本的Sublime Text。

Windows
=======

便携的 or 非便携的?
-------------------------

Sublime Text对Windows有两种风格的版本：普通版，和便携版。如果你对便携版有所了解可以使用它，否则最好使用普通版本。

**普通安装版** 把数据分开在两个目录：对应的安装文件夹，和 *data 目录*。后面会解释这些概念。普通安装版同时也会集成Sublime Text到Windows菜单。

**便携安装版** 把所有Sublime Text所有需要运行的文件都放在一个目录下。 你可以把这个文件夹移动到其它地方，编辑器仍可以正常工作。

如何安装普通版Sublime Text
-------------------------------------------------

下载安装程序，运行并按界面提示安装。

如何安装便携版Sublime Text
----------------------------------------------------

下载压缩吧，解压到指定位置。
解压目录下会有 *sublime_text.exe* 可执行文件。

OS X
====

以Sublime Text 2为例

下载并打开 *.dmg*文件，然后把Sublime Text 2拖拽到 *Applications*文件夹下。

Linux
=====

以Sublime Text 2为例

你可以手动下载安装包并解压。不过你可以通过命令行来完成。

**For i386**

::

    cd ~
    wget http://c758482.r82.cf2.rackcdn.com/Sublime\ Text\ 2.0.1.tar.bz2
    tar vxjf Sublime\ Text\ 2.0.1.tar.bz2

**For x64**

::

    cd ~
    wget http://c758482.r82.cf2.rackcdn.com/Sublime Text 2.0.1 x64.tar.bz2
    tar vxjf Sublime\ Text\ 2.0.1\ x64.tar.bz2


把解压的目录转移到合适的位置。

::

    sudo mv Sublime\ Text\ 2 /opt/


最后，给命令行调用创建一个 `符号链接(symbolic link)`。

::

    sudo ln -s /opt/Sublime\ Text\ 2/sublime_text /usr/bin/sublime


Ubuntu下，如果你要把Sublime Text添加到Unity启动器的话，继续阅读。

首先需要创建一个新的文件。

::

    sudo sublime /usr/share/applications/sublime.desktop


把下面这些内容复制进去。

::

    [Desktop Entry]
    Version=2.0.1
    Name=Sublime Text 2
    # Only KDE 4 seems to use GenericName, so we reuse the KDE strings.
    # From Ubuntu's language-pack-kde-XX-base packages, version 9.04-20090413.
    GenericName=Text Editor

    Exec=sublime
    Terminal=false
    Icon=/opt/Sublime Text 2/Icon/48x48/sublime_text.png
    Type=Application
    Categories=TextEditor;IDE;Development
    X-Ayatana-Desktop-Shortcuts=NewWindow

    [NewWindow Shortcut Group]
    Name=New Window
    Exec=sublime -n
    TargetEnvironment=Unity

如果你已经注册了Sublime Text许可，但是每次启动时都要你输入license,可以尝试执行下面这个命令。

::

    sudo chown -R username:username /home/username/.config /sublime-text-2

把 `username` 替换成你的用户名。这样就可以避免输入license之后以root权限打开Sublime Text的权限错误。


勇于尝试 or Not
============================

Sublime Text 有三个发布 *通道*:

* `Stable`_ (默认)
* `Dev`_
* `Nightly`_

.. _Stable: http://www.sublimetext.com/2
.. _Dev: http://www.sublimetext.com/dev
.. _Nightly: http://www.sublimetext.com/nightly

如果你做的是NASA项目或者正处于deadline的话，你还是使用stable releases吧。 **Stable releases** 经过良好的测试，比其它版本都更加稳定。大于一个月会发布一次更新。 **大多数用户都只需要使用稳定版本**。

*dev* 和 *nightly* 通道是不稳定版本，意味着他们可能有很多bug，不那么可靠。它们比stable releases更新得更频繁。

**Dev builds** 所有人都可以使用。平均来看，每2个月会发布一次。它并不是给所有人准备的，它们会展现一些新功能。

**nightly builds** 是一个边缘版本，会频繁的更新，同时也会频繁的引发问题。尝试它们会非常的有趣，不过你要自己承担风险。Nightly 版本 **只开放给注册用户使用**。
