KBUILD_CFLAGS := $(subst -O3,-O2,$(KBUILD_CFLAGS))
KBUILD_CFLAGS := $(subst -march=armv8-a+crc+crypto -mtune=cortex-a57.cortex-a53 -mcpu=cortex-a57.cortex-a53,,$(KBUILD_CFLAGS))
KBUILD_CFLAGS := $(subst --param l1-cache-size=32 --param l1-cache-line-size=64 --param l2-cache-size=2048,,$(KBUILD_CFLAGS))
KBUILD_CFLAGS := $(subst --param simultaneous-prefetches=6 --param prefetch-latency=400 -ffast-math,,$(KBUILD_CFLAGS))

motosh-objs := motosh_core.o \
		motosh_flash.o \
		motosh_ioctl.o \
		motosh_irq.o \
		motosh_queue.o \
		motosh_reset.o \
		motosh_wake_irq.o \
		motosh_display.o \
		motosh_time.o \
		motosh_touch.o \
		motosh_antcap.o
obj-$(CONFIG_MMI_HALL_NOTIFICATIONS) += motosh_mmi_notifications.o
obj-$(CONFIG_SENSORS_MOTOSH) += motosh.o
