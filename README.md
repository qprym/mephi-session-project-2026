# MEPHI Session Project 2026

## Студент
- Номер зачётки: M265964

## Выполненные разделы

| Раздел | Что сделано | Артефакт |
|--------|-------------|----------|
| 1 | Установка РЕД ОС 8, hostname mephi-2026.domain.local, DHCP | ping.out |
| 2 | dnf update, nginx, libcap-ng-utils, локальный tcpdump.rpm | dnf.out |
| 3 | /dev/sdb1 → ext4 LABEL=MEPHI_WEB → /mephi-web (fstab по LABEL) | fstab, stat.out |
| 4 | nginx запущен, включён в автозагрузку | journalctl.out |
| 5.1 | /data/mephi-2026, ACL: user1-3 rw, curators r, other ---; проверены запись user2, чтение и отказ в записи curator1, отказ постороннему пользователю | stat.out, getfacl_dir.out, getfacl_file.out, acl_test.out |
| 5.2 | tcpdump через capabilities, без set-UID | getcap.out |
| 5.3 | SELinux Enforcing, httpd_sys_content_t на /mephi-web | getenforce.out, stat.out |
| 6 | access.conf, PASS_MAX_DAYS 90, minlen 12; пароль короче 12 символов отклонён, curator1 отказано во входе через текстовую консоль | access.conf, login.defs, pwquality.conf, password-minlen-check.png, curator-console-denied.png |
| 7 | index.html "Hello from Student: M265964" | curl.out, mephi-screenshot.png |
