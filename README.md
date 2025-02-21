esta es una modificacion para utilizarse en freetz

#!/bin/bash

git clone --depth 1 --recursive -b dtls https://github.com/home-assistant/libcoap.git
cd libcoap
./autogen.sh
#LDFLAGS=-static ./configure  --build=i386-linux-gnu --target=mipsel-linux --host=mipsel-linux   --disable-ipv6  --without-included-gettext --disable-nls --without-gnutls --without-pthread  --disable-documentation --disable-shared --without-debug  CC="/home/francisco/freetz-ng/toolchain/target/bin-ccache/mipsel-linux-gcc"   CFLAGS="-Os -pipe -march=4kc -Wa,--trap -D COAP_DEBUG_FD=stderr"
./configure --build=i386-linux-gnu --target=mipsel-linux --host=mipsel-linux   --disable-documentation --disable-shared --without-debug CC="/home/francisco/freetz-ng/toolchain/target/bin-ccache/mipsel-linux-gcc"   CFLAGS="-Os -pipe -march=4kc -Wa,--trap -D COAP_DEBUG_FD=stderr"
make
make install



![WhatsApp Image 2025-02-21 at 13 51 36](https://github.com/user-attachments/assets/9c224a59-cada-4b6a-ac37-ed8a97a234ce)
![WhatsApp Image 2025-02-21 at 13 51 36 (1)](https://github.com/user-attachments/assets/cb616299-0412-4ff5-9740-c5da319b0118)








libcoap: A C implementation of IETF Constrained Application Protocol (RFC 7252)

Copyright (C) 2010--2015 by Olaf Bergmann <bergmann@tzi.org>

ABOUT LIBCOAP
=============

libcoap is a C implementation of a lightweight application-protocol
for devices that are constrained their resources such as computing
power, RF range, memory, bandwith, or network packet sizes. This
protocol, CoAP, is standardized by the IETF as RFC 7252. For further
information related to CoAP, see <http://coap.technology>.

PACKAGE CONTENTS
================

This directory contains a protocol parser and basic networking
functions for platform with support for malloc() and BSD-style
sockets. The examples directory contains a client and a server to
demonstrate the use of this library. 

LICENSE INFORMATION
===================

This library is published as open-source software without any warranty
of any kind. Use is permitted under the terms of the GNU General
Public License (GPL), Version 2 or higher, OR the simplified BSD
license. Please refer to LICENSE.GPL oder LICENSE.BSD for further
details.

