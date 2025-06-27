all: ja/share/man/man1/rbenv.1
.PHONY: all

ja/share/man/man1/rbenv.1: ja/share/man/man1/rbenv.1.adoc ja/Makefile
	${MAKE} --directory ja share/man/man1/rbenv.1

ja/Makefile: ../Makefile
	ln $< $@

translate: ja/share/man/man1/rbenv.1.adoc
.PHONY: translate

ja/share/man/man1/rbenv.1.adoc: po/ja.po ../share/man/man1/rbenv.1.adoc po4a.cfg po/en.pot credit.md credit.adoc
	po4a po4a.cfg

po/en.pot:
	touch $@

remotes:
	git remote | grep mainstream \
		|| git remote add mainstream https://github.com/rbenv/rbenv
	git remote --verbose
.PHONY: remotes
