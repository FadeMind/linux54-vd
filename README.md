## Kernel 5.4 for Manjaro
#### Features: 
- based on Manjaro's default linux54 PKGBUILD
- graysky's CPU optimisations
- several 5.5 backports from H. Hoffstätte's repo
- Steam's futex/fsync patches from SirLucjan's repo
- Arch patches from SirLucjan's repo
- Clear Linux patches
- amdgpu patches
- add NVMe sensor reading to hwmon (`sensors`) by G. Röck
- tuned VM settings
- tuned CFS settings for lower latency
- kernel module compression optimisations
- kernel config selection and key generation dialog in PKGBUILD
- includes Manjaro's default linux54 as well as a few custom ones
- several fixes to Manjaro's original PKGBUILD by bringing it more in line with Arch
- apply patches by looping through an array instead of one-by-one
- beautification of build process output in PKGBUILD

#### Credits:
- Holger Hoffstätte
- SirLucjan (Piotr Gorski)
- Günter Röck
- Manjaro
- Arch
- StackOverflow

