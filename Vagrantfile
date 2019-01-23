Vagrant.configure("2") do |config|
  config.vm.define "ros1404" do |config|
    config.vm.box = "ubuntu/trusty64"
    config.vm.hostname = "ros1404"
  end

  config.vm.define "ros1604" do |config|
    config.vm.box = "ubuntu/xenial64"
    config.vm.hostname = "ros1604"
  end

  config.vm.define "ros1804" do |config|
    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = "ros1804"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.galaxy_roles_path = "../"
    ansible.playbook = "example.yml"
  end

end
