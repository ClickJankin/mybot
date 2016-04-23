# �p��b Windows �w�� HUBOT
How Install HUBOT on Windows 

�i�Ѧ�HUBOT�x��[HUBOT](https://hubot.github.com/)���w�˱о� �C<br>   
���H�b�o�̰Ѧ�[HUBOT](https://hubot.github.com/)�x�����оǡA�åΤ�������@�U:memo:

## �w��node and npm
�w�ˤ�k�Ѧ�[ HUBOT ](https://hubot.github.com/)�x����ĳ���ϥ�[ chocolatey ](https://chocolatey.org/) �w�ˡA<br>
�����A�ϥ�<b> �t�κ޲z�� </b>����CMD�A�M���J�H�U���O
```
@powershell -NoProfile -ExecutionPolicy unrestricted -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin
```
�άO<br>
�ϥ�<b> �t�κ޲z�� </b>���� PowerShell �R�O�C�A�M���J�H�U���O
```
iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))
```
�H�W��k��@�اY�i�A�w�ˮɡA���ӷ|�X�{���~�A�Х�<b> �t�κ޲z�� </b>���} PowerShell�A�M�����H�U���O�G
```
Set-ExecutionPolicy RemoteSigned
```
���ۿ� Y(YES)�A�Y�i���Q�w�ˡC

## �w��Node JS
### ��k�@
�ϥ�<b> �t�κ޲z�� </b>���� PowerShell �R�O�C�A�M���J�H�U���O
```
choco install nodejs.install
```
�i��|�ݧA�@�ǪF��A�� 1 YES�C<br>
���� �]�w�����ܼơA<br>
�ϥ�<b> �t�κ޲z�� </b>����CMD�A�M���J�H�U���O
```
setx /M PATH "%PATH%;C:\Program Files\nodejs\"
```
�]�i�H��ʦۤv�]�w�����ܼơA�]�w�n�|�p�U��<br>
![alt tag](http://i.imgur.com/YKlFgrF.jpg)<br>
<br>
### ��k�G
������[ Node.js ](https://nodejs.org/en/)�x���U���A�M��w�ˡC

## �}�l�إ� HUBOT
���w�˥��n�M��A����CMD�A�M���J�H�U���O
```
npm install -g hubot coffee-script yo generator-hubot
```
���ۿ�@�Ӧۤv���w�����|�A����CMD�A�M���J�H�U���O
```
mkdir myhubot
cd myhubot
```
���ۦA��J�H�U���O
```
yo hubot
```
���۷|�ݧA�@�ǭn�]�w���F��A�֦��̡B�����H�W�١B�y�z �BBot adapter�A�򥻤W���ιw�]�N��F�A������Enter<br>
P.S <b> Bot adapter </b> �b�o�̧ڬO��J <b> slack </b> (�i�̷Ӧۤv���ݨD���[ Adapters ](https://hubot.github.com/docs/adapters/) )
![alt tag](http://i.imgur.com/U623K56.jpg)<br>

�}�l�Ұ� HUBOT�A�b�ۤv�Хߪ���Ƨ��̤U�ϥ�CMD�A�M���J�H�U���O�A
�ڭ̥��ϥ�<b> shell adapter </b>�U�h����
```
bin\hubot -a shell
```
�Ұʦ��\��A�i��J���O���աA�Ҧp
```
[�����H�W��] echo [�Q�n�o�X���T��] 
myhubot echo hello
```
�p���[�ݧ�h���O�A�i�H�ϥ�
```
[�����H�W��] help
myhubot help
```
![alt tag](http://i.imgur.com/4yMnqgT.jpg)<br>

�H�W�N�O�ϥ�<b> shell adapter </b>�A<br>

## ���Xhubot-slack
�i�Ѧ�[ hubot-slack](https://github.com/slackhq/hubot-slack)<br>
�b�P��Ƨ����U����CMD�A�M���J�H�U���O
```
npm install -g hubot-slack --save
```
���ۨ�[ Slack](https://slack.com/) �ӽбb���A<br>
�h [https://my.slack.com/services/new/hubot](https://my.slack.com/services/new/hubot) �s�W�@�� Hubot APP�A<br>
�åB���o�ۤv�� API Token<br>
```
HUBOT_SLACK_TOKEN=xoxb-xxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```
![alt tag](http://i.imgur.com/VFHA2og.jpg)<br>
�]�w<b> �����ܼ� </b>�A����CMD�A�M���J�H�U���O<br>
�`�N�A�������঳�Ů�A���M�|�L�k�]�w�����ܼơC
```
set HUBOT_SLACK_TOKEN=xoxb-xxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```
�ϥ�Node.js����A�M���J�H�U���O
```
process.env
```
�p���[�ݯS�w�Ѽƪ��ȡA�i��J�U�C���O
```
process.env.HUBOT_SLACK_TOKEN
```
��h��ƥi�Ѧ� [Node.js](https://nodejs.org/api/process.html)  

���ۦA��J�H�U���O�Mslack�s��
```
bin\hubot -a slack
```
![alt tag](http://i.imgur.com/Dhak4wm.jpg)<br>
���ۦA�^��slack�W�A�i�H�o�{�s�u���\<br>
![alt tag](http://i.imgur.com/DrLXF8C.jpg)<br>

## Deploying to Heroku
�i�Ѧ� [hubot-slack](https://github.com/slackhq/hubot-slack)�A���� [Heroku](https://www.heroku.com/)���U�b���A�A�w�� [Heroku Toolbelt ](https://toolbelt.heroku.com/)�A<br>
����CMD�A�M���J�H�U���O�A��J�ۤv���b���M�K�X
```
% heroku login
Enter your Heroku credentials.
Email: youremail@example.com
Password:
Could not find an existing public key.
Would you like to generate one? [Yn]
Generating new SSH public key.
Uploading ssh public key /Users/you/.ssh/id_rsa.pub
```
Initialize git and make your initial commit
```
% git init
% git add .
% git commit -m "Initial commit"
```
�}�l�гy Heroku APP
```
% heroku create
Creating app... done, stack is cedar-14
https://cryptic-basin-78675.herokuapp.com/ | https://git.heroku.com/cryptic-basin-78675.git
```
���ۿ�J�ۤv�� Heroku APP ���}�H�� APP �W�٥H�� HUBOT_SLACK_TOKEN
```
% heroku config:add HEROKU_URL=https://cryptic-basin-78675.herokuapp.com/ --app cryptic-basin-78675
% heroku config:add HUBOT_SLACK_TOKEN=xoxb-xxxxxxxxxxxxxxxxxxxxxxxxxxxx --app cryptic-basin-78675

Setting config vars and restarting cryptic-basin-78675... done
HUBOT_SLACK_TOKEN: xoxb-xxxxxxxxxxxxxxxxxxxxxxxxxxxx
```
Deploy the bot
```
git push heroku master
```
�G�p��������A�A�^��slack�W�A�i�H�o�{�s�u���\�C<br>
![alt tag](http://i.imgur.com/DrLXF8C.jpg)<br>
�p�G�٦���L�������ܼƭn�]�w�A�i�H�b�H�U�a��]�w�C<br>
![alt tag](http://i.imgur.com/UOKEt7a.jpg)<br>

## ��L�`�N�ƶ�
�p�G�n�ϥ� hubot-scripts �̭����ɮסA���]���ѭn�ϥ� news.coffee�A<br>
news.coffee ���|�� \myhubot\node_modules\hubot-scripts\news.coffee�A<br>
�аO�o�b<b> hubot-scripts.json </b> �̥[�J "news.coffee"�C<br><br>

���pscript�̥X�{ 
```
HTMLParser  = require "cheerio"
```
�N��ݭn�B�~�w�ˡA����CMD�A�M���J�H�U���O
```
npm install cheerio --save
```
�åB�b<b> package.json </b>��<b> dependencies </b>�[�J "cheerio"�H�Ϊ���<br><br>

�p�G�n�ϥ� [hubot-youtube](https://github.com/hubot-scripts/hubot-youtube)�A����CMD�A�M���J�H�U���O<br>
```
npm install hubot-youtube --save
```
�æb<b> external-scripts.json </b>�[�J "hubot-youtube"


## Environment
* Windows 8.1
* npm 3.8.6
* Node 4.4.3
