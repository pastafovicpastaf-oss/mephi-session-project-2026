# MEPHI Session Project 2026

Сессионный проект по курсу «Безопасность GNU/Linux».

- Номер зачётной книжки: **375042**
- ОС: **РЕД ОС 8**
- Имя хоста: **mephi-2026.domain.local**
- Репозиторий: **mephi-session-project-2026**

## Выполненные разделы

| Раздел | Выполненная настройка | Артефакт |
|---|---|---|
| 1.1 | DHCP на интерфейсе `enp0s3` | `history.out`, `ping.out` |
| 1.2 | Имя хоста `mephi-2026.domain.local` | `history.out` |
| 1.3 | Проверка связи с `8.8.8.8` | `ping.out` |
| 2.1 | Обновление РЕД ОС | `dnf.out` |
| 2.2 | Установка nginx и capabilities utilities | `dnf.out` |
| 2.3 | Скачивание и установка RPM tcpdump | `dnf.out`, `history.out` |
| 3 | Раздел ext4 с меткой `MEPHI_WEB` и монтирование `/mephi-web` | `fstab`, `stat.out` |
| 4.1 | Запуск nginx и автозапуск | `journalctl.out` |
| 4.2 | Журнал nginx текущей загрузки | `journalctl.out` |
| 5.1 | Пользователи, группы, set-GID и ACL проекта | `passwd`, `group`, `stat.out` |
| 5.2 | Capabilities для tcpdump | `getcap.out`, `tcpdump-user1.out` |
| 5.3 | SELinux Enforcing и контекст web-директории | `getenforce.out`, `stat.out` |
| 6.1 | Запрет локального входа группе curators через PAM | `access.conf`, `pam-login` |
| 6.2 | Срок пароля 90 дней и минимальная длина 12 символов | `shadow`, `pwquality.conf` |
| 7 | Страница nginx с номером студента | `curl.out`, `mephi-screenshot.png` |
| 8 | Публикация результатов | GitHub |

## Пользователи

| Пользователь | UID | Группа |
|---|---:|---|
| `user1` | 5501 | `devsite` |
| `user2` | 5502 | `devsite` |
| `user3` | 5503 | `devsite` |
| `curator1` | 5504 | `curators` |
| `curator2` | 5505 | `curators` |

Группа `curators` создана с GID `4444`.

## Web-страница

nginx отдаёт страницу из нестандартной директории `/mephi-web`.

Результат:

```text
Hello from Student: 375042