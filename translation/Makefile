all: ja/share/man/man1/rbenv.1
.PHONY: all

ja/share/man/man1/rbenv.1: ja/share/man/man1/rbenv.1.adoc ja/Makefile
	${MAKE} --directory ja share/man/man1/rbenv.1

ja/Makefile: ../Makefile
	ln $< $@

ja/share/man/man1/rbenv.1.adoc: po/ja.po ../share/man/man1/rbenv.1.adoc po4a.cfg po/en.pot credit.md credit.adoc
	po4a po4a.cfg

po/en.pot:
	touch $@
