#
# Makefile for gemreadout package
#

Project=cmsgemos
ShortProject=gem
Package=gemreadout
LongPackage=gemreadout
ShortPackage=readout
PackageName=readout

GEMREADOUT_VER_MAJOR=0
GEMREADOUT_VER_MINOR=2
GEMREADOUT_VER_PATCH=0

include $(BUILD_HOME)/$(Project)/config/mfDefs.gem

Sources =version.cc
#Sources+=GEMDataParker.cc
Sources+=GEMReadoutApplication.cc GEMReadoutWebApplication.cc
#Sources+=GEMDataChecker.cc

DynamicLibrary=gemreadout

IncludeDirs+=$(BUILD_HOME)/$(Project)/$(Package)/include
IncludeDirs+=$(BUILD_HOME)/$(Project)/gemutils/include
IncludeDirs+=$(BUILD_HOME)/$(Project)/gembase/include
IncludeDirs+=$(ROOTDIR)/include

DependentLibraryDirs+=$(BUILD_HOME)/$(Project)/gemutils/lib/$(XDAQ_OS)/$(XDAQ_PLATFORM)
DependentLibraryDirs+=$(BUILD_HOME)/$(Project)/gembase/lib/$(XDAQ_OS)/$(XDAQ_PLATFORM)

LibraryDirs+=$(ROOTLIBS)
LibraryDirs+=$(ROOTGLIBS)

UserCFlags +=$(ROOTCFLAGS)
UserCCFlags+=$(ROOTCFLAGS)

DependentLibraries+=gemutils gembase

UserDynamicLinkFlags+=$(ROOTLIBS)

include $(XDAQ_ROOT)/config/Makefile.rules
include $(BUILD_HOME)/$(Project)/config/mfRPM_gem.rules

print-env:
	@echo BUILD_HOME    $(BUILD_HOME)
	@echo XDAQ_ROOT     $(XDAQ_ROOT)
	@echo XDAQ_OS       $(XDAQ_OS)
	@echo XDAQ_PLATFORM $(XDAQ_PLATFORM)
	@echo LIBDIR        $(LIBDIR)
	@echo ROOTCFLAGS    $(ROOTCFLAGS)
	@echo ROOTLIBS      $(ROOTLIBS)
	@echo ROOTGLIBS     $(ROOTGLIBS)
	@echo GIT_VERSION   $(GIT_VERSION)
	@echo GEMDEVELOPER  $(GEMDEVELOPER)
	@echo CC            $(CC)
	@echo CPP           $(CPP)
	@echo CXX           $(CXX)
	@echo LD            $(LD)
	@echo AR            $(AR)
	@echo NM            $(NM)
	@echo RANLIB        $(RANLIB)
	@echo GCCVERSION    $(GCCVERSION)
	@echo CLANGVERSION  $(CLANGVERSION)
