include depends.mk

CONFIGURE=./configure \
	--prefix=$(PREFIX) \
	--build=$(BUILD) \
	--host=$(HOST) \

SRC=../../../

all: configure
	(cd $(SRC); make -j$(JOBS))

autogen:
	(cd $(SRC); ./autogen.sh)

configure: autogen
	(cd $(SRC); $(CONFIGURE))

install:
	(cd $(SRC); make install)
