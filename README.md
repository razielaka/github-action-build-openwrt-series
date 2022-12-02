# Github Action Build OpenWRT Series
## what is this
This is a tool related to compiling OpenWRT using Github Action, you can compile the latest OpenWRT or LEDE, or compile a single package.
## how to use
**Compile a single package**
1. Give a Star to show support
2. Fork the current warehouse
3. Add the config of your device in the device folder, which contains `x86_64` and `Newifi3 D2` configurations by default
4. Modify .github/workflows/build-openwrt-package.yml
   - Change `SDK_URL` to the SDK download address of your OpenWRT version, you can find your OpenWRT version SDK in https://downloads.openwrt.org/releases/. Such as `https://downloads.openwrt.org/releases/22.03.2/targets/x86/64/openwrt-sdk-22.03.2-x86-64_gcc-11.2.0_musl.Linux-x86_64.tar.xz`
   - `CONFIG_FILE` is changed to your device's configuration file. Such as `device/x86-64.config`
   - `PACKAGE_REPO` is changed to your package warehouse address. Such as `https://github.com/yichya/luci-app-xray.git`
   - `PACKAGE_NAME` is changed to your package name, which can be customized. Such as `luci-app-xray`
   - `PACKAGE_BRANCH` is changed to the branch of your package. such as `master`
5. Select the Action on the warehouse page, select your workflows, such as `Build OpenWRT Package`, select `Run workflow`, click `Run workflow` to run the compilation.
6. After the compilation is successful, you can download the bin compressed package on the Workflow page of the Action.
