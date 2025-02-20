# 6.12

patches for kernel-blu 6.12

- `0001-kernel-blu-base.patch`
	- base patch to be applied, includes all upstream config changes and additions to build the blu kernel
- `0002-drm-amdgpu-enable-SI-and-CIK-support-by-default.patch`
	- simple patch to enable the use of the amdgpu driver on SI and CIK family GPUs
	- while no one reported any breakage yet the amdgpu is not tested or designed for older radeon GPUs and may cause undesirable effects, you can use the radeon driver by launching with `radeon.si_support=1 amdgpu.si_support=0` or `radeon.cik_support=1 amdgpu.cik_support=0`
- `0003-tkg-misc-additions.patch`
	- simple miscellaneous additions inherited from [linux-tkg](https://github.com/Frogging-Family/linux-tkg/tree/master)
	- https://github.com/Frogging-Family/linux-tkg/blob/master/linux-tkg-patches/6.12/0012-misc-additions.patch 
- `0004-cachy-bore.patch`
	- patch for the [bore scheduler](https://github.com/firelzrd/bore-scheduler) inherited from [CachyOS](https://cachyos.org/)
	- https://github.com/CachyOS/kernel-patches/blob/master/6.12/sched/0001-bore.patch
- `0006-drm-i915-quirks-disable-async-page-flipping-on-some-.patch`
	- patch to add a quirk and cmdline option which disables async page flipping under i915 which may cause multi GPU systems to run into a race condition preventing further display output
- `0007-ASUS-ROG-Ally.patch`
	- patch to improve compatibility with the ROG Ally Hardware contributed by a variety of people
- `0008-Steam-Deck.patch`
	- patch to improve compatibility with Steam Deck hardware usually directly from valve or community members
- `0009-blu-misc-additions.patch`
	- various simple miscellaneous additions
- `0010-uinput.patch`
    - input related stuff

the linux surface were dropped for the time being due to it not having rebased to 6.13 yet