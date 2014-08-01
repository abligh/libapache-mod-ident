# Makefile for mod_ident2.c (gmake)
# $Id:$

#APXS2=/path/to/your/apxs
APXS2=`which apxs2`

default:
	@echo mod_ident2:
	@echo author: andrew@scoop.co.nz
	@echo
	@echo following options available:
	@echo \"make ident2\" to compile the 2.0 version
	@echo \"make install\" to install the 2.0 version
	@echo
	@echo change path to apxs if this is not it: \"$(APXS2)\"


ident2: mod_ident2.o
	@echo make done, type \"make install\" to install mod_ident2-2.0

mod_ident2.o: mod_ident2.c
	$(APXS2) -c -n $@ mod_ident2.c

mod_ident2.c:

install: mod_ident2.o
	$(APXS2) -i -n mod_ident2.so mod_ident2.la

clean:
	rm -rf *~ *.o *.so *.lo *.la *.slo .libs/
