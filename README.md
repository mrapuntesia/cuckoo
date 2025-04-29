# cuckoo

(cuckoo-test) thisjesusalan@thisjesusalan:/opt$ VBoxManage unregistervm win7x64base --delete
0%...10%...20%...30%...40%...50%...60%...70%...80%...90%...100%
(cuckoo-test) thisjesusalan@thisjesusalan:/opt$ rm -rf /home/thisjesusalan/.vmcloak/vms/win7x64base
(cuckoo-test) thisjesusalan@thisjesusalan:/opt$ vmcloak init --verbose --win7x64 win7x64base --cpus 2 --ramsize 2048
/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/OpenSSL/crypto.py:14: CryptographyDeprecationWarning: Python 2 is no longer supported by the Python core team. Support for it is now deprecated in cryptography, and will be removed in the next release.
  from cryptography import utils, x509
0%...10%...20%...30%...40%...50%...60%...70%...80%...90%...100%
INFO:vmcloak:Starting the Virtual Machine u'win7x64base' to install Windows.
VBoxManage: error: VT-x is not available (VERR_VMX_NO_VMX)
VBoxManage: error: Details: code NS_ERROR_FAILURE (0x80004005), component ConsoleWrap, interface IConsole
ERROR:vmcloak.vm:[-] Error running command: Command '['/usr/bin/VBoxManage', 'startvm', u'win7x64base', '--type', 'headless']' returned non-zero exit status 1
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
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/vmcloak/main.py", line 273, in init
    m.start_vm(visible=vm_visible)
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/vmcloak/vm.py", line 201, in start_vm
    type_="gui" if visible else "headless")
  File "/home/thisjesusalan/.virtualenvs/cuckoo-test/local/lib/python2.7/site-packages/vmcloak/vm.py", line 41, in _call
    raise CommandError
vmcloak.exceptions.CommandError
