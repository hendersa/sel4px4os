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
TARGETS := px4navigator.bin

# Source files required to build the target
CFILES   := $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/src/*.c))
CPPFILES := $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/src/*.cpp))
ASMFILES := $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/crt/arch-${ARCH}/crt0.S))

NK_CFLAGS += -D_BSD_SOURCE -O2

CPPFLAGS := -Os -D__PX4_POSIX -D__PX4_LINUX -Dnoreturn_function=
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4mathlib/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4systemlib/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4eigen/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libuclibc++/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4drivers/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4geo/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4geo_lookup/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4controllib/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4controllib/include/controllib
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include/platforms
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include/platforms/posix/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../apps/px4uorb/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../apps/px4uorb/include/uORB
CPPFLAGS += -I$(SEL4_COMMON)/../../../../apps/px4navigator/include/navigator
CPPFLAGS += -fvisibility=hidden -include visibility.h -fpermissive
CPPFLAGS += -std=c++11 -nostdinc++ -fno-exceptions -fno-rtti

# Libraries required to build the target
LIBS := c sel4 refossys refos datastruct uclibc++ px4drivers px4compat px4systemlib px4geo px4geo_lookup px4controllib px4dataman px4fw_pos_control_l1 px4uorb px4mathlib

# Custom linker script
NK_LDFLAGS += -T $(SOURCE_DIR)/linker.lds

include $(SEL4_COMMON)/common.mk
