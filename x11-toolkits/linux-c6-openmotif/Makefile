# Created by: Johannes Meixner <johannes@perceivon.net>
# $FreeBSD$

PORTNAME=	openmotif
PORTVERSION=	2.3.3
PORTREVISION=	2
CATEGORIES=	x11-toolkits linux

MAINTAINER=	emulation@FreeBSD.org
COMMENT=	Motif toolkit libraries (Linux CentOS ${LINUX_DIST_VER})

CONFLICTS=	linux-openmotif-[0-9]* linux-f8-openmotif-[0-9]*

USES=		linux:c6
RPMVERSION=	8.el6
USE_LINUX_RPM=	yes
USE_LINUX=	xorglibs
USE_LDCONFIG=	yes
DESCR=	${.CURDIR}/../open-motif/pkg-descr

post-extract:
		@${RM} -r ${WRKSRC}/etc ${WRKSRC}/usr/bin ${WRKSRC}/usr/include \
			${WRKSRC}/usr/share

.include <bsd.port.mk>
