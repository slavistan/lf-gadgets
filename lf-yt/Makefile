.POSIX:

PREFIX = /usr/local
ifeq ($(XDG_CONFIG_HOME),)
	XDG_CONFIG_HOME="${HOME}/.config"
endif

install:
	mkdir -p "${DESTDIR}${PREFIX}/bin"
	cp -f lf-yt lf-yt-cleaner lf-yt-previewer \
		"${DESTDIR}${PREFIX}/bin"
	chmod 755 "${DESTDIR}${PREFIX}/bin/lf-yt" \
		"${DESTDIR}${PREFIX}/bin/lf-yt-cleaner" \
		"${DESTDIR}${PREFIX}/bin/lf-yt-previewer"
	mkdir -p "${DESTDIR}${XDG_CONFIG_HOME}/lf-yt"
	cp -f lfrc-yt "${DESTDIR}${XDG_CONFIG_HOME}/lf-yt"

uninstall:
	rm -f "${DESTDIR}${PREFIX}/bin/lf-yt" \
		"${DESTDIR}${PREFIX}/bin/lf-yt-cleaner" \
		"${DESTDIR}${PREFIX}/bin/lf-yt-previewer"
	rm -rf "${DESTDIR}${XDG_CONFIG_HOME}/lf-yt"
