VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define "ubuntu" do |ubuntu|
    ubuntu.vm.hostname = "ufw"
    ubuntu.vm.box = "ubuntu/trusty64"
    ubuntu.vm.network "private_network", ip: "192.168.0.2"
    ubuntu.vm.provision "ansible" do |ansible|
      ansible.extra_vars = { ansible_ssh_user: 'vagrant' }
      ansible.verbose    = "v"
      ansible.playbook   = "ubuntu.yml"
    end
  end
end
