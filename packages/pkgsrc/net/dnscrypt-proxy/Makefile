
DISTNAME=	dnscrypt-proxy-1.0
CATEGORIES=	net
MASTER_SITES=	https://github.com/downloads/opendns/dnscrypt-proxy/

MAINTAINER=	dnscrypt@opendns.com
HOMEPAGE=	http://github.com/opendns/dnscrypt-proxy/
COMMENT=	secure communications between a client and a DNS resolver
LICENSE=	modified-bsd

PKG_DESTDIR_SUPPORT=	user-destdir

GNU_CONFIGURE=		yes
CONFIGURE_ARGS+=	--sysconfdir=${PKG_SYSCONFDIR}
CONFIGURE_ARGS+=	--localstatedir=${VARBASE}

BUILD_DEFS+=		VARBASE

.include "../../mk/bsd.prefs.mk"

RCD_SCRIPTS=		dnscrypt_proxy
INSTALLATION_DIRS=	share/doc/dnscrypt-proxy

post-install:
	cd ${WRKSRC} &&	\
		${INSTALL_DATA} README.markdown	 \
			${DESTDIR}${PREFIX}/share/doc/dnscrypt-proxy

.include "../../mk/bsd.pkg.mk"
