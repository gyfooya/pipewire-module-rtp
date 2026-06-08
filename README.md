# pipewire-module-rtp
UDP network audio stream

sudo pacman -S pipewire wireplumber pipewire-pulse pavucontrol
systemctl --user status or enable --now pipewire pipewire-pulse wireplumber
pactl info (pipewire as server is fine)


behind the scene without script :
# Sender setup (PC A → sends audio)
- pw-cli load-module libpipewire-module-rtp-sink

# Receiver setup (PC B ← receives audio)
- pw-cli load-module libpipewire-module-rtp-source
