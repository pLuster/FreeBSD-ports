# Created by: Ed Schouten <ed@FreeBSD.org>
# $FreeBSD$

PKGNAMEPREFIX=	cloudabi-
PKGNAMESUFFIX=	-aarch64

MAINTAINER=	ed@FreeBSD.org
COMMENT=	GNU Binutils for CloudABI cross-development

MASTERDIR=	${.CURDIR}/../binutils
PATCHDIR=	${.CURDIR}/files
PLIST=		${.CURDIR}/pkg-plist

BUTARGET=	aarch64-unknown-cloudabi
BUREMOVE=	ar dlltool nlmconv nm objdump ranlib size windmc windres

.include "${MASTERDIR}/Makefile"
