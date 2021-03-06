# Created by: Pete Fritchman <petef@databits.net>
# $FreeBSD$

PORTNAME=	xxdiff
PORTVERSION=	4.0
CATEGORIES=	textproc
MASTER_SITES=	SF

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Graphical file and directories comparator and merge tool

LICENSE=	GPLv2+
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		bison gmake tar:bz2
USE_QT4=	gui moc_build qmake_build uic_build

BUILD_WRKSRC=	${WRKSRC}/src

PLIST_FILES=	bin/xxdiff
PORTDOCS=	*

OPTIONS_DEFINE=	DOCS

.include <bsd.port.pre.mk>

# base flex(1) v2.5.4 is not sufficient
.if ${OPSYS} == FreeBSD && ${OSVERSION} < 1000033
BUILD_DEPENDS+=	${LOCALBASE}/bin/flex:textproc/flex

post-patch:
	@${REINPLACE_CMD} -e 's!flex!${LOCALBASE}/bin/&!' \
		${BUILD_WRKSRC}/xxdiff.pro
.endif

pre-build:
	@(cd ${BUILD_WRKSRC} && ${SETENV} ${MAKE_ENV} QMAKE=${QMAKE} \
		${MAKE_CMD} -f Makefile.bootstrap ${MAKE_ARGS} Makefile)

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/bin/xxdiff ${STAGEDIR}${PREFIX}/bin

do-install-DOCS-on:
	cd ${WRKSRC}/doc && ${COPYTREE_SHARE} "${PORTDOCS} ! -name Makefile" \
		${STAGEDIR}/${DOCSDIR}

.include <bsd.port.post.mk>
