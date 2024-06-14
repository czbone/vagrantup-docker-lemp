Vagrant.configure(2) do |config|
  # Disable auto updating VirtualBox Guest Additions
  if Vagrant.has_plugin?("vagrant-vbguest")
    config.vbguest.auto_update = false
    config.vbguest.no_remote = true
  end

  config.vm.box = "ubuntu/jammy64"

  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provision "ansible_local" do |ansible|
    ansible.become = true
    ansible.playbook = "playbooks/main.yml"
    ansible.galaxy_role_file = "playbooks/requirements.yml"
    ansible.galaxy_command = 'ansible-galaxy install -r %{role_file} --force'
  end
end
