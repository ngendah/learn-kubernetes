# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
 
  config.vm.define :master, primary:true do |master| 
    master.box = "fedora/28-cloud-base"
    master.hostname = "k8s-master"
    master.provider :libvirt do |libvirt, override|
      libvirt.memory = 2048
      libvirt.nested = true
    end
    master.provision "shell", inline: <<-SHELL
      dnf install -y ansible
    SHELL
    master.provision :ansible do |ansible|
      ansible.playbook = "master.yml"
    end
  end

  config.vm.define :minion do |minion| 
    minion.box = "fedora/28-cloud-base"
    minion.hostname = "k8s-minion"
    minion.provider :libvirt do |libvirt, override|
      libvirt.memory = 2048
      libvirt.nested = true
    end
    master.provision "shell", inline: <<-SHELL
      dnf install -y ansible
    SHELL
    master.provision :ansible do |ansible|
      ansible.playbook = "minion.yml"
    end
  end
 
end
