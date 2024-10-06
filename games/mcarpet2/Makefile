PORTNAME=	mcarpet2
DISTVERSION=20241006
CATEGORIES=	games

MAINTAINER=	petre.rodan@subdimension.ro
COMMENT=	Magic Carpet 2 port
WWW=		https://github.com/rodan/magic_carpet_2

LICENSE=		BULLFROG_PROD
LICENSE_NAME=	Bullfrog Productions License
LICENSE_FILE=	${FILESDIR}/LICENSE
LICENSE_PERMS=	dist-mirror pkg-mirror auto-accept

LIB_DEPENDS=libpng.so:graphics/png \
	libfmt.so:devel/libfmt \
	libspdlog.so:devel/spdlog \
	libboost_system.so:devel/boost-libs
RUN_DEPENDS= 7zz:archivers/7-zip \
	bchunk:sysutils/bchunk \
	wget:ftp/wget

USES=		cmake:noninja compiler:c++11-lang pkgconfig sdl openal shebangfix
SHEBANG_FILES=	assets/scripts/mcarpet2 assets/scripts/mcarpet2_install.sh
USE_SDL=	sdl2 image2 mixer2 ttf2
USE_GITHUB=	yes
GH_ACCOUNT=	rodan
GH_TUPLE=	rodan:magic_carpet_2:20241006 \
	benhoyt:inih:r58:inih/lib/inih \
	ocornut:imgui:v1.91.3:imgui/lib/imgui \
	MathieuTurcotte:findfirst:2c4733bb77cb3357c691c7a6b7a46baeed2d5fe1:findfirst/lib/findfirst \
	aminosbh:sdl2-cmake-modules:ad006a3daae65a612ed87415037e32188b81071e:sdl2cmake/assets/sdl2-cmake-modules

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/assets/scripts/mcarpet2 ${STAGEDIR}${PREFIX}/bin
	${INSTALL_SCRIPT} ${WRKSRC}/assets/scripts/mcarpet2_install.sh ${STAGEDIR}${PREFIX}/bin
	@${MKDIR} ${STAGEDIR}${DATADIR}/font
	${INSTALL_DATA} ${WRKSRC}/assets/font/8x8-font.bmp ${STAGEDIR}${DATADIR}/font
	${INSTALL_DATA} ${WRKSRC}/assets/font/16x16-font.bmp ${STAGEDIR}${DATADIR}/font
	${INSTALL_DATA} ${WRKSRC}/assets/config_3d_pro.ini ${STAGEDIR}${DATADIR}
	${INSTALL_DATA} ${WRKSRC}/assets/config_attack_3.ini ${STAGEDIR}${DATADIR}
	${INSTALL_DATA} ${WRKSRC}/assets/config_xbox.ini ${STAGEDIR}${DATADIR}
	${INSTALL_PROGRAM} ${BUILD_WRKSRC}/src/remc2 ${STAGEDIR}${DATADIR}
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/README.md ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/README_OpenAL ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/README_controllers ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
