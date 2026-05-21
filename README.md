# Installation

## Install Dependencies

### Debian/Ubuntu/Kali-based systems

```bash
sudo apt install build-essential git libwebsockets-dev pkg-config \
zlib1g-dev libnl-3-dev libnl-genl-3-dev libcap-dev libpcap-dev \
libnm-dev libdw-dev libsqlite3-dev libsensors-dev libusb-1.0-0-dev \
libubertooth-dev libbtbb-dev libmosquitto-dev librtlsdr-dev
```

### Fedora-based systems:

```bash
sudo dnf install gcc gcc-c++ zlib-devel sqlite3 sqlite-devel openssl-devel \
libwebsockets libwebsockets-devel libpcap libpcap-devel libusb1 libusb1-devel \
rtl-sdr rtl-sdr-devel mosquitto mosquitto-devel lm_sensors lm_sensors-devel \
libnl3-devel NetworkManager-libnm-devel
```

## Clone the Repository

```bash
git clone https://github.com/itsmelsec/kismet_nethunter.git
cd kismet_nethunter
```

## Build and Install

```bash
./configure
make version
make -j$(nproc)
sudo make install
```

## Usage with Nexmon

```bash
kismet -c wlan0:nexmon=true
```

Replace wlan0 with your WiFi interface name if different.
