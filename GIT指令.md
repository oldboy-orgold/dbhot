�й�����ά��Զ�̿�

�����������Լ��һ��GitLab������
����������ʹ�����ơ�Github
�汾���ƹ���

����ʽ��CSV ,SVN,VSS
�ֲ�ʽ��Git��Darcs,...
Git�����в���
1.1���ؿ��ʼ��
�����ļ���

git init
ע�⣺���ɵ� .git Ŀ¼�д�ŵ��Ǳ��ؿ�����ļ�����Ҫɾ��
1.2����ǩ��
��Ŀ(�ֿ�)������ڵ�ǰ���ؿ���Ч

git config user.name tom  #�����û���tom
git config user.email liu@qq.com #�����û�����
ϵͳ�û�������ڵ�ǰ��¼�Ĳ���ϵͳ�û���Ч

git config --global user.name tom
git config --global user.email liu@qq.com
��������һ�� --global

���ȼ�����Ŀ���� > ϵͳ����

��Ϣ����λ�ã�~/.gitconfig �ļ�

1.3��������
1.3.1 ״̬�鿴
git status   #�鿴���������ݴ���״̬
1.3.2 ���
git add fileName  #ָ���ļ�
git add . #����
˵���������������ļ���ӵ��ݴ���
1.3.3 �ύ
git commit -m 'commit message' fileName
˵�������ݴ��������ύ�����ؿ�
1.3.4 �鿴��ʷ��¼
git log 
git reflog  #����
git log --greph #ͼ����ʾ,��ֱ��
git log --pretty=oneline #Ư��һ����ʾ
git log --oneline #�����ʾ
˵����HEAD@{�ƶ�����ǰ�汾��Ҫ���ٲ�}
1.3.5 ǰ������
��������ֵ�Ƽ�

git reset --hard ָ��λ��
���ӣ�git reset --hard a6ace91 #�ص����״̬
ʹ�� ^ ����ֻ�ܺ���

git reset --hard HEAD^
���ӣ�git reset --hard HEAD^^
ע�⣺���� ^ ��ʾ���˼���
ʹ�� ~ ����ֻ�ܺ���

git reset --hard HEAD~n
���ӣ�git reset --hard HEAD~3
1.3.6 reset�����������Ƚ�
soft: 
  - �����ؿ��ƶ�HEAD ָ��
mixed:
  - �ڱ��ؿ��ƶ�HEADָ��
  - �����ݴ���
hard:
  - �ڱ��ؿ��ƶ�HEADָ��
  - �����ݴ���
  - ���ù�����
1.3.7��ɾ���ļ����һ�
�൱�ڽ���һ�����գ���Ȼɾ���ˣ���ֻҪ��ӵ��ݴ����������һ�
git reset --hard ָ��λ��
1.3.8 �ļ�����Ƚ�
git diff �ļ���
git diff ��ϣֵ �ļ���  #����ʷ�е�һ���汾�Ƚ�
git diff  #�����ļ�������Ƚ϶���ļ�
2.2 ��֧����
hot_fix master feature_x feature_y

2.2.1 ʲô�Ƿ�֧����
�ڰ汾�����У�ʹ���ƽ��������
2.2.2 ��֧�ĺô�
ͬʱ�����ƽ�������ܿ�������߿���Ч��
ĳһ��֧����ʧ�ܣ������������֧���κ�Ӱ��
2.2.3 ��֧����
������֧
git branch ��֧��
�鿴��֧
git branch
git branch -v 
�л���֧
git checkout ��֧��
git checkout -b ��֧��   #������֧��ֱ���л����÷�֧
�ϲ���֧�൱�ڰ��޸��˵��ļ�������
git merge xxx
ע�⣺�ϲ���֧��ʱ��Ҫ��ȷ˭˭�ϲ�
	����a��֧�����޸��ˡ�Ҫ�ϲ���master�������л���master��Ȼ��ϲ�b
ɾ����֧
git branch -d ��֧��
2.2.4 �����ͻ
��ͻ�ı���
��ͻ�Ľ��
��һ�����༭��ɾ��������<<< ===
�ڶ������޸ĵ�����λ�ã������˳�
����������ӵ������� git add �ļ���
���Ĳ����ύ�����ؿ�git commit -m '��־��Ϣ' ע�⣺����һ�����ܴ��ļ���
Git ���Github
����� ���� ��֧��

1.1 ����Զ�̿��ַ����
git remote -v  #�鿴Զ�̵�ַ����
git remote add ���� Զ�̵�ַ 
���ӣ�git remote add origin https://xx
1.2 ����
�����޸���ѱ��ؿ���ļ����͵�Զ�ֿ̲� ǰ�����ύ���˱��ؿ�ſ�������

git push ���� ��֧��
git push -u ���� ��֧��    #-uָ��Ĭ������
���ӣ�git push origin master
1.3 ��¡
�����İ�Զ�̿��¡������ ��¡������Ҫ������֧���������� clone����һ�Σ����޵��еĹ��̣�������pull

git clone  Զ�̵�ַ
���ӣ�git clone https://xx
1.4 ��ȡ
���ش���clone�������ļ� ����pull����

pull = fetch + merge
	git fetch ���� ��֧��
	git merge ���� ��֧��
git pull ���� ��֧��
1.5 �����ͻ
ע�⣺�����ͻ����ύ�ǲ��ܴ��ļ�����

������ǻ���Զ�̿����°������޸Ĳ������ͣ�������pull������װ��ͻ�취���

1.6 rebase
�ύ��¼��಻�ֲ� ûѧ�����о��е㼦�� ������

git rebase -i ������
git rebase -i HEAD~3  #�ϲ����������¼
˵������vim�༭����ĳ�s
1.7 beyond compare
����������ͻ

1.��װ ��
   beyond compare 
2.���ã�
   git config --local merge.tool bc3  #�ϲ�����
   git config --local mergetool.path '/usr/local/bin/bcomp' #���·��
   git config --local mergetool.keepBackup false  #False���ñ��汸��
3.Ӧ�ã�
   git mergetool
˵����--localָֻ�ڵ�ǰ����ϵͳ��Ч
1.8 ���ŶӺ���
����review֮��ϲ�

�����ڸ���

�����Ա:Settings --> Collaborators -->��д�û��� -->�����ӽ�������

��ҵ ����һ����֯ �������

review

��֯��review ͨ��Pull request

����Դ�����������

������˲ֿ��fork ���Լ��Ĳֿ� -- > Ȼ��clone���� �޸ĺ����͵�Զ�̿� --> ���Pull Request���� --> Create pull request����Ϣ

1.9 Tag��ǩ
Ϊ�������İ汾������˾һ�㲻��ֱ��ʹ��commit�ύ

git tag -a v1.0 -m '�汾����'   #��������tag��Ϣ
git tag -d v1.0    		#ɾ��tag
git push origin --tags   #������tag��Ϣ���͵�Զ�̿�
git pull origin --tags    #��ȡ������

git checkout v.10    #�л�tag
git clone -b v0.1 ��ַ   #ָ��tag���ش���
1.10 SSH ���ܵ�¼
����:ssh-keygen -t rsa -C GitHub�����ַ
����.sshĿ¼������id_rsa.pub�ļ�����
��¼GitHub��Settings --> SSH and GPG keys --> New SSH Key
�ص�gitͨ��ssh��ַ������git remote add ���� SSH��ַ
Git������
1.1 ����
����Ŀ����������ʹ��Git�ķ�ʽ
1.2 ����
1.2.1 ����ʽ������
��SVNһ��������ʽ��������һ������ֿ⣬���е��޸Ķ��ύ����Master��֧��
1.2.2 GitFlow������ *
���ɷ�֧master ������֧develop �޸���֧hotfix Ԥ������֧release ���ܷ�֧feature

GitFlow �ж����ķ�֧���÷����������̸�������
1.2.3 Forking ������
�� GitFlow �����ϣ� ��������� Git �� Fork �� pull request �Ĺ����Դﵽ������˵�Ŀ�ġ� 
��ȫ�ɿ��ع�����ŶӵĿ�����