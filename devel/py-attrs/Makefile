PORTNAME=	attrs
PORTVERSION=	23.1.0
CATEGORIES=	devel python
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

BROKEN_purecap=	requires missing CheriABI Python
USE_PKG64=	1

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Python attributes without boilerplate
WWW=		https://github.com/python-attrs/attrs

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

# Note: sysutils/py-psutil comes from devel/py-pytest-xdist[psutil]
BUILD_DEPENDS=	${PYTHON_PKGNAMEPREFIX}hatch-fancy-pypi-readme>=0:devel/py-hatch-fancy-pypi-readme@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}hatch-vcs>=0:devel/py-hatch-vcs@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}hatchling>=0:devel/py-hatchling@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}setuptools>=63.1.0:devel/py-setuptools@${PY_FLAVOR}
TEST_DEPENDS=	${PYTHON_PKGNAMEPREFIX}cloudpickle>=0:devel/py-cloudpickle@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}hypothesis>=0:devel/py-hypothesis@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}mypy>=1.1.1:devel/py-mypy@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}psutil>=3.0:sysutils/py-psutil@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}Pympler>=0:devel/py-pympler@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pytest-xdist>=0:devel/py-pytest-xdist@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}zope.interface>=0:devel/py-zope.interface@${PY_FLAVOR}

USES=		python
USE_PYTHON=	autoplist concurrent pep517 pytest

NO_ARCH=	yes

.include <bsd.port.pre.mk>

.if ${PYTHON_REL} < 31100
TEST_DEPENDS+=	${PYTHON_PKGNAMEPREFIX}pytest-mypy-plugins>=0:devel/py-pytest-mypy-plugins@${PY_FLAVOR}
.endif

.include <bsd.port.post.mk>
