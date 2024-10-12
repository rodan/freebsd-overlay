PORTNAME=	cwiticald
DISTVERSION=1.4
CATEGORIES=	sysutils

MAINTAINER=	petre.rodan@subdimension.ro
COMMENT=	an EGD-compatible server for a TrueRNG device
WWW=		https://github.com/rodan/cwiticald

LICENSE=	GPLv3
LICENSE_FILE=${WRKSRC}/LICENSE

BUILD_DEPENDS=gmake:devel/gmake \
        gsed:textproc/gsed \
		pkg-config:devel/pkgconf
LIB_DEPENDS=libevent.so:devel/libevent

USES=		gmake compiler pkgconfig
USE_GITHUB=	yes
GH_ACCOUNT=	rodan
GH_TUPLE=	rodan:cwiticald:v1.4
BUILD_WRKSRC=   ${WRKSRC}/src
INSTALL_TARGET=	install-strip

do-install:
	${INSTALL_PROGRAM} ${BUILD_WRKSRC}/cwiticald ${STAGEDIR}${PREFIX}/bin
	${INSTALL_MAN} ${WRKSRC}/doc/cwiticald.1 ${STAGEDIR}${PREFIX}/share/man/man1

.include <bsd.port.mk>
