# Домашнее задание к занятию «Хранение в K8s»
## Задание 1. Volume: обмен данными между контейнерами в поде

Задача

Создать Deployment приложения, состоящего из двух контейнеров, обменивающихся данными.

Шаги выполнения

- Создать Deployment приложения, состоящего из контейнеров busybox и multitool.

- Настроить busybox на запись данных каждые 5 секунд в некий файл в общей директории.

- Обеспечить возможность чтения файла контейнером multitool.

Что сдать на проверку

Манифесты:

1. containers-data-exchange.yaml

Скриншоты:

1. описание пода с контейнерами (kubectl describe pods data-exchange)

2. вывод команды чтения файла (tail -f <имя общего файла>)

<img width="1154" height="1187" alt="image" src="https://github.com/user-attachments/assets/00b23a3c-83e6-4bd8-b07e-7a31cdda0757" />
<img width="1217" height="1093" alt="image" src="https://github.com/user-attachments/assets/e4a99245-689b-438f-a98b-4b0094673c8d" />
<img width="1202" height="610" alt="image" src="https://github.com/user-attachments/assets/598bc3c1-3b54-4406-a6d6-cc31c6add3c2" />
![Uploading image.png…]()
