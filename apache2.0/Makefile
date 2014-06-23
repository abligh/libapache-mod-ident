# Makefile for mod_ident.c (gmake)
# $Id:$

#APXS2=/path/to/your/apxs
APXS2=`which apxs2`

default:
	@echo mod_ident:
	@echo author: andrew@scoop.co.nz
	@echo
	@echo following options available:
	@echo \"make ident\" to compile the 2.0 version
	@echo \"make install\" to install the 2.0 version
	@echo
	@echo change path to apxs if this is not it: \"$(APXS2)\"


ident: mod_ident.o
	@echo make done, type \"make install\" to install mod_ident-2.0

mod_ident.o: mod_ident.c
	$(APXS2) -c -n $@ mod_ident.c

mod_ident.c:

install: mod_ident.o
	$(APXS2) -i -n mod_ident.so mod_ident.la

clean:
	rm -rf *~ *.o *.so *.lo *.la *.slo .libs/
