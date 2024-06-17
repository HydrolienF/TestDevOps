$ ansible all -m ping --private-key=id_rsa -u centos
[WARNING]: No python interpreters found for host emilien.raveneau.takima.cloud (tried ['python3.12',
'python3.11', 'python3.10', 'python3.9', 'python3.8', 'python3.7', '/usr/bin/python3', 'python3'])
emilien.raveneau.takima.cloud | FAILED! => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3"
    },
    "changed": false,
    "module_stderr": "Shared connection to emilien.raveneau.takima.cloud closed.\r\n",
    "module_stdout": "/bin/sh: /usr/bin/python3: No such file or directory\r\n",
    "msg": "The module failed to execute correctly, you probably need to set the interpreter.\nSee stdout/stderr for the exact error",
    "rc": 127
}


ansible all -m ping --private-key=id_rsa -u centos
[WARNING]: Unhandled error in Python interpreter discovery for host emilien.raveneau.takima.cloud:
Expecting value: line 1 column 1 (char 0)
An exception occurred during task execution. To see the full traceback, use -vvv. The error was: SyntaxError: future feature annotations is not defined
[WARNING]: Platform linux on host emilien.raveneau.takima.cloud is using the discovered Python
interpreter at /usr/bin/python3, but future installation of another Python interpreter could change the
meaning of that path. See https://docs.ansible.com/ansible-
core/2.17/reference_appendices/interpreter_discovery.html for more information.
emilien.raveneau.takima.cloud | FAILED! => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3"
    },
    "changed": false,
    "module_stderr": "Shared connection to emilien.raveneau.takima.cloud closed.\r\n",
    "module_stdout": "Traceback (most recent call last):\r\n  File \"/home/centos/.ansible/tmp/ansible-tmp-1718619611.9046173-54659-100898105726751/AnsiballZ_ping.py\", line 107, in <module>\r\n    _ansiballz_main()\r\n  File \"/home/centos/.ansible/tmp/ansible-tmp-1718619611.9046173-54659-100898105726751/AnsiballZ_ping.py\", line 99, in _ansiballz_main\r\n    invoke_module(zipped_mod, temp_path, ANSIBALLZ_PARAMS)\r\n  File \"/home/centos/.ansible/tmp/ansible-tmp-1718619611.9046173-54659-100898105726751/AnsiballZ_ping.py\", line 44, in invoke_module\r\n    from ansible.module_utils import basic\r\n  File \"<frozen importlib._bootstrap>\", line 971, in _find_and_load\r\n  File \"<frozen importlib._bootstrap>\", line 951, in _find_and_load_unlocked\r\n  File \"<frozen importlib._bootstrap>\", line 894, in _find_spec\r\n  File \"<frozen importlib._bootstrap_external>\", line 1157, in find_spec\r\n  File \"<frozen importlib._bootstrap_external>\", line 1131, in _get_spec\r\n  File \"<frozen importlib._bootstrap_external>\", line 1112, in _legacy_get_spec\r\n  File \"<frozen importlib._bootstrap>\", line 441, in spec_from_loader\r\n  File \"<frozen importlib._bootstrap_external>\", line 544, in spec_from_file_location\r\n  File \"/tmp/ansible_ping_payload_lkhg0dwd/ansible_ping_payload.zip/ansible/module_utils/basic.py\", line 5\r\nSyntaxError: future feature annotations is not defined\r\n",
    "msg": "MODULE FAILURE\nSee stdout/stderr for the exact error",
    "rc": 1
}
