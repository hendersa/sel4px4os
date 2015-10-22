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

CFLAGS := -Os

include $(SEL4_COMMON)/common.mk
