## -*- mode: ruby -*-
# vi: set ft=ruby :
VAGRANTFILE_API_VERSION = '2'
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "ubuntu/trusty64"
    config.vm.box_check_update = false
    config.vm.hostname = "ubuntu"
    # VirtualBox
    config.vm.define "server1" do |sr1|
        sr1.name = "server1"
        sr1.memory = 768
        sr1.cpus = 2
    end
    # VirtualBox2
    config.vm.define "server2" do |sr2|
        sr2.name = "server2"
        sr2.memory = 768
        sr2.cpus = 2
    end
    config.vm.provision :shell, inline: "ntpdate ntp.ubuntu.com"
    config.vm.provision :shell, inline: "apt-get update"
    config.vm.provision :shell, inline: "apt-get install -y libffi-dev libssl-dev python-dev python-pip unzip git ntp"
end
