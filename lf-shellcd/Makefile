.POSIX:

ifeq ($(XDG_CONFIG_HOME),)
	XDG_CONFIG_HOME="${HOME}/.config"
endif

install:
	mkdir -p "${DESTDIR}${XDG_CONFIG_HOME}/lf-shellcd"
	cp -f lfrc-shellcd lf-shellcd "${DESTDIR}${XDG_CONFIG_HOME}/lf-shellcd"

uninstall:
	rm -rf "${DESTDIR}${XDG_CONFIG_HOME}/lf-shellcd"
