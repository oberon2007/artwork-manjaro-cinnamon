#!/usr/bin/make -f

THEME      =    cinnamon
PREFIX     = 	/usr
DPATH 	   =	$(DESTDIR)$(PREFIX)/share/backgrounds/$(THEME)
DXMLGNOME  =    $(DESTDIR)$(PREFIX)/share/gnome-background-properties
DEL 	   =  	rm -Rf
INSTD 	   =	install -Dm644 -t

install:
	./backgrounds-xml.sh
	mkdir -p $(DXMLGNOME)
	cp -f $(THEME).xml $(DXMLGNOME)
	$(INSTD) $(DPATH) *.jpg
	$(INSTD) $(DPATH) *.png
	
uninstall:
	$(DEL) $(DPATH)
	rm -f $(DXMLGNOME)/$(THEME).xml
