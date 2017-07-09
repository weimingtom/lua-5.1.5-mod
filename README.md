# lua-5.1.5-mod

# How to compile
## Download source code
	git clone https://github.com/zhaojh329/lua-5.1.5-mod.git
	cd lua-5.1.5-mod

## Set cross compiler paths based on your environment
	TARGET_CROSS=/home/zjh/lede/staging_dir/toolchain-mipsel_24kc_gcc-5.4.0_musl/bin/mipsel-openwrt-linux-

## Compile
	make CC="${TARGET_CROSS}gcc" AR="${TARGET_CROSS}ar rcu" RANLIB="${TARGET_CROSS}ranlib" PKG_VERSION=5.1.5 CFLAGS=-fPIC linux

## Copy library to your cross compiler
	cp -a src/liblua.so* xxxxxx/lib/