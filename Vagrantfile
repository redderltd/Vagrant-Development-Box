# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant::Config.run do |config|

  config.vm.box = "base"
  config.vm.network "33.33.33.100"
  # remove the next line when running on a windows host system (Windows does not have NFS support)
  config.vm.share_folder("v-root", "/vagrant", ".", :nfs => true)
  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "manifests"
    puppet.manifest_file = "app.pp"
  end
  
end

