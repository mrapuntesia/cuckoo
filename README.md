# cuckoo

(cuckoo-test) thisjesusalan@thisjesusalan:/opt$ vmcloak init --verbose --win7x64 win7x64base --cpus 2 --ramsize 2048
/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/OpenSSL/crypto.py:14: CryptographyDeprecationWarning: Python 2 is no longer supported by the Python core team. Support for it is now deprecated in cryptography, and will be removed in the next release.
  from cryptography import utils, x509
ERROR:vmcloak:Please specify --iso-mount to a directory containing the mounted Windows Installer ISO image.
INFO:vmcloak:Refer to the documentation on mounting an .iso image.
(cuckoo-test) thisjesusalan@thisjesusalan:/opt$ vmcloak init --verbose --win7x64 win7x64base --cpus 2 --ramsize 2048 --iso-mount /mnt/win7
/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/OpenSSL/crypto.py:14: CryptographyDeprecationWarning: Python 2 is no longer supported by the Python core team. Support for it is now deprecated in cryptography, and will be removed in the next release.
  from cryptography import utils, x509
ERROR:vmcloak:Please specify --iso-mount to a directory containing the mounted Windows Installer ISO image.
INFO:vmcloak:Refer to the documentation on mounting an .iso image.
(cuckoo-test) thisjesusalan@thisjesusalan:/opt$ sudo mount -o ro,loop es_windows_7_professional_with_sp1_x64_dvd_u_676947.iso /mnt/win7
[sudo] contraseña para thisjesusalan: 
(cuckoo-test) thisjesusalan@thisjesusalan:/opt$ vmcloak init --verbose --win7x64 win7x64base --cpus 2 --ramsize 2048 --iso-mount /mnt/win7
/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/OpenSSL/crypto.py:14: CryptographyDeprecationWarning: Python 2 is no longer supported by the Python core team. Support for it is now deprecated in cryptography, and will be removed in the next release.
  from cryptography import utils, x509
VBoxManage: error: Machine settings file '/home/thisjesusalan/.vmcloak/vms/win7x64base/win7x64base.vbox' already exists
VBoxManage: error: Details: code VBOX_E_FILE_ERROR (0x80bb0004), component MachineWrap, interface IMachine, callee nsISupports
VBoxManage: error: Context: "CreateMachine(bstrSettingsFile.raw(), bstrName.raw(), ComSafeArrayAsInParam(groups), bstrOsTypeId.raw(), createFlags.raw(), machine.asOutParam())" at line 274 of file VBoxManageMisc.cpp
ERROR:vmcloak.vm:[-] Error running command: Command '['/usr/bin/VBoxManage', 'createvm', '--register', '--name', 'win7x64base', '--basefolder', '/home/thisjesusalan/.vmcloak/vms']' returned non-zero exit status 1
Traceback (most recent call last):
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/bin/vmcloak", line 8, in <module>
    sys.exit(main())
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/click/core.py", line 716, in __call__
    return self.main(*args, **kwargs)
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/click/core.py", line 696, in main
    rv = self.invoke(ctx)
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/click/core.py", line 1060, in invoke
    return _process_result(sub_ctx.command.invoke(sub_ctx))
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/click/core.py", line 889, in invoke
    return ctx.invoke(self.callback, **ctx.params)
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/click/core.py", line 534, in invoke
    return callback(*args, **kwargs)
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/vmcloak/main.py", line 258, in init
    m.create_vm()
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/vmcloak/vm.py", line 75, in create_vm
    basefolder=vms_path, register=True)
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/vmcloak/vm.py", line 41, in _call
    raise CommandError
vmcloak.exceptions.CommandError
(cuckoo-test) thisjesusalan@thisjesusalan:/opt$ vmcloak init --verbose --win7x64 win7x64base --cpus 2 --ramsize 2048
/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/OpenSSL/crypto.py:14: CryptographyDeprecationWarning: Python 2 is no longer supported by the Python core team. Support for it is now deprecated in cryptography, and will be removed in the next release.
  from cryptography import utils, x509
VBoxManage: error: Machine settings file '/home/thisjesusalan/.vmcloak/vms/win7x64base/win7x64base.vbox' already exists
VBoxManage: error: Details: code VBOX_E_FILE_ERROR (0x80bb0004), component MachineWrap, interface IMachine, callee nsISupports
VBoxManage: error: Context: "CreateMachine(bstrSettingsFile.raw(), bstrName.raw(), ComSafeArrayAsInParam(groups), bstrOsTypeId.raw(), createFlags.raw(), machine.asOutParam())" at line 274 of file VBoxManageMisc.cpp
ERROR:vmcloak.vm:[-] Error running command: Command '['/usr/bin/VBoxManage', 'createvm', '--register', '--name', 'win7x64base', '--basefolder', '/home/thisjesusalan/.vmcloak/vms']' returned non-zero exit status 1
Traceback (most recent call last):
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/bin/vmcloak", line 8, in <module>
    sys.exit(main())
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/click/core.py", line 716, in __call__
    return self.main(*args, **kwargs)
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/click/core.py", line 696, in main
    rv = self.invoke(ctx)
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/click/core.py", line 1060, in invoke
    return _process_result(sub_ctx.command.invoke(sub_ctx))
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/click/core.py", line 889, in invoke
    return ctx.invoke(self.callback, **ctx.params)
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/click/core.py", line 534, in invoke
    return callback(*args, **kwargs)
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/vmcloak/main.py", line 258, in init
    m.create_vm()
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/vmcloak/vm.py", line 75, in create_vm
    basefolder=vms_path, register=True)
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/vmcloak/vm.py", line 41, in _call
    raise CommandError
vmcloak.exceptions.CommandError
(cuckoo-test) thisjesusalan@thisjesusalan:/opt$ 
