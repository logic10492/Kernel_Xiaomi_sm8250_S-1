obj-$(CONFIG_KSU)	+= kernelsu.o
kernelsu-$(CONFIG_KSU)	:= ksu.o allowlist.o apk_sign.o module_api.o sucompat.o uid_observer.o lsm_hook.o kprobe_hook.o 
obj-$(CONFIG_KSU)	+= selinux/

ifdef CONFIG_KSU
ifndef EXPECTED_SIZE
EXPECTED_SIZE := 0x033b
endif
ifndef EXPECTED_HASH
EXPECTED_HASH := 0xb0b91415
endif
ccflags-y += -DEXPECTED_SIZE=$(EXPECTED_SIZE)
ccflags-y += -DEXPECTED_HASH=$(EXPECTED_HASH)
ccflags-y += -Wno-implicit-function-declaration -Wno-strict-prototypes -Wno-int-conversion -Wno-gcc-compat
ccflags-y += -Wno-macro-redefined -Wno-declaration-after-statement
endif
