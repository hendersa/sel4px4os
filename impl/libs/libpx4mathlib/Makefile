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
TARGETS := libpx4mathlib.a

# Source files required to build the target
CPPFILES := $(SOURCE_DIR)/src/test/test.cpp
CPPFILES += $(SOURCE_DIR)/src/Limits.cpp

# Header files/directories this library provides
HDRFILES := $(wildcard $(SOURCE_DIR)/include/*)

CPPFLAGS := -Os -D__PX4_POSIX -D__PX4_LINUX -Dnoreturn_function= 
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4mathlib/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4systemlib/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4eigen/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libuclibc++/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include/platforms
CPPFLAGS += -I$(SEL4_COMMON)/../../../../apps/px4uorb/include
CPPFLAGS += -fvisibility=hidden -include visibility.h -fpermissive
CPPFLAGS += -std=c++11 -nostdinc++ -fno-exceptions -fno-rtti

include $(SEL4_COMMON)/common.mk
