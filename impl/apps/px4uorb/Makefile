#
# Copyright 2014, NICTA
#
# This software may be distributed and modified according to the terms of
# the BSD 2-Clause license. Note that NO WARRANTY is provided.
# See "LICENSE_BSD2.txt" for details.
#
# @TAG(NICTA_BSD)
#

# Targets
TARGETS := px4uorb.bin

# Source files required to build the target
CPPFILES := $(SOURCE_DIR)/src/uORBDevices_posix.cpp
CPPFILES += $(SOURCE_DIR)/src/uORBManager_posix.cpp
CPPFILES += $(SOURCE_DIR)/src/uORBTest_UnitTest.cpp
CPPFILES += $(SOURCE_DIR)/src/objects_common.cpp
CPPFILES += $(SOURCE_DIR)/src/Publication.cpp
CPPFILES += $(SOURCE_DIR)/src/Subscription.cpp
CPPFILES += $(SOURCE_DIR)/src/uORBUtils.cpp
CPPFILES += $(SOURCE_DIR)/src/uORB.cpp
CPPFILES += $(SOURCE_DIR)/src/uORBMain.cpp
ASMFILES := $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/crt/arch-${ARCH}/crt0.S))

NK_CFLAGS += -D_BSD_SOURCE -O2

CPPFLAGS := -Os -D__PX4_POSIX -D__PX4_LINUX -Dnoreturn_function=
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4mathlib/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4systemlib/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4eigen/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libuclibc++/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4drivers/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include/platforms
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include/platforms/posix/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../apps/px4uorb/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../apps/px4uorb/include/uORB
CPPFLAGS += -fvisibility=hidden -include visibility.h -fpermissive
CPPFLAGS += -std=c++11 -nostdinc++ -fno-exceptions -fno-rtti

# Libraries required to build the target
LIBS := c sel4 refossys refos datastruct uclibc++ px4drivers px4compat

# Custom linker script
NK_LDFLAGS += -T $(SOURCE_DIR)/linker.lds

include $(SEL4_COMMON)/common.mk
