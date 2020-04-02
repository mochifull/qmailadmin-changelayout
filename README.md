# qmailadmin-changelayout

■ purpose  
to modify qmailadmin's page

■ used enviroment  
qmailadmin-1.2.16

■ used skill to modify  
・jQuery  
・Popper  
・Bootstrap  

■ modified existing resources(qmailadmin-1.2.16\html)  
all except colortable,footer.html,header.html

■ added resoures(qmailadmin-1.2.16\images\)  
added 'assets'folder including bootstrap,jquery and popper'js and each page's css etc

■ construct enviroment  
copy above resoureces against local test enviroment and excute Command below

cd qmailadmin-1.2.16  
./configure  --enable-htmldir=/var/www/html  --enable-cgibindir=/var/www/cgi-bin　　　※option：depend on your env  
make  
make install-strip  
