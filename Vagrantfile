Vagrant.configure("2") do |config|
  config.vm.box = "mylab.box"
  config.vm.hostname = "ashe"
  config.vm.network :private_network, ip: "192.168.0.88"
  config.vm.synced_folder "./shared", "/vagrant_data",id: "vagrant-root",
      owner: "vagrant",
      group: "www-data",
      mount_options: ["dmode=775,fmode=764"]
  config.vm.provider :virtualbox do |vb|
    vb.customize [
      "modifyvm", :id,
      "--natdnshostresolver1", "on",
      "--memory", "1024"
    ]
  end
end