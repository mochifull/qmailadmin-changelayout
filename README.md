# qmailadmin-changelayout

■ purpose  
to modify qmailadmin's page  

■ used enviroment  
qmailadmin-1.2.16  
※https://sourceforge.net/projects/qmailadmin/files/qmailadmin-devel/  

■used patch  
qmailadmin-catchall.patch  
※https://notes.sagredo.eu/files/qmail/patches/qmailadmin/qmailadmin-catchall.patch  

■ used skill to modify  
・jQuery  
・Popper  
・Bootstrap  

■ modified existing resources(qmailadmin-1.2.16\html)  
all except colortable,footer.html,header.html  

■ added resoures(qmailadmin-1.2.16\images\)  
added 'assets'folder including bootstrap,jquery and popper'js and each page's css etc  
※to copy 'assests'folder, I modify the 715 row in Makefile.in  

■ construct enviroment  
excute Command below  

tar xvfz  qmailadmin-changelayout.tar.gz  
cd qmailadmin-1.2.16  
./configure  --enable-htmldir=/var/www/html  --enable-cgibindir=/var/www/cgi-bin　　　※option：depend on your env  
make clean  
make  
make install-strip  
