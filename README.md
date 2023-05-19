
# Домашнее задание к занятию 2. «Применение принципов IaaC в работе с виртуальными машинами»

## Как сдавать задания

Обязательны к выполнению задачи без звёздочки. Их нужно выполнить, чтобы получить зачёт и диплом о профессиональной переподготовке.

Задачи со звёздочкой (*) — дополнительные задачи и/или задачи повышенной сложности. Их выполнять не обязательно, но они помогут вам глубже понять тему.

Домашнее задание выполните в файле readme.md в GitHub-репозитории. В личном кабинете отправьте на проверку ссылку на .md-файл в вашем репозитории.

Любые вопросы по решению задач задавайте в чате учебной группы.

---


## Важно

Перед отправкой работы на проверку удаляйте неиспользуемые ресурсы.
Это нужно, чтобы не расходовать средства, полученные в результате использования промокода.

Подробные рекомендации [здесь](https://github.com/netology-code/virt-homeworks/blob/virt-11/r/README.md).

---

## Задача 1

- Опишите основные преимущества применения на практике IaaC-паттернов.

```
На мой взгляд - автоматизация процесса развертывания инфраструктуры.
Не важно в облаке это делается или частной системе виртуализации.
А это нам дает стандартизацию, повторяемость, лучшую документацию,
возможность быстро вносить изменения, высокую сокрость развертывания и уменьшение затрат,
как временных так и на персонал.
```
- Какой из принципов IaaC является основополагающим?

```
Основная идея IaaC подхода это — описывать инфраструктуру кодом,
переиспользуя практики из разработки ПО.
```


## Задача 2

- Чем Ansible выгодно отличается от других систем управление конфигурациями?
```
Простота развертывания, нет необходимости устанавливать агенты 
(все делается через ssh или winrm)  и достаточно развитое коммунити.
```
- Какой, на ваш взгляд, метод работы систем конфигурации более надёжный — push или pull?
```
push - я за централизацию особенно в большой инфраструктуре.
```
## Задача 3

Установите на личный компьютер:

- [VirtualBox](https://www.virtualbox.org/),
- [Vagrant](https://github.com/netology-code/devops-materials),
- [Terraform](https://github.com/netology-code/devops-materials/blob/master/README.md),
- Ansible.

*Приложите вывод команд установленных версий каждой из программ, оформленный в Markdown.*
```
yaha@yahawork:~$ vboxmanage --version
6.1.38_Ubuntur153438
yaha@yahawork:~$ 
yaha@yahawork:~$ vagrant --version
Vagrant 2.2.19
yaha@yahawork:~$
yaha@yahawork:~$ terraform --version
Terraform v1.4.6
on linux_386
yaha@yahawork:~$
yaha@yahawork:~$ ansible --version
ansible 2.10.8
  config file = None
  configured module search path = ['/home/yaha/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python3/dist-packages/ansible
  executable location = /usr/bin/ansible
  python version = 3.10.6 (main, Mar 10 2023, 10:55:28) [GCC 11.3.0]
yaha@yahawork:~$

```


## Задача 4 

Воспроизведите практическую часть лекции самостоятельно.

- Создайте виртуальную машину.
- Зайдите внутрь ВМ, убедитесь, что Docker установлен с помощью команды
```
docker ps,
```

```
yaha@yahawork:~/new$ vagrant ssh
Welcome to Ubuntu 20.04.6 LTS (GNU/Linux 5.4.0-144-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

 System information disabled due to load higher than 1.0


This system is built by the Bento project by Chef Software
More information can be found at https://github.com/chef/bento
Last login: Fri May 19 09:47:35 2023 from 10.0.2.2
vagrant@server1:~$ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
vagrant@server1:~$ 
```

Vagrantfile из лекции и код ansible находятся в [папке](https://github.com/netology-code/virt-homeworks/tree/virt-11/05-virt-02-iaac/src).

Примечание. Если Vagrant выдаёт ошибку:
```
URL: ["https://vagrantcloud.com/bento/ubuntu-20.04"]     
Error: The requested URL returned error: 404:
```

выполните следующие действия:

1. Скачайте с [сайта](https://app.vagrantup.com/bento/boxes/ubuntu-20.04) файл-образ "bento/ubuntu-20.04".
2. Добавьте его в список образов Vagrant: "vagrant box add bento/ubuntu-20.04 <путь к файлу>".

```
l2tp vpn через vpngate.net решил проблемы с доступом.


