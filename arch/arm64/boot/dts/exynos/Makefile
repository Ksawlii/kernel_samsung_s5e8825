# SPDX-License-Identifier: GPL-2.0
dtb-$(CONFIG_ARCH_EXYNOS) += \
	exynos5433-tm2.dtb	\
	exynos5433-tm2e.dtb	\
	exynos7-espresso.dtb \
	s5e8825.dtb

ifeq ($(CONFIG_ARCH_EXYNOS),y)
dtbo-y += samsung/a25x/a25x_swa_open_w00_r00.dtbo
dtbo-y += samsung/a25x/a25x_swa_open_w00_r04.dtbo
dtbo-y += samsung/a25x/a25x_swa_open_w00_r05.dtbo
endif

targets += dtbs
DTB_LIST  := $(dtb-y) $(dtbo-y)
always-y    := $(DTB_LIST)

dtbs: $(addprefix $(obj)/, $(DTB_LIST))

clean-files := *.dtb*
