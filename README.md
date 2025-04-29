# cuckoo

VBoxManage unregistervm win7x64base --delete
rm -rf /home/thisjesusalan/.vmcloak/vms/win7x64base


vmcloak init --verbose --win7x64 win7x64base --cpus 2 --ramsize 2048 --iso-mount /mnt/win7
