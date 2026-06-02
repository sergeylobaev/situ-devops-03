# situ-devops-03 Лаб 3.

Плейбук устанавливает на хосты пакет nmap и сканирует хосты из targets.txt на доступность порта 80

Запуск плейбука
```
ansible-playbook -i inventory playbook.yml 
```

Пример вывода результата
```
ok: [server2] => (item={'changed': False, 'stdout': 'Starting Nmap 7.94SVN ( https://nmap.org ) at 2026-06-01 16:20 UTC\nNmap scan report for epos.permkrai.ru (212.33.224.16)\nHost is up (0.019s latency).\nrDNS record for 212.33.224.16: 212.33.224.16.static-business.perm.ertelecom.ru\n\nPORT   STATE SERVICE\n80/tcp open  http\n\nNmap done: 1 IP address (1 host up) scanned in 0.20 seconds', 'stderr': '', 'rc': 0, 'cmd': ['nmap', '-p', '80', 'epos.permkrai.ru'], 'start': '2026-06-01 16:20:38.889302', 'end': '2026-06-01 16:20:39.099692', 'delta': '0:00:00.210390', 'msg': '', 'invocation': {'module_args': {'_raw_params': 'nmap -p 80 epos.permkrai.ru', '_uses_shell': False, 'expand_argument_vars': True, 'stdin_add_newline': True, 'strip_empty_ends': True, 'cmd': None, 'argv': None, 'chdir': None, 'executable': None, 'creates': None, 'removes': None, 'stdin': None}}, 'stdout_lines': ['Starting Nmap 7.94SVN ( https://nmap.org ) at 2026-06-01 16:20 UTC', 'Nmap scan report for epos.permkrai.ru (212.33.224.16)', 'Host is up (0.019s latency).', 'rDNS record for 212.33.224.16: 212.33.224.16.static-business.perm.ertelecom.ru', '', 'PORT   STATE SERVICE', '80/tcp open  http', '', 'Nmap done: 1 IP address (1 host up) scanned in 0.20 seconds'], 'stderr_lines': [], 'failed': False, 'item': 'epos.permkrai.ru', 'ansible_loop_var': 'item'}) => {
    "msg": "Target: epos.permkrai.ru\nStarting Nmap 7.94SVN ( https://nmap.org ) at 2026-06-01 16:20 UTC\nNmap scan report for epos.permkrai.ru (212.33.224.16)\nHost is up (0.019s latency).\nrDNS record for 212.33.224.16: 212.33.224.16.static-business.perm.ertelecom.ru\n\nPORT   STATE SERVICE\n80/tcp open  http\n\nNmap done: 1 IP address (1 host up) scanned in 0.20 seconds\n"
}
```
