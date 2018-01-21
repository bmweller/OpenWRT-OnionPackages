# OpenWRT-Packages

Onion Packages for OpenWRT/LEDE firmware. Meant for the Onion Omega2 & Omega2+

duplicates from https://git.lede-project.org/feed/packages.git;
feeds/packages/utils/avrdude
feeds/packages/utils/bluez
feeds/packages/utils/i2c-tools
feeds/packages/libs/libwebsockets
feeds/packages/sound/pulseaudio

./scripts/feeds install -p utils avrdude
./scripts/feeds install -p onion bluez
./scripts/feeds install i2c-tools -p utils
./scripts/feeds install -p libs libwebsockets
#./scripts/feeds install -p sound pulseaudio
./scripts/feeds install -p onion shellinabox
