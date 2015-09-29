---
 layout: detail
 title: window7上 ruby + selenium-webdriver 环境搭建
 description: 自动化测试环境搭建
 category: core
 tags: [core]
---

###安装包下载

1. 从ruby官网下载ruby1.9.3-p551安装包

  点击链接下载[http://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-1.9.3-p551.exe](http://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-1.9.3-p551.exe)

2. 从ruby官网下载DevKit安装包

  点击链接下载[http://dl.bintray.com/oneclick/rubyinstaller/DevKit-tdm-32-4.5.2-20111229-1559-sfx.exe](http://dl.bintray.com/oneclick/rubyinstaller/DevKit-tdm-32-4.5.2-20111229-1559-sfx.exe)

3. 不同的ruby版本需要不同的DevKit，可以到ruby官网自行下载

  ruby官网下载地址[http://rubyinstaller.org/downloads/](http://rubyinstaller.org/downloads/)

### ruby1.9.3-p551安装

1. 双击安装文件rubyinstaller-1.9.3-p551.exe

  ![弹出如下设置语言界面](/pictures/ruby_install/SetupLanguae.jpg)
  
2. 默认选择English，点击OK

  ![接受license并点击Next](/pictures/ruby_install/Next.jpg)

3. 进入安装页面，
  
  ![选择安装路径并勾选三个可选项](/pictures/ruby_install/Install.jpg),点击Install

4. 进入自动安装页面，大约1分钟，安装完成，自动跳转到

  ![安装完成页面](/pictures/ruby_install/Finish.jpg)

5. 命令行确认ruby安装是否安装成功

  在开始->所有程序->Ruby 1.9.3-p551找到Start Command Prompt with Ruby，单击运行命令行
  
  输入如下命令
  
  >ruby -v 
  
  ruby 1.9.3p551 (2014-11-13) [i386-mingw32]
  
  查看到ruby版本信息表示安装成功

6. 命令行检查rubygem是否安装

  >gem -v
  
  1.8.29
  
  查看到gem版本表示rubygem已经安装

7. 命令行更新rubygem

  >gem update --system
  
  ......
  
  RubyGems system software updated
  
  几分钟后更新完成，更新过程没有出现error
  
8. 再次查看gem版本，显示更新后的版本

  >gem -v
  
  2.4.8

###Devkit安装

1. 双击DevKit-tdm-32-4.5.2-20111229-1559-sfx.exe，
  
  ![指定解压路径](/pictures/DevKit_install/Extract.jpg)

  注意：路径中不能有空格，路径要使用英文，这个路径就是DevKit安装路径

2. 执行如下命令安装DevKit

  >D:

  >cd \DevKit

  >ruby dk.rb init

  >ruby dk.rb install

  执行过程，没有error

3. 验证是否安装成功

  >gem install rdiscount --platform=ruby
  
  此处可能会由于网络原因导致安装失败，可以先跳过此步骤继续后续安装

### Selenium-webdriver安装

1. 命令行执行如下操作安装selenium-webdriver

  >gem install selenium-webdriver

2. 验证是否安装成功

  >gem list selenium-webdriver

  *** LOCAL GEMS ***

  selenium-webdriver (2.47.1)

  查看到版本信息表示安装成功

### rspec安装

1. 执行如下命令安装rspec

  >gem install rspec

  ...

  6 gems installed

  安装过程没有error,表示安装成功

