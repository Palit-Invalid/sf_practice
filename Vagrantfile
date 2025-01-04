Vagrant.configure(2) do |config|
  config.vm.box = "generic/ubuntu1804"
  config.vm.provision "file", source: "./empty", destination: "empty"
  config.vm.define "ubuntu" do |ub|
    ub.vm.provider :virtualbox do |vb|
      vb.gui = false
      vb.name = "ubuntu"
      vb.memory = 4096
      vb.cpus = 4
    end

    ub.vm.provision 'shell' do |s|
      s.path = 'setup.sh'
      s.privileged = true
    end
  end
end
