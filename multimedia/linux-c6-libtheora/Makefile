# Created by: Johannes Meixner <johannes@perceivon.net>
# $FreeBSD$

PORTNAME=	libtheora
PORTVERSION=	1.1.0
PORTREVISION=	3
CATEGORIES=	multimedia linux

MAINTAINER=	emulation@FreeBSD.org
COMMENT=	Theora Video Compression Codec (Linux  CentOS ${LINUX_DIST_VER})

CONFLICTS=	linux-libtheora-[0-9]* linux-f10-libtheora[0-9]*

USES=		linux:c6
USE_LINUX_RPM=	yes

RPMVERSION=	2.el6
USE_LDCONFIG=	yes

PORTDOCS=	COPYING README
DESCR=		${.CURDIR}/../${PORTNAME}/pkg-descr

.include <bsd.port.mk>
