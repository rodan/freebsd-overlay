PORTNAME=	authprogs
DISTVERSION=0.9.201
CATEGORIES=	sysutils

MAINTAINER=	petre.rodan@subdimension.ro
COMMENT=	ssh command authenticator
WWW=		https://github.com/11001100/authprogs

LICENSE=	GPLv3
LICENSE_FILE=${WRKSRC}/LICENSE

USE_GITHUB=	yes
GH_ACCOUNT=	11001100
GH_TUPLE=	11001100:authprogs:0.9.201
#BUILD_WRKSRC=   ${WRKSRC}/src
#INSTALL_TARGET=	install-strip

do-install:
	${INSTALL_PROGRAM} ${BUILD_WRKSRC}/src/authprogs ${STAGEDIR}${PREFIX}/bin

.include <bsd.port.mk>
