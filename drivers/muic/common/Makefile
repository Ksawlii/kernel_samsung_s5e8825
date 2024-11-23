#
# Makefile for muic devices
#
subdir-ccflags-y := -Wformat

ifeq ($(CONFIG_SM_COMMON),y)
obj-$(CONFIG_MUIC_NOTIFIER)	+= common_muic_sm.o
common_muic_sm-y	:= muic-core_sm.o muic_notifier_sm.o muic_param_sm.o
common_muic_sm-$(CONFIG_MUIC_COMMON_SYSFS) += muic_sysfs_sm.o
else
obj-$(CONFIG_MUIC_NOTIFIER)	+= common_muic.o
common_muic-y	:= muic-core.o muic_notifier.o muic_param.o
common_muic-$(CONFIG_MUIC_COMMON_SYSFS) += muic_sysfs.o
endif

ifeq ($(CONFIG_SEC_KUNIT),y)
ifeq ($(CONFIG_SM_COMMON),y)
GCOV_PROFILE_muic-core_sm.o := $(CONFIG_SEC_KUNIT)
else
GCOV_PROFILE_muic-core.o := $(CONFIG_SEC_KUNIT)
endif
endif
