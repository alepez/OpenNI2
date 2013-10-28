include ../../../ThirdParty/PSCommon/BuildSystem/CommonDefs.mak

ALLOW_WARNINGS = 1

BIN_DIR = ../../../Bin

INC_DIRS = \
	../../../Include \
	../../../ThirdParty/PSCommon/XnLib/Include \
    /usr/include/libfreenect

SRC_FILES = \
	*.cpp

ifeq ("$(OSTYPE)","Darwin")
	INC_DIRS += /opt/local/include
	LIB_DIRS += /opt/local/lib
	LDFLAGS += -framework CoreFoundation -framework IOKit
endif

LIB_NAME = Freenect

LIB_DIRS = ../../../ThirdParty/PSCommon/XnLib/Bin/$(PLATFORM)-$(CFG)
USED_LIBS = XnLib dl pthread freenect
ifneq ("$(OSTYPE)","Darwin")
        USED_LIBS += rt  
endif

CFLAGS += -Wall -std=c++0x -D__linux__ -Di386

OUT_DIR := $(OUT_DIR)/OpenNI2/Drivers

include ../../../ThirdParty/PSCommon/BuildSystem/CommonCppMakefile
