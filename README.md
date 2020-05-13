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

■ notes  
After I construct qmailadmin-1.2.16 and vpopmail-5.4.33 on CentOS 7.4.1708 and Virtualbox,  
I input items at 'Add Forward Account's page and 'add autorespond's page'  
and push "add button",then,blank page is displayed.  
I modify "alias.c" and "autorespond.c" and make patch files.  if you need, please use.  

patch < alias_mod.patch  
patch < autorespond_mod.patch  
