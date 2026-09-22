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


### Решение
<img width="1154" height="1187" alt="image" src="https://github.com/user-attachments/assets/00b23a3c-83e6-4bd8-b07e-7a31cdda0757" />
<img width="1217" height="1093" alt="image" src="https://github.com/user-attachments/assets/e4a99245-689b-438f-a98b-4b0094673c8d" />
<img width="1202" height="610" alt="image" src="https://github.com/user-attachments/assets/598bc3c1-3b54-4406-a6d6-cc31c6add3c2" />
<img width="917" height="445" alt="image" src="https://github.com/user-attachments/assets/c3193926-c305-4ea5-ad4b-20b174909cb2" />


## Задание 2. PV, PVC

Задача

Создать Deployment приложения, использующего локальный PV, созданный вручную.

Шаги выполнения

- Создать Deployment приложения, состоящего из контейнеров busybox и multitool, использующего созданный ранее PVC

- Создать PV и PVC для подключения папки на локальной ноде, которая будет использована в поде.

- Продемонстрировать, что контейнер multitool может читать данные из файла в смонтированной директории, в который busybox записывает данные каждые 5 секунд.

- Удалить Deployment и PVC. Продемонстрировать, что после этого произошло с PV. Пояснить, почему. (Используйте команду kubectl describe pv).

- Продемонстрировать, что файл сохранился на локальном диске ноды. Удалить PV. Продемонстрировать, что произошло с файлом после удаления PV. Пояснить, почему.

Что сдать на проверку

Манифесты:

1. pv-pvc.yaml

Скриншоты:

1. каждый шаг выполнения задания, начиная с шага 2.


### Решение
<img width="1093" height="604" alt="image" src="https://github.com/user-attachments/assets/103b65a7-ac5d-4378-a6f5-3c19792805e5" />
<img width="1037" height="542" alt="image" src="https://github.com/user-attachments/assets/520ad7ed-8e3a-48ab-a77a-d5a096f9073d" />
<img width="751" height="583" alt="image" src="https://github.com/user-attachments/assets/ad6e0757-dd1f-4983-a3b4-c672cb490787" />


## Задание 3. StorageClass

Задача

Создать Deployment приложения, использующего PVC, созданный на основе StorageClass.

Шаги выполнения

- Создать Deployment приложения, состоящего из контейнеров busybox и multitool, использующего созданный ранее PVC.

- Создать SC и PVC для подключения папки на локальной ноде, которая будет использована в поде.

- Продемонстрировать, что контейнер multitool может читать данные из файла в смонтированной директории, в который busybox записывает данные каждые 5 секунд.

Что сдать на проверку

Манифесты:

1. sc.yaml

Скриншоты:

1. каждый шаг выполнения задания, начиная с шага 2

2. Шаблоны манифестов с учебными комментариями


### Решение
<img width="894" height="564" alt="image" src="https://github.com/user-attachments/assets/e2c29b56-c478-4842-be70-13b69478caf3" />
<img width="996" height="468" alt="image" src="https://github.com/user-attachments/assets/8ae1673d-193f-49ac-bb35-3b0b21b9b741" />
<img width="1068" height="419" alt="image" src="https://github.com/user-attachments/assets/da55853d-5d2e-4fbb-8c86-8119eceec5c9" />
