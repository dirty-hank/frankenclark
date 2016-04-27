KBUILD_CFLAGS := $(subst -O3,-O2,$(KBUILD_CFLAGS))
KBUILD_CFLAGS := $(subst -march=armv8-a+crc+crypto -mtune=cortex-a57.cortex-a53 -mcpu=cortex-a57.cortex-a53,,$(KBUILD_CFLAGS))
KBUILD_CFLAGS := $(subst --param l1-cache-size=32 --param l1-cache-line-size=64 --param l2-cache-size=2048,,$(KBUILD_CFLAGS))
KBUILD_CFLAGS := $(subst --param simultaneous-prefetches=6 --param prefetch-latency=400 -ffast-math,,$(KBUILD_CFLAGS))

ccflags-y += -Idrivers/media/platform/msm/camera_v2
ccflags-y += -Idrivers/media/platform/msm/camera_v2/sensor
ccflags-y += -Idrivers/media/platform/msm/camera_v2/codecs
ccflags-y += -Idrivers/media/platform/msm/camera_v2/isps
ccflags-y += -Idrivers/media/platform/msm/camera_v2/pproc
ccflags-y += -Idrivers/media/platform/msm/camera_v2/msm_vb2
ccflags-y += -Idrivers/media/platform/msm/camera_v2/camera
ccflags-y += -Idrivers/media/platform/msm/camera_v2/jpeg_10
ccflags-y += -Idrivers/media/platform/msm/camera_v2/fd

obj-$(CONFIG_MSMB_CAMERA) += msm.o
obj-$(CONFIG_MSMB_CAMERA) += camera/
obj-$(CONFIG_MSMB_CAMERA) += msm_vb2/
obj-$(CONFIG_MSMB_CAMERA) += sensor/
obj-$(CONFIG_MSMB_CAMERA) += pproc/
obj-$(CONFIG_MSMB_CAMERA) += isp/
obj-$(CONFIG_MSMB_CAMERA) += ispif/
obj-$(CONFIG_MSMB_JPEG) += jpeg_10/
obj-$(CONFIG_MSMB_CAMERA) += msm_buf_mgr/
obj-$(CONFIG_MSM_FD) += fd/
obj-$(CONFIG_MSMB_CAMERA) += cci_intf.o
