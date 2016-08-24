ifneq ($(KERNELRELEASE),)

obj-m		:= sunxi-cedrus.o

sunxi-cedrus-y	:= sunxi_cedrus.o sunxi_cedrus_hw.o sunxi_cedrus_dec.o

else
KDIR ?= /lib/modules/$(uname -r)/build

default:
	$(MAKE) -C $(KDIR) M=$$PWD
endif
