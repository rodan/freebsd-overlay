PORTNAME=	daemontools-scripts
DISTVERSION=20241011
CATEGORIES=	sysutils

MAINTAINER=	petre.rodan@subdimension.ro
COMMENT=	Scripts for daemontools's supervisor
WWW=		https://github.com/rodan/daemontools-scripts

LICENSE=	BSD2CLAUSE
LICENSE_FILE=${WRKSRC}/LICENSE

RUN_DEPENDS=svscanboot:sysutils/daemontools

USE_GITHUB=	yes
GH_ACCOUNT=	rodan
GH_TUPLE=	rodan:daemontools-scripts:20241011

NO_BUILD= yes

do-install:
	${INSTALL_SCRIPT} ${BUILD_WRKSRC}/scripts/runsvcscript.sh ${STAGEDIR}${PREFIX}/bin
	${INSTALL_DATA} ${BUILD_WRKSRC}/scripts/svcscript.conf ${STAGEDIR}${PREFIX}/etc
	${LN} -s runsvcscript.sh ${STAGEDIR}${PREFIX}/bin/svcinit

.include <bsd.port.mk>
