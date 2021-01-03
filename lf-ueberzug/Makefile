.POSIX:

PREFIX = /usr/local
ifeq ($(XDG_CONFIG_HOME),)
	XDG_CONFIG_HOME="${HOME}/.config"
endif

install:
	mkdir -p "${DESTDIR}${PREFIX}/bin"
	cp -f lf-ueberzug lf-ueberzug-cleaner lf-ueberzug-previewer \
		"${DESTDIR}${PREFIX}/bin"
	chmod 755 "${DESTDIR}${PREFIX}/bin/lf-ueberzug" \
		"${DESTDIR}${PREFIX}/bin/lf-ueberzug-cleaner" \
		"${DESTDIR}${PREFIX}/bin/lf-ueberzug-previewer"
	mkdir -p "${DESTDIR}${XDG_CONFIG_HOME}/lf-ueberzug"
	cp -f lfrc-ueberzug "${DESTDIR}${XDG_CONFIG_HOME}/lf-ueberzug"

uninstall:
	rm -f "${DESTDIR}${PREFIX}/bin/lf-ueberzug" \
		"${DESTDIR}${PREFIX}/bin/lf-ueberzug-cleaner" \
		"${DESTDIR}${PREFIX}/bin/lf-ueberzug-previewer"
	rm -rf "${DESTDIR}${XDG_CONFIG_HOME}/lf-ueberzug"
