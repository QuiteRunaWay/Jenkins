# Домашнее задание к занятию "09.04 Jenkins"

## Подготовка к выполнению

1. Создать 2 VM: для jenkins-master и jenkins-agent.
2. Установить jenkins при помощи playbook'a.

Установлен:

![image](https://user-images.githubusercontent.com/92969676/172392815-ec5d729a-c4d1-46e4-92ea-abfeb3c2e6c5.png)

4. Запустить и проверить работоспособность.
5. Сделать первоначальную настройку.

Всё сделано:

![image](https://user-images.githubusercontent.com/92969676/172393315-710443b0-0cea-498f-bef8-aa1f95353f27.png)


## Основная часть

1. Сделать Freestyle Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.

Успешно:

![image](https://user-images.githubusercontent.com/92969676/172453249-34fd5205-2475-4aa3-97e8-ad83a2219153.png)

![image](https://user-images.githubusercontent.com/92969676/172453106-a2a26af7-a3a4-471c-948a-b8169cee536e.png)

3. Сделать Declarative Pipeline Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.

Успешно:

![image](https://user-images.githubusercontent.com/92969676/172458369-4de6988b-c84b-4cf0-aed7-5631877fe0e0.png)

![image](https://user-images.githubusercontent.com/92969676/172458311-614c3ec4-907f-48b2-b8dc-4cf34e1c3cd8.png)


5. Перенести Declarative Pipeline в репозиторий в файл `Jenkinsfile`.

Сделано

6. Создать Multibranch Pipeline на запуск `Jenkinsfile` из репозитория.

![image](https://user-images.githubusercontent.com/92969676/172461901-bf97ab2c-32da-44a4-8ffc-188f9d3666b7.png)

![image](https://user-images.githubusercontent.com/92969676/172462015-b5467911-c1da-4a46-a910-701c40b50469.png)

![image](https://user-images.githubusercontent.com/92969676/172462264-7b60b095-3cd7-4caf-920a-f72fa9d58ac3.png)


8. Создать Scripted Pipeline, наполнить его скриптом из [pipeline](./pipeline).
Сделано.

10. Внести необходимые изменения, чтобы Pipeline запускал `ansible-playbook` без флагов `--check --diff`, если не установлен параметр при запуске джобы (prod_run = True), по умолчанию параметр имеет значение False и запускает прогон с флагами `--check --diff`.

Сделано:

Для корректного отрабатывания скрипта понадобилось ```63``` попытки. 

![image](https://user-images.githubusercontent.com/92969676/172842315-c51fa415-2ed8-43fa-bd79-9ab067688478.png)

![image](https://user-images.githubusercontent.com/92969676/172842531-785312a1-0b8e-4039-bdee-f99572e97b70.png)

11. Проверить работоспособность, исправить ошибки, исправленный Pipeline вложить в репозиторий в файл `ScriptedJenkinsfile`.

Выложил.

12. Отправить ссылку на репозиторий с ролью и Declarative Pipeline и Scripted Pipeline.

Файлы приложены в текущем репозитории. Ссылка на роль, на которой проводилось тестирование 'molecule test': https://github.com/QuiteRunaWay/Jjenkins (репозиторий сделал отдельный, чтобы просто было удобно работать по данному ДЗ).

