#SELinux
Задание 1

Запустить nginx на нестандартном порту 3-мя разными способами

Необходимо запустить nginx на нестандартном 4881 порту 3-мя разными способами.
SELinux в целях безопасности блокирует запуск nginx т.к. используется не стандартный порт.
![nginx error](nginx_error.png)
- 1 способ
  при помощи переключателей setsebool включить ![nis_enabled](setsebool.png)
- 2 способ
  при помощм добавления нестандартного порта в имеющийся тип ![http_port_t](semanage.png)
- 3 способ
  при помощи формирования и установки модуля ![SELinux](semodule.png)

Задание 2

Обеспечение работоспособности приложения при включенном SELinux на примере dns

При изменении dns зоны клиентом происходит ![ошибка](client_fail.png), из за неправильного контекста безопастности каталога с размещаемой зоной на ![сервере](ns01.png). После изменения контекста запись зоны проходит ![успешно](client_ok.png)
