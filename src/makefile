# 此文件由makeobj.sh自动生成
############################################################
# 项目名 : 
# 模块名 : 
# 备  注 : 
############################################################

###### 源文件配置区
#@ c_FILE
c_FILE		=	\
			list.c \
			rbtree.c \
			rbtree_ins.c \
			LOGC.c \
			tcpdaemon_lib.c \

c_FILE2		=	\
			tcpdaemon_main.c \

###### 目标文件、安装目录配置区
include makeinstall
LIB		=	libtcpdaemon.a
LIBINST		=	$(HOME)/lib
BIN		=	tcpdaemon
BININST		=	$(HOME)/bin
HDER		=	tcpdaemon.h
HDERINST	=	$(HOME)/include/tcpdaemon

###### 编译选项
CFLAGS		=	$(_CFLAGS) \

###### 链接选项
LFLAGS		=	$(_LFLAGS) \
			-lpthread \
			-ldl \

###### 额外宏定义区
CLEAN_ADDITION	=

###### 加载mktpl模板库
#@ make_all
#@ make_clean
#@ make_install
#@ make_install_LIBINST
#@ make_install_BININST
#@ make_install_HDERINST
#@ make_install_DFTHDERINST
#@ make_uninstall
#@ make_uninstall_LIBINST
#@ make_uninstall_BININST
#@ make_uninstall_HDERINST
#@ make_uninstall_DFTHDERINST
include $(MKTPLDIR)/makeobj_$(MKTPLOS).inc

###### 目标文件依赖关系
libtcpdaemon.a	:	${c_FILE_o}
	$(AR) $(ARFLAGS) $@ ${c_FILE_o}

tcpdaemon	:	${c_FILE_o} ${c_FILE2_o}
	$(CC) $(ESOFLAGS) -o $@ ${c_FILE_o} ${c_FILE2_o} $(LFLAGS)

