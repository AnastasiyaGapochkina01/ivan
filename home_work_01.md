#### Пользователи и права доступа
1) Добавить в систему пользователей linus и katana (у пользователей должны быть домашние директории с правильными правами и заданы пароли)
2) Создать текстовый файл в директории /opt.
3) Установить владельцем и группой владельцев пользователя linus
4) Запретить всем остальным доступ к файлу и проверить что доступ пропал.
5) Добавить группе право читать файл, добавить пользователя katana в группу linus и проверить доступ.
Создать группы develop и sales, создать пользователей coder1, coder2, manager1, manager2 и добавить их в группы (coder1, coder2 в develop; manager1, manager2 в sales).
6) Создать папки /opt/stall, /opt/stall/code, /opt/stall/orders
7) Дать все права на /opt/stall группам develop и sales
8) Дать все права на /opt/stall/code группе develop
9) Дать все права на /opt/stall/orders группе sales
10) Создать пользователя director и дать ему все права на /opt/stall (включая поддиректории orders и code)
11) Проверить выданные доступы (посоздавать/почитать/поредактировать) папки и файлы

#### Файловые системы
1) Подключить к ВМ дополнительный диск, размером 2G
2) Запустить ВМ, командой lsblk увидеть, что в системе виден добавленный диск
3) Командой df -Th проверить, что он не смонтировался автоматически
4) Создать на диске файловую систему командой mkfs.ext4 /dev/$disk_name
5) Выполнить blkid и найти UUID нового диска
6) Создать папку /opt/new_disk
7) Сделать запись в /etc/fstab, которая примонтирует /dev/$disk_name в папку /opt/new_disk
8) Проверить findmnt --verify
9) Если не предыдущем шаге нет ошибок, то сделать mount -a и проверить с помощью df -Th что диск смонтировался
10) Положить в /opt/new_disk текстовый файл с таким содержимым
  Парадидл — это основной рудимент, который барабанщик должен уметь исполнять.
11) Отмонтировать /dev/$disk_name (команда umount /dev/$disk_name)
12) Создать папку /opt/paradidle, смонтировать диск туда руками (команда mount /dev/$disk_name /opt/paradidle), проверить, что файл из п.11 на месте и не изменился
13) Отмонтировать /dev/$disk_name
