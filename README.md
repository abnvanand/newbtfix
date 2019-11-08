# newbtfix-4.15
Ubuntu 4.15 bluetooth source code patched with https://bugzilla.opensuse.org/attachment.cgi?id=770190

Credit goes to Takashi Iwai for the patch

Bluetooth: hci0: don't support firmware rome 0x11020000 

Should fix Ubuntu Bug https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1764645

To use

sudo apt install git build-essential dkms

git clone https://github.com/jeremyb31/newbtfix-4.15.git

sudo dkms add ./newbtfix-4.15

sudo dkms install btusb/4.0

Reboot



# For mediatek 
```bash
git clone https://github.com/abnvanand/newbtfix-4.15.git
sudo dkms add ./newbtfix-4.15
sudo dkms install btusb/4.0
reboot
sudo modprobe mt76xx


sudo systemctl enable bluetooth
sudo systemctl start bluetooth

```

```
sudo dkms remove btusb/4.0 -k $(uname -r)
```
