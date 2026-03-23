# Ansible Test - OpenLDAP Setup

Автоматическая установка и настройка OpenLDAP сервера с использованием Vagrant и Ansible.

## 📋 Зависимости 

- **Vagrant**
- **libvirt**
- **Ansible**

## 🚀 Быстрый старт

### 1. Клонирование репозитория

```bash
git clone https://github.com/Elijah-iSO/ansible-test-unosoft.git
cd ansible-test-unosoft
```

### 2. Запуск (создание ВМ с Ubuntu LTS и последующий запуск Ansible скрипта)

```bash
vagrant up
```

### 3. Проверка

```bash
ldapsearch -x -H ldap://localhost:3899 \
  -b "dc=example,dc=local" \
  -D "cn=admin,dc=example,dc=local" \
  -w admin123 -LLL
```
