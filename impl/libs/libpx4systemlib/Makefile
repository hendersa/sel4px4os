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
TARGETS := libpx4systemlib.a

# Source files required to build the target
CPPFILES := $(patsubst $(SOURCE_DIR)/%,%,$(wildcard $(SOURCE_DIR)/src/*.cpp))

# Header files/directories this library provides
HDRFILES := $(wildcard $(SOURCE_DIR)/include/*)

CPPFLAGS := -Os -D__PX4_POSIX -D__PX4_LINUX
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4mathlib/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include/platforms
CPPFLAGS += -I$(SEL4_COMMON)/../../../../apps/px4uorb/include

include $(SEL4_COMMON)/common.mk