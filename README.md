# TP-Link-Archer-T3U

      git clone https://github.com/cilynx/rtl88x2bu.git
      cd rtl88x2bu
      # VER=$(sed -n 's/\PACKAGE_VERSION="\(.*\)"//p' dkms.conf)
      # check the dkms.conf in repo
      VER="5.8.7.1"
      sudo rsync -rvhP ./ /usr/src/rtl88x2bu-${VER}
      sudo dkms add -m rtl88x2bu -v ${VER}
      sudo dkms build -m rtl88x2bu -v ${VER}
      sudo dkms install -m rtl88x2bu -v ${VER}
      sudo modprobe 88x2bu
