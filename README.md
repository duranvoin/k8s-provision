Имя роли
=========

### k8s-provision - роль для провижна кубер нод и сборки неотказоустойчивого кластера

Требования
------------

По умолчанию кластер не собирается. Для его сборки нужно переопределить переменную **k8s_provision__cluster_create** со значением **true**, во время запуска плейбука с ролью.

Переменные роли
--------------

* **k8s_provision__arch** - автоматическое определение архитектуры процессора
* **k8s_provision__containerd_version** - версия containerd
* **k8s_provision__runc_version** - версия runc
* **k8s_provision__cni_plugin_version** - версия сетевых плагинов
* **k8s_provision__crictl_version** - версия crictl
* **k8s_provision__release_version** - версия компонентов k8s
* **k8s_provision__download_dir** - путь до стандартной директории для бинарников k8s из мануала
* **k8s_provision__cidr** - подсеть для подов. По умолчанию используется сетевой плагин flannel и его подсеть.
* **k8s_provision__kernel_modules** - модули ядра 
* **k8s_provision__cluster_create** - булевая переменная для указания необходимости создания кластера. По умолчанию - false

Зависимости
------------

**Роли:**
- base-package-install

**Коллекции:**
- ansible.posix
- community.general
- kubernetes.core

Информация об авторе
------------------

Kiselev Mikhail (duranvoin)
