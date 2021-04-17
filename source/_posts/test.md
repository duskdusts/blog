pkg install -y nodejs-lts
pkg install -y git
pkg install openssh
npm install -g hexo-cli
mkdir blog
hexo init blog
cd blog
npm install
npm install hexo-renderer-pug hexo-renderer-stylus --save
npm install hexo-deployer-git --save
git clone -b master https://github.com/Molunerfinn/hexo-theme-melody themes/melody
hexo clean&&hexo g&&hexo d
git config --global user.name "duskdust"
git config --global user.email "czy@live.in"
ssh-keygen -t rsa -C "czy@live.in"
cat ~/.ssh/id_rsa.pub
ssh -T git@e.coding.net
termux-setup-storage
cp -rv ~/blog ~/storage/shared/blog
坑
https://e.coding.net/duskdust/duskdust.git



https://mobile.yangkeduo.com/goods2.html?goods_id=134029050508&page_from=101&pxq_secret_key=IILGYZOYHLSFBKNQ6FTP2FF6TO75IAD6DJ4I2XAMOU4IIZXY6GHQ&share_uin=N4M7LPK7NBXK6QBM4D4YHSMV2I_GEXDA&refer_share_id=eb7e336aa4f347a8987fa4e4e100670a&refer_share_uid=4744876276&refer_share_channel=copy_link&refer_share_form=text..