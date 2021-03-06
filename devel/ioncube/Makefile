# Created by: Svyatoslav Lempert <svyatoslav.lempert@gmail.com>
# $FreeBSD$

PORTNAME=	ioncube
DISTVERSION=	6.0.4
CATEGORIES=	devel
MASTER_SITES=	http://downloads3.ioncube.com/loader_downloads/ \
		http://dl.ispsystem.info/ioncube/${DISTVERSION}/ \
		http://downloads2.ioncube.com/loader_downloads/
DISTNAME=	${PORTNAME}_loaders_fre_${VER}_${ARCH:S,i386,x86,:S,amd64,x86-64,}
DIST_SUBDIR=	${PORTNAME}/${DISTVERSION}

MAINTAINER=	svyatoslav.lempert@gmail.com
COMMENT=	Loader for ionCube-encoded PHP files

ONLY_FOR_ARCHS=	i386 amd64
NO_BUILD=	yes
USES=		php

SUB_FILES=	pkg-message
WRKSRC=		${WRKDIR}/${PORTNAME}

VER=	9
IGNORE_DragonFly=	is unsupported on DragonFly

PHP_INSTVER=	${PHP_VERSION:C/^([0-9]+\.[0-9]+).*/\1/}

do-install:
	@${MKDIR} ${STAGEDIR}${PREFIX}/lib/php/${PHP_EXT_DIR}/ioncube/
	${INSTALL_DATA} ${WRKSRC}/ioncube_loader_fre_${PHP_INSTVER}.so \
		${STAGEDIR}${PREFIX}/lib/php/${PHP_EXT_DIR}/ioncube/ioncube_loader.so
	${INSTALL_DATA} ${WRKSRC}/ioncube_loader_fre_${PHP_INSTVER}_ts.so \
		${STAGEDIR}${PREFIX}/lib/php/${PHP_EXT_DIR}/ioncube/ioncube_loader_ts.so
# Put it before opcache, like the previous pkg-message was saying
	@${MKDIR} ${STAGEDIR}${PREFIX}/etc/php
	@${ECHO_CMD} "[Zend]" > ${STAGEDIR}${PREFIX}/etc/php/ext-05-ioncube.ini
	@${ECHO_CMD} "zend_extension=${PREFIX}/lib/php/${PHP_EXT_DIR}/ioncube/ioncube_loader.so" >> ${STAGEDIR}${PREFIX}/etc/php/ext-05-ioncube.ini
	@${ECHO_CMD} "zend_extension_ts=${PREFIX}/lib/php/${PHP_EXT_DIR}/ioncube/ioncube_loader_ts.so" >> ${STAGEDIR}${PREFIX}/etc/php/ext-05-ioncube.ini

.include <bsd.port.mk>
