---
 layout: detail
 title: window7�� ruby + selenium-webdriver �����
 description: �Զ������Ի����
 category: core
 tags: [core]
---

###��װ������

1.��ruby��������ruby1.9.3-p551��װ��
�����������[http://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-1.9.3-p551.exe](http://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-1.9.3-p551.exe)
2.��ruby��������DevKit��װ��
�����������[http://dl.bintray.com/oneclick/rubyinstaller/DevKit-tdm-32-4.5.2-20111229-1559-sfx.exe](http://dl.bintray.com/oneclick/rubyinstaller/DevKit-tdm-32-4.5.2-20111229-1559-sfx.exe)
3.��ͬ��ruby�汾��Ҫ��ͬ��DevKit�����Ե�ruby������������
ruby�������ص�ַ[http://rubyinstaller.org/downloads/](http://rubyinstaller.org/downloads/)

###ruby1.9.3-p551��װ

1.˫����װ�ļ�rubyinstaller-1.9.3-p551.exe
![���������������Խ���](/pictures/ruby_install/SetupLanguae.jpg)
2.Ĭ��ѡ��English�����OK��
![����license�����Next](/pictures/ruby_install/Next.jpg)

3.���밲װҳ�棬![ѡ��װ·������ѡ������ѡ��](/pictures/ruby_install/Install.jpg),���Install
4.�����Զ���װҳ�棬��Լ1���ӣ���װ��ɣ��Զ���ת��![��װ���ҳ��](/pictures/ruby_install/Finish.jpg)
5.������ȷ��ruby��װ�Ƿ�װ�ɹ�
�ڿ�ʼ->���г���->Ruby 1.9.3-p551�ҵ�Start Command Prompt with Ruby����������������
������������
>ruby -v
ruby 1.9.3p551 (2014-11-13) [i386-mingw32]
�鿴��ruby�汾��Ϣ��ʾ��װ�ɹ�

6.�����м��rubygem�Ƿ�װ
>gem -v
1.8.29
�鿴��gem�汾��ʾrubygem�Ѿ���װ

7.�����и���rubygem
>gem update --system
......
RubyGems system software updated
�����Ӻ������ɣ����¹���û�г���error
8.�ٴβ鿴gem�汾����ʾ���º�İ汾
>gem -v
2.4.8

###Devkit��װ

1.˫��DevKit-tdm-32-4.5.2-20111229-1559-sfx.exe��![ָ����ѹ·��](/pictures/DevKit_install/Extract.jpg)
ע�⣺·���в����пո�·��Ҫʹ��Ӣ�ģ����·������DevKit��װ·��

2.ִ���������װDevKit
>D:
>cd \DevKit
>ruby dk.rb init
>ruby dk.rb install
ִ�й��̣�û��error
3.��֤�Ƿ�װ�ɹ�
>gem install rdiscount --platform=ruby
�˴����ܻ���������ԭ���°�װʧ�ܣ������������˲������������װ

###Selenium-webdriver��װ

1.������ִ�����²�����װselenium-webdriver
>gem install selenium-webdriver
2.��֤�Ƿ�װ�ɹ�
>gem list selenium-webdriver
*** LOCAL GEMS ***

selenium-webdriver (2.47.1)
�鿴���汾��Ϣ��ʾ��װ�ɹ�

###rspec��װ

1.ִ���������װrspec
>gem install rspec
...
6 gems installed
��װ����û��error,��ʾ��װ�ɹ�

