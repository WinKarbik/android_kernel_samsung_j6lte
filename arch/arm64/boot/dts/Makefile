dtb-$(CONFIG_SOC_EXYNOS7870) += exynos7870-j6lte_cis_ser_00.dtb exynos7870-j6lte_cis_ser_02.dtb

targets += dtbs

DTB_NAMES := $(subst $\",,$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES))
ifneq ($(DTB_NAMES),)
DTB_LIST := $(addsuffix .dtb,$(DTB_NAMES))
else
DTB_LIST := $(dtb-y)
endif
targets += $(DTB_LIST)

dtbs: $(addprefix $(obj)/, $(DTB_LIST))
 
clean-files := dts/*.dtb *.dtb*
