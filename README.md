# ContainerizationSemTwo

### Контейнирезация семинар 2

 ## Команда для создания новой контрольной группы

``cgcreate -a $USER -g memory:mytestgroup -g cpu:mytestgroup`` 

 ``$USER`` // Текущий пользователь  
 ``-g memory:mytestgroup`` // ограничение на использование памяти  
 ``-g cpu:mytestgroup`` // ограничения на использование процессора  

 ## Каманда для проверки создания  контрольной группы 

 ``ls /sys/fs/cgroup/mytestgroup/``

![image](https://github.com/ScherbakovM/ContainerizationSemTwo/assets/109952823/52c0ad6c-b4c7-4112-8ec7-1998bd08f88e)

### Создаём новый контейнер 

``lxc-create -n test123 -t ubuntu ``

Если команда не запускается возможнго потребуется установить пакет с зависимостями для lxc 

``apt-get install lxc-templates``

![image](https://github.com/ScherbakovM/ContainerizationSemTwo/assets/109952823/fd8e95d7-429a-422e-94af-c8cc0c6f8bc4)

### Дожидаёмся сообщения об успешной устанвки 

![image](https://github.com/ScherbakovM/ContainerizationSemTwo/assets/109952823/85fb3581-65b6-408f-80f7-37e6012c3555)

### Переходим к запуску контейнера
 
``lxc-start -n test123`` // запуск контейнера  
``lxc-attach -n test123`` // вход в контейнер  

