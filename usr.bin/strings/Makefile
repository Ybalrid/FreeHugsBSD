# $FreeBSD$

.include <src.opts.mk>

ELFTCDIR=	${SRCTOP}/contrib/elftoolchain

.PATH: ${ELFTCDIR}/strings

PROG=	strings

LIBADD=	elftc elf

.if ${MK_CASPER} != "no" && !defined(BOOTSTRAPPING)
LIBADD+=	casper
LIBADD+=	cap_fileargs
CFLAGS+=	-DWITH_CASPER
.endif

CFLAGS+=-I${ELFTCDIR}/libelftc -I${ELFTCDIR}/common

.include <bsd.prog.mk>
