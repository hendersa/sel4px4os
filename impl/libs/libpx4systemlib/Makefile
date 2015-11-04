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
CFILES := $(SOURCE_DIR)/src/perf_counter.c
CFILES += $(SOURCE_DIR)/src/param/param.c
CFILES += $(SOURCE_DIR)/src/conversions.c
CFILES += $(SOURCE_DIR)/src/cpuload.c
CFILES += $(SOURCE_DIR)/src/getopt_long.c
CFILES += $(SOURCE_DIR)/src/pid/pid.c
CFILES += $(SOURCE_DIR)/src/airspeed.c
CFILES += $(SOURCE_DIR)/src/system_params.c
CFILES += $(SOURCE_DIR)/src/mavlink_log.c
CFILES += $(SOURCE_DIR)/src/rc_check.c
CFILES += $(SOURCE_DIR)/src/otp.c
CFILES += $(SOURCE_DIR)/src/board_serial.c
CFILES += $(SOURCE_DIR)/src/pwm_limit/pwm_limit.c
CFILES += $(SOURCE_DIR)/src/mcu_version.c
CFILES += $(SOURCE_DIR)/src/bson/tinybson.c
CFILES += $(SOURCE_DIR)/src/circuit_breaker_params.c
CPPFILES := $(SOURCE_DIR)/src/circuit_breaker.cpp

# Header files/directories this library provides
HDRFILES := $(wildcard $(SOURCE_DIR)/include/*)

CPPFLAGS := -Os -D__PX4_POSIX -D__PX4_LINUX -Dnoreturn_function=
CPPFLAGS += -D_XOPEN_SOURCE=700
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4mathlib/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4systemlib/include/systemlib
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4systemlib/include/systemlib/pid
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4systemlib/include/systemlib/pwm_limit
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4systemlib/include/systemlib/bson
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libuclibc++/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include/platforms
CPPFLAGS += -I$(SEL4_COMMON)/../../../../px4include/platforms/posix/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4uorb/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4geo/include
CPPFLAGS += -I$(SEL4_COMMON)/../../../../libs/libpx4geo_lookup/include
CPPFLAGS += -fvisibility=hidden -include visibility.h -fpermissive
CPPFLAGS += -std=c++11 -nostdinc++ -fno-exceptions -fno-rtti

include $(SEL4_COMMON)/common.mk
