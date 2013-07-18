Vagrant.configure('2') do |config|
  config.vm.box      = 'precise32'
  config.vm.box_url  = 'http://files.vagrantup.com/precise32.box'
  config.vm.hostname = 'rails-dev-box'

  config.vm.network :forwarded_port, guest: 3000, host: 3001
  config.vm.network :forwarded_port, guest: 3306, host: 3309

  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = 'puppet/manifests'
    puppet.module_path    = 'puppet/modules'
  end

  config.vm.synced_folder "/Users/royuen/Working/vagrant", "/vagrant"
end
