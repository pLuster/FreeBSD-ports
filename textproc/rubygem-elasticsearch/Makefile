# Created by: Ryan Steinmetz <zi@FreeBSD.org>
# $FreeBSD$
#
# NOTE: This port must be updated at the same time as textproc/rubygem-elasticsearch-api
# and textproc/rubygem-elasticsearch-transport

PORTNAME=	elasticsearch
PORTVERSION=	1.0.15
CATEGORIES=	textproc rubygems
MASTER_SITES=	RG

MAINTAINER=	ruby@FreeBSD.org
COMMENT=	Ruby integrations for Elasticsearch

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

RUN_DEPENDS=	rubygem-elasticsearch-api=${PORTVERSION}:textproc/rubygem-elasticsearch-api \
		rubygem-elasticsearch-transport=${PORTVERSION}:textproc/rubygem-elasticsearch-transport

NO_ARCH=	yes
USE_RUBY=	yes
USE_RUBYGEMS=	yes
RUBYGEM_AUTOPLIST=	yes

.include <bsd.port.mk>
