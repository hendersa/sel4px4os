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
TARGETS := libpx4controllib.a

# Source files required to build the target
CFILES := $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/src/*.c))
CPPFILES := $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/src/*.cpp))
CPPFILES := $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/src/uorb/*.cpp))
CPPFILES := $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/src/block/*.cpp))

# Header files/directories this library provides
HDRFILES := $(wildcard $(SOURCE_DIR)/include/*)

CPPFLAGS := -Os -D__PX4_POSIX -D__PX4_LINUX
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4mathlib/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4systemlib/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4eigen/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libuclibc++/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4controllib/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4controllib/include/controllib/block
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include/platforms
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4uorb/include
CPPFLAGS += -fvisibility=hidden -include visibility.h -fpermissive
CPPFLAGS += -std=c++11 -nostdinc++ -fno-exceptions -fno-rtti

include $(SEL4_COMMON)/common.mk
