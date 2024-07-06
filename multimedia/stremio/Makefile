COMMENT = 		Stremio desktop app
V = 			4.4.168
DISTNAME =		stremio-${V}
CATEGORIES =		multimedia
HOMEPAGE = 		https://github.com/stremio/stremio-shell
MAINTAINER =		Anjeel <email@mail.com>
COMMIT = 		88ae5efba002d6a2451fea6f450b7de6db535d78

# GPL 3.0
PERMIT_PACKAGE = 	Yes
WRKDIST =		${WRKDIR}/stremio-shell-${COMMIT}

DIST_TUPLE += 		github Stremio stremio-shell ${COMMIT} .
DIST_TUPLE +=		github Ivshti libmpv b0eae77cf6dc59aaf142b7d079cb13a0904fd3ee deps/libmpv
DIST_TUPLE += 		github itay-grudev SingleApplication aede311d28d20179216c5419b581087be2a8409f deps/singleapplication


BUILD_DEPENDS = net/curl \
			x11/gnome/librsvg  \
			devel/cmake \
			x11/qt5/qtbase \
			x11/qt5/qtwebengine \
			x11/qt5/qtwebchannel \
			multimedia/mpv

RUN_DEPENDS = 	multimedia/mpv \
			lang/node \
			x11/qt5/qtbase \
			x11/qt5/qtdeclarative \
			x11/qt5/qtquickcontrols \
			x11/qt5/qtquickcontrols2 \
			x11/qt5/qtwebengine \
			x11/qt5/qttranslations \
			x11/qt5/qtwebchannel 

do-build:
	cd ${WRKDIST} && \
	qmake-qt5 stremio.pro -spec openbsd-clang && \
	Qt5_DIR=/usr/local/lib/qt5/cmake make -f release.makefile PREFIX=build/

do-install: 
	cd ${WRKDIST} && \
	make -f release.makefile install

post-install:
	ln -sf /usr/local/share/stremio/stremio /usr/local/bin/stremio

.include <bsd.port.mk>

