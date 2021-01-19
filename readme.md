### 安装tt
```sh
yum install gcc gnutls-devel zlib-devel pcre-devel make cmake git -y
git clone https://github.com/scandum/tintin.git tt
cd tt/src
./configure
make install
rm  -rf tt
```
### vim编辑脚本时中文乱码
```sh
vi ~/.vimrc
```
内容
```
syntax on
set t_Co=256
set bg=dark
set autoindent
set hlsearch
colorscheme murphy
set fileencodings=utf-8,ucs-bom,gb18030,gbk,gb2312,cp936
set termencoding=utf-8
set encoding=utf-8
"set number
```
##
脚本中文乱码转换编码
1.vim按ESC键退出编辑模式后输入下列命令：
` :set fileencoding=gb18030 `

2.批量转换脚本编码
使用 gbktoutf8 工具进行转换。
## vim语法高亮
`cd ~ && git clone https://github.com/LokiChaos/vim-tintin.git .vim`

## 目录结构
framework 放框架
etc 放用户配置，用户配置其实也是主程序，脚本入口
data 放数据（为了脱敏脚本）
utils 放一些常用触发和别名
plugins 放插件，插件分全局插件，增强插件，机器人，任务等等
log 放日志，日志分类，加时间戳，分用户