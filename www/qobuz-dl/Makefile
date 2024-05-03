COMMENT = 	A complete Lossless and Hi-Res music downloader for Qobuz
V =	0.9.9.10
CATEGORIES =	www
HOMEPAGE = 	https://github.com/vitiko98/qobuz-dl

# GPL 3.0
MAINTAINER = 	Anjeel <emaill@mail.com>
PERMIT_PACKAGE = 	Yes
GH_ACCOUNT = 	vitiko98
GH_PROJECT =	qobuz-dl
GH_COMMIT =	8096e6cf65856638065bfd95302ece8195a9e218

MODULES =	lang/python
MODPY_PYBUILD =	setuptools
WRKDIST =	${WRKDIR}/qobuz-dl-${GH_COMMIT}
DISTNAME=	qobuz-dl-${V}

RUN_DEPENDS = 	devel/py-pathvalidate \
		www/py-requests \
		audio/py-mutagen \
		devel/py-tqdm \
		devel/py-pick \
		www/py-beautifulsoup4 \
		devel/py-colorama

.include	<bsd.port.mk>
