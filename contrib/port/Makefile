# Created by: Maciej Pasternacki <maciej@3ofcoins.net>
# $FreeBSD$

PORTNAME=	jetpack
PORTVERSION=	0.0.1.20151013
CATEGORIES=	sysutils

MAINTAINER=	maciej@3ofcoins.net
COMMENT=	App Container runtime

LICENSE=	BSD3CLAUSE

BUILD_DEPENDS=	gb>=0.0.0.2015080301:${PORTSDIR}/devel/gb

USE_GITHUB=	yes
GH_ACCOUNT=	3ofcoins
GH_TAGNAME=	5f3218c

USERS=		_jetpack
GROUPS=	_jetpack
USE_RC_SUBR=	jetpack_mds

UID_FILES+=	${MASTERDIR}/UIDs
GID_FILES+=	${MASTERDIR}/GIDs

MAKE_ARGS=	prefix=${LOCALBASE}
USES=		compiler

.include <bsd.port.pre.mk>

# golang assumes that if clang is in use, it is called "clang" and not "cc". If
# it's called "cc", go fails.
.if ${COMPILER_TYPE} == clang
CC=	clang
.endif

.include <bsd.port.post.mk>
