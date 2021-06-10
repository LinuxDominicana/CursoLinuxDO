Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  
  config.vm.provision "shell", inline: "sudo echo linuxdo | passwd root --stdin"
  config.vm.provision "shell", inline: "adduser pinguino"
  config.vm.provision "shell", inline: "sudo echo opensaturday | passwd pinguino --stdin"
  config.vm.provision "shell", inline: "echo LC_CTYPE=en_US.UTF-8 >>  /etc/environment  "
  config.vm.provision "shell", inline: "
  echo '
  #Nuestros contactos 
  #Instagram https://www.instagram.com/linuxdominicana
  #Twitter https://twitter.com/linuxdominicana
  #Canal de youtube https://www.youtube.com/c/linuxdominicana 
  #Facebook Opensaturday https://www.facebook.com/opensaturday
  #Facebook Grupo https://www.facebook.com/groups/LinuxDo
  #Github https://github.com/LinuxDominicana/' > /etc/motd"
  
  config.vm.define :linuxdo do |linuxdo|
  linuxdo.vm.box = "almalinux/8"
  linuxdo.vm.hostname = "cursolinux.local"
  linuxdo.vm.network :private_network, ip: "192.168.56.150"
  linuxdo.vm.provider :virtualbox do |vb|
  vb.memory = 2048
  vb.cpus = 1
  vb.name = "Almalinux-LinuxDO"
  end
  end
  end

