Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/precise64"
  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
    v.cpus = 2
  end
  config.vm.network "forwarded_port", guest: 9080, host: 9080
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "devops/ansible/playbook.yml"
    ansible.verbose = "v"
  end
end
