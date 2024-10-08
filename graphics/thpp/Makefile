PORTNAME=	thpp
DISTVERSION=20241008
CATEGORIES=	graphics

MAINTAINER=	petre.rodan@subdimension.ro
COMMENT=	Thermal processing panel - viewer and analyzer of radiometric images
WWW=		https://github.com/rodan/thpp

LICENSE=		GPLv3
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=gmake:devel/gmake \
	gsed:textproc/gsed
LIB_DEPENDS=libglfw.so:graphics/glfw \
	libGLX.so:graphics/libglvnd
RUN_DEPENDS=exiftool:graphics/p5-Image-ExifTool

USES=		gmake compiler:c++17-lang pkgconfig
USE_GITHUB=	yes
GH_ACCOUNT=	rodan
GH_TUPLE=	rodan:thpp:20241008 \
	ocornut:imgui:v1.91.3-docking:imgui/lib/imgui \
	epezent:implot:f156599faefe316f7dd20fe6c783bf87c8bb6fd9:implot/lib/implot \
	lvandeve:lodepng:ed3c5f14b136c936d615ee3b38aaa7e7e642f12c:lodepng/lib/lodepng \
	jkriege2:TinyTIFF:4.0.1.0:tinytiff/lib/TinyTIFF
BUILD_WRKSRC=   ${WRKSRC}/src

do-install:
	${INSTALL_PROGRAM} ${BUILD_WRKSRC}/thpp ${STAGEDIR}${PREFIX}/bin
	@${MKDIR} ${STAGEDIR}${DATADIR}
	${INSTALL_DATA} ${WRKSRC}/src/res/dir_icon.png ${STAGEDIR}${DATADIR}
	${INSTALL_DATA} ${WRKSRC}/src/res/file_icon.png ${STAGEDIR}${DATADIR}
	${INSTALL_DATA} ${WRKSRC}/src/res/imgui.ini ${STAGEDIR}${DATADIR}

.include <bsd.port.mk>
