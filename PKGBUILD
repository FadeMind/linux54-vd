# Based on the file created for Arch Linux by:
# Tobias Powalowski <tpowa@archlinux.org>
# Thomas Baechler <thomas@archlinux.org>

# Maintainer: Philip Müller (x86_64) <philm@manjaro.org>
# Maintainer: Jonathon Fernyhough (i686) <jonathon@manjaro.org>
# Contributor: Helmut Stult <helmut[at]manjaro[dot]org>
# Maintainer (vd): torvic9

pkgbase=linux54-vd
pkgname=('linux54-vd' 'linux54-vd-headers')
_basekernel=5.4
_kernelname=-vd
_sub=5
kernelbase=${_basekernel}${_kernelname}
pkgver=${_basekernel}.${_sub}
pkgrel=1
arch=('x86_64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'elfutils' 'git')
options=('!strip')
source=(https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-${pkgver}.tar.{xz,sign}
		# the main kernel config files
		'config.x86_64' 'config.vd' 'config.x200' 'config.x270' 'config.x570' 'x509.genkey' "${pkgbase}.preset"
		# ARCH Patches
		0001-arch-patches-20191217.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.4/arch-patches-v4/0001-arch-patches.patch
        # MANJARO Patches
        0001-amdgpu-Add-DC-feature-mask-to-disable-fractional-pwm.patch
        0002-amdgpu-nonupstream-navi10-vfio-reset.patch
		# amdgpu backports
		0001-amdgpu-sriov-vf-does-not-support-baco.patch
		0002-amdgpu-fix-gfx-vf-flr-fail-on-navi.patch
		0003-amdgpu-explicitly-wait-for-cp-idle.patch
		0004-amdgpu-reinit-clear-state-buffer-after-reset.patch
		0005-amdgpu-update-gfx-golden-settings-20191211.patch
		0006-amdgpu-update-gfx-golden-settings-for-navi14-20191211.patch
		# bmq scheduler
		#bmq-5.4-20191125.patch::https://gitlab.com/alfredchen/bmq/raw/master/5.4/bmq_v5.4-r0.patch
        # sirlucjan
		0001-futex-steam-fsync.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.4/futex-patches-sep/0001-futex-Split-key-setup-from-key-queue-locking-and-rea.patch
		0002-futex-steam-fsync.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.4/futex-patches-sep/0002-futex-Implement-mechanism-to-wait-on-any-of-several-.patch
		0003-futex-steam-fsync.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.4/futex-patches-sep/0003-futex-Change-WAIT_MULTIPLE-opcode-to-31.patch
		0001-clearlinux-tweak-intel-cpuidle.patch::https://raw.githubusercontent.com/clearlinux-pkgs/linux/master/0106-intel_idle-tweak-cpuidle-cstates.patch
		0002-clearlinux-add-config-opt-for-raid6-bench.patch::https://raw.githubusercontent.com/clearlinux-pkgs/linux/master/0109-raid6-add-Kconfig-option-to-skip-raid6-benchmarking.patch
		0003-clearlinux-init-ata-before-graphics.patch::https://raw.githubusercontent.com/clearlinux-pkgs/linux/master/0110-Initialize-ata-before-graphics.patch
		# vd
		0001-tune-vm-and-vfs-settings.patch
		0002-tune-cfs-scheduler.patch
		0003-optimise-module-compression.patch
		0004-add-nvme-hwmon-temp.patch
		0005-cpu-optimisations-graysky.patch
		# hho
		0001-enable-O3-opt-for-all-arches.patch::https://raw.githubusercontent.com/hhoffstaette/kernel-patches/5.4/5.4/kconfig-20191211-enable-O3-for-all-arches.patch
		0002-mm-split-vmalloc_sync_all.patch::https://raw.githubusercontent.com/hhoffstaette/kernel-patches/5.4/5.4/mm-20191009-split-vmalloc_sync_all.patch
		0003-introduce-list-for-each-continue.patch::https://raw.githubusercontent.com/hhoffstaette/kernel-patches/5.4/5.4/"list-20191129-introduce-list_for_each_continue().patch"
		0004-block-perf-optimisations.patch
		0005-net-disable-tcp-ssthresh-cache.patch::https://raw.githubusercontent.com/hhoffstaette/kernel-patches/5.4/5.4/net-20191209-disable-TCP-ssthresh-metrics-cache-by-default.patch
)

validpgpkeys=(
  'ABAF11C65A2970B130ABE3C479BE3E4300411886'  # Linus Torvalds
  '647F28654894E3BD457199BE38DBBDC86092693E'  # Greg Kroah-Hartman
)

sha256sums=('568e9f27fbba86131c2e2849f296d54216e2ed3e8c4d8aa78a93b417cab23ec0'
            'SKIP'
            'db77510e6a269c42d0e67398123187a80fa29db7c4ef10b9873d422f84338391'
            'a86be5e02a6cf81e79b0d022dd560bb341ee1d7a6d7ab4256a19a6a0d4dd7580'
            '975417fe2e60af9abe5743dee4b5170ce125cb669fb675c7f24b1c98e54defa6'
            'e31f869bc553cc8e09fc1a5f50b3e3b5324d74b14b8674fe8e28816784a417be'
            '50f5651c8a9ce3a19e93f372cc48bacbcc055cf41c4409ae0d8ef3d84e690e4a'
            'ab010dc5ef6ce85d352956e5996d242246ecd0912b30f0b72025c38eadff8cd5'
            'c14f60f37c5ef16d104aaa05fdc470f8d6d341181f5370b92918c283728e5625'
            'd3e2903a05d42412bbe7eb1c082208cc47f900e0f5aa9c9c3a470bd13c167a45'
            '1fd4518cb0518d68f8db879f16ce16455fdc2200ed232f9e27fb5f1f3b5e4906'
            '7a2758f86dd1339f0f1801de2dbea059b55bf3648e240878b11e6d6890d3089c'
            'c449d684f27a44c2368622b6f76abb960c03281218d4512969c567371a74afe0'
            '1801216e75c7fc6569be04bc134d8233b6cbaa02f96d5eb58f18429bef724683'
            'fcf767648859ef8ff6a90b598207548ad81a8bf68be75c402ef50a1afb10c3ed'
            'ebb35c21509e4acddff0f912c85bda501ab4eefd2f0bb976c28e4301bf27eda3'
            'ddbc236dcd79174cbb73552453927062af2bb86a5ae97f2631445993be912845'
            '7fbf6328c7df3a98e409c12e66c9584ed57dd717328281d886739c1855e1a1e4'
            'fd1f34cf87e72ccd6070590028ad34e12dc42285637a0c61894680cb81d4fb88'
            '9660f0d31bdc5718b7fde41015898f67dce86602886585848d6300dfce2542db'
            'cd228e4b62cab5679c93cd0eda5d96d570f1b3ba84340eddd2d049f2a07eef9d'
            '88b5597753b01f90f77b99580943263969902ffc084972f8843e0659fdd5eb8f'
            '47d26eb8a2ec74b3684ab61837ecfcdad5cdc40722ca01a32684dfdd3775fafc'
            'b4a3d140bc93e4d224570c0f6b87c40c64148571588064858fcdc9f2406feeaa'
            'f4041dc77564ee6de09c1c02c59068b8eceb6fbdbe60158acdec0a0cfb5cb3f7'
            '949360a832de6c4951433607444c55369703f8a030455609729d7cf11aca7efc'
            '0d6fbf9a5206529d6791d41767ec254f0040d053713092b5fbb21fbe7f3604b7'
            'c6944879f5cdfd335a3adc75b6f6194d127ad93d4dd5bf90d2ad505e83c9b6d2'
            '607097f22f202cd829f12acce7a401fb7f7af5678ffeda90c1fc7da71b895ad7'
            '21eac56173eb18959bbf02c1687dc7fa2c5d1df063ec90e6507f0008ce88bbef'
            '47844884e429ffc395f51610825271c2549d2ab28b52251407d5b4f8a21fe1d9'
            '7f9aa69187e7d197017c6bb15b623330e050a27ba384a3894cbd3e347fdd8a83'
            'b37b2132e97357201e039872c595da18aade6a64743d35ec33ebfd4d4851c3f4'
            '9c006e4845c22808c954ca2374a2a9dd927c192e4bdaf0d00c6abc559831106e')

export KBUILD_BUILD_USER=systemd-run
export KBUILD_BUILD_HOST=manjaro

prepare() {
  local TBOLD=$(tput bold)
  local TNORMAL=$(tput sgr0)
  cd "${srcdir}/linux-${pkgver}"

  # add latest fixes from stable queue, if needed
  # http://git.kernel.org/?p=linux/kernel/git/stable/stable-queue.git
  # enable only if you have "gen-stable-queue-patch.sh" executed before
  #patch -Np1 -i "${srcdir}/prepatch-${_basekernel}`date +%Y%m%d`"
  printf '\n'
  msg2 "APPLYING PATCHES"

  # apply patch from the source array (should be a pacman feature)
  local filename filename2
  for filename in "${source[@]}"; do
  	if [[ "$filename" =~ \.patch$ ]]; then
		filename="${filename%%::*}"
		filename2="${filename#*-}"
        	echo -e "\n---- Applying patch ${TBOLD}${filename2%%.*}${TNORMAL}:"
        	patch -Np1 -i "$srcdir/${filename}"
  	fi
  done

  cat ../x509.genkey > ./certs/x509.genkey

  # kernel config
  printf '\n'
  msg2 "KERNEL CONFIGURATION"
  local _config
  echo "---- Select configuration file:"
  echo "${TBOLD}1)${TNORMAL} Manjaro default"
  echo "${TBOLD}2)${TNORMAL} vd default"
  echo "${TBOLD}3)${TNORMAL} x570"
  echo "${TBOLD}4)${TNORMAL} x270"
  echo "${TBOLD}5)${TNORMAL} x200"
  while true ; do
  	read -p "Enter number (1-5): " _config
	  case ${_config} in
		1) cat ../config.x86_64 > ./.config && break ;;
		2) cat ../config.vd > ./.config && break ;;
		3) cat ../config.x570 > ./.config && break ;;
		4) cat ../config.x270 > ./.config && break ;;
		5) cat ../config.x200 > ./.config && break ;;
		*) echo "Please enter a number (1-5)!" && continue ;;
  	  esac
  done

  # add key
  printf '\n'
  msg2 "KERNEL KEY GENERATION"
  read -p "---- Enter the full path to the key if you have one, else enter 'n': " UCHOICE
  if [[ ${UCHOICE} != "n" ]]; then
    if [[ -f ${UCHOICE} ]]; then
      cat ${UCHOICE} > ./certs/vd54-kernel-key.pem || exit 2
    else
      echo "Path does not exist. Aborting..." ; exit 2
    fi
  else
    sed -i 's/vd54\-kernel\-key/signing\_key/' ./.config || exit 2
  fi

  if [ "${_kernelname}" != "" ]; then
    sed -i "s|CONFIG_LOCALVERSION=.*|CONFIG_LOCALVERSION=\"${_kernelname}\"|g" ./.config
    sed -i "s|CONFIG_LOCALVERSION_AUTO=.*|CONFIG_LOCALVERSION_AUTO=n|" ./.config
  fi

  # set patchlevel to 4
  sed -ri "s|^(PATCHLEVEL =).*|\1 4|" Makefile

  # set extraversion to pkgrel
  sed -ri "s|^(EXTRAVERSION =).*|\1 -${pkgrel}|" Makefile

  # don't run depmod on 'make install'. We'll do this ourselves in packaging
  sed -i '2iexit 0' scripts/depmod.sh

  # get kernel version
  make prepare
  make -s kernelrelease > version
  printf '\n'
  msg2 "Prepared %s version %s" "$pkgbase" "$(<version)"
  read -p "---- Enter 'y' for nconfig: " NCONFIG
  if [[ $NCONFIG = "y" ]] ; then make nconfig ; fi

  # rewrite configuration
  yes "" | make config >/dev/null
}

build() {
  cd "${srcdir}/linux-${pkgver}"

  # build!
  make ${MAKEFLAGS} LOCALVERSION= bzImage modules
}

package_linux54-vd() {
  pkgdesc="The ${pkgbase/linux/Linux} vd kernel and modules"
  depends=('coreutils' 'linux-firmware' 'kmod' 'mkinitcpio>=27')
  optdepends=('crda: to set the correct wireless channels of your country')
  provides=("linux=${pkgver}")

  cd "${srcdir}/linux-${pkgver}"

  KARCH=x86

  local kernver="$(<version)"
  local modulesdir="$pkgdir/usr/lib/modules/$kernver"

  mkdir -p "${pkgdir}"/{boot,usr/lib/modules}
  printf '\n'
  msg2 "Installing modules..."
  make LOCALVERSION= INSTALL_MOD_PATH="${pkgdir}/usr" modules_install

  # systemd expects to find the kernel here to allow hibernation
  # https://github.com/systemd/systemd/commit/edda44605f06a41fb86b7ab8128dcf99161d2344
  install -Dm644 "$(make -s image_name)" "$modulesdir/vmlinuz"

  # Used by mkinitcpio to name the kernel
  echo "${pkgbase}" | install -Dm644 /dev/stdin "$modulesdir/pkgbase"
  echo "${kernelbase}-${CARCH}" | install -Dm644 /dev/stdin "$modulesdir/kernelbase"

  # add kernel version
  echo "${pkgver}-${pkgrel}${_kernelname} x64" > "${pkgdir}/boot/${pkgbase}-${CARCH}.kver"

  # make room for external modules
  local _extramodules="extramodules-${kernelbase}"
  ln -s "../${_extramodules}" "$modulesdir/extramodules"

  # add real version for building modules and running depmod from hook
  echo "${kernver}" |
    install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_extramodules}/version"

  # now we call depmod...
  printf '\n'
  msg2 "Running depmod..."
  depmod -v -b "${pkgdir}/usr" -F System.map "$kernver"

  # remove build and source links
  rm $modulesdir/source
  rm $modulesdir/build

  # Fixing permissions
  printf '\n'
  msg2 "Fixing permissions..."
  chmod -Rc u=rwX,go=rX "$pkgdir"

  # add vmlinux
  #install -Dt "$modulesdir/build" -m644 vmlinux

  # add mkinitcpio preset (not strictly needed)
  install -Dm644 "$srcdir/${pkgbase}.preset" "$pkgdir/etc/mkinitcpio.d/${pkgbase}.preset"
}

package_linux54-vd-headers() {
  pkgdesc="Header files and scripts for building modules for ${pkgbase/linux/Linux} vd kernel"
  provides=("linux-headers=$pkgver")

  cd "${srcdir}/linux-${pkgver}"
  local kernver="$(<version)"
  local _builddir="${pkgdir}/usr/lib/modules/${kernver}/build"

  printf '\n'
  msg2 "Installing headers..."
  install -Dt "${_builddir}" -m644 Makefile .config Module.symvers System.map || exit 32
  install -Dt "${_builddir}/kernel" -m644 kernel/Makefile

  mkdir "${_builddir}/.tmp_versions"

  cp -t "${_builddir}" -a include scripts

  install -Dt "${_builddir}/arch/${KARCH}" -m644 "arch/${KARCH}/Makefile"
  install -Dt "${_builddir}/arch/${KARCH}/kernel" -m644 "arch/${KARCH}/kernel/asm-offsets.s"
  #install -Dt "${_builddir}/arch/${KARCH}/kernel" -m644 "arch/${KARCH}/kernel/macros.s"

  cp -t "${_builddir}/arch/${KARCH}" -a "arch/${KARCH}/include"

  # add objtool for external module building and enabled VALIDATION_STACK option
  install -Dt "${_builddir}/tools/objtool" tools/objtool/objtool

  install -Dt "${_builddir}/drivers/md" -m644 drivers/md/*.h
  install -Dt "${_builddir}/net/mac80211" -m644 net/mac80211/*.h

  # http://bugs.archlinux.org/task/13146
  install -Dt "${_builddir}/drivers/media/i2c" -m644 drivers/media/i2c/msp3400-driver.h

  # http://bugs.archlinux.org/task/20402
  install -Dt "${_builddir}/drivers/media/usb/dvb-usb" -m644 drivers/media/usb/dvb-usb/*.h
  install -Dt "${_builddir}/drivers/media/dvb-frontends" -m644 drivers/media/dvb-frontends/*.h
  install -Dt "${_builddir}/drivers/media/tuners" -m644 drivers/media/tuners/*.h

  # add xfs and shmem for aufs building
  mkdir -p "${_builddir}"/{fs/xfs,mm}

  # copy in Kconfig files
  find . -name Kconfig\* -exec install -Dm644 {} "${_builddir}/{}" \;

  # remove unneeded stuff
  printf '\n'
  msg2 "Removing unneeded files..."
  # remove unneeded architectures
  local _arch
  for _arch in "${_builddir}"/arch/*/; do
    [[ ${_arch} == */x86/ ]] && continue
    rm -r "${_arch}"
  done

  # remove files already in linux-docs package
  rm -r "${_builddir}/Documentation"

  # remove broken symlinks
  find -L "${_builddir}" -type l -printf 'Removing %P\n' -delete

  # remove loose objects"
  find "${_builddir}" -type f -name '*.o' -printf 'Removing %P\n' -delete

  # strip scripts directory
  printf '\n'
  msg2 "Stripping build tools..."
  local file
  while read -rd '' file; do
    case "$(file -bi "$file")" in
      application/x-sharedlib\;*)      # Libraries (.so)
        strip -v $STRIP_SHARED "$file" ;;
      application/x-archive\;*)        # Libraries (.a)
        strip -v $STRIP_STATIC "$file" ;;
      application/x-executable\;*)     # Binaries
        strip -v $STRIP_BINARIES "$file" ;;
      application/x-pie-executable\;*) # Relocatable binaries
        strip -v $STRIP_SHARED "$file" ;;
    esac
  done < <(find "${_builddir}" -type f -perm -u+x ! -name vmlinux -print0)

  # Fix permissions
  printf '\n'
  msg2 "Fixing permissions..."
  chmod -Rc u=rwX,go=rX "${pkgdir}"
}

