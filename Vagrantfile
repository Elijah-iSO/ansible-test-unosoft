Vagrant.configure("2") do |config|
  config.vm.box = "cloud-image/ubuntu-24.04"
  
  config.vm.provider "libvirt" do |libvirt|
    libvirt.memory = "4096"
    libvirt.cpus = 2
  end

  # Пробрасываем порты для теста ldap с осн хоста
  config.vm.network "forwarded_port", guest: 389, host: 3899

  # Сразу после поднятия ВМ запускаем ansible
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "openldap.yml"
    ansible.compatibility_mode = "2.0"
  end

end
