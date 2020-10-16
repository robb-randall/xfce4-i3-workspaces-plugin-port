# $FreeBSD$

PORTNAME=       xfce4-i3-workspaces-plugin
DISTVERSION=    1.3.2
CATEGORIES=     x11

DISTFILES=      ${DISTVERSION}${EXTRACT_SUFX}

MAINTAINER=     robb.randall@gmail.com
COMMENT=        Workspace switcher plugin for xfce4-panel which can be used for the i3 window manager

LICENSE=        GPLv3
LICENSE_FILE_GPLv3=     ${WRKSRC}/COPYING

ONLY_FOR_ARCHS=	amd64 \
		i386

USES=		gettext \
		gmake \
		gnome \
		libtool \
		pkgconfig \
		xfce \
		xorg

GH_ACCOUNT=	denesb

LIB_DEPENDS=	libfontconfig.so:x11-fonts/fontconfig \
		libfreetype.so:print/freetype2 \
		libjson-glib-1.0.so:devel/json-glib

BUILD_DEPENDS=	intltool>0:textproc/intltool \
		json-glib>=0:devel/json-glib \
		xfce4-dev-tools>=0:devel/xfce4-dev-tools

USE_GNOME+=	atk \
		cairo \
		gdkpixbuf2 \
		glib20 \
		gtk20 \
		pango

USE_XFCE+=	libmenu \
		libutil \
		panel \

USE_XORG=	xcb

GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--prefix=${DESTDIR}/${GNU_CONFIGURE_PREFIX} MAKE=${GMAKE}
CONFIGURE_SCRIPT=	autogen.sh

INSTALL_TARGET=	install-strip

.include <bsd.port.mk>
