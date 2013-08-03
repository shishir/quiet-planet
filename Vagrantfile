# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
   config.vm.provision :chef_solo do |chef|
     chef.cookbooks_path = "cookbooks"
     chef.add_recipe "magento"
     chef.json = {
      'mysql'=> {
                 'server_debian_password' => "password",
                 'server_root_password'   => "password",
                 'server_repl_password'   => "password"
      }
    }
   end
end
