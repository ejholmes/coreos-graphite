Vagrant.configure('2') do |config|
  config.vm.box = 'coreos-beta'
  config.vm.box_url = 'http://beta.release.core-os.net/amd64-usr/current/coreos_production_vagrant.json'

  config.vm.network :private_network, ip: '172.17.8.101'

  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.vm.network :forwarded_port, guest: 2003, host: 2003
  config.vm.network :forwarded_port, guest: 8125, host: 8125

  config.vm.provision :file, source: './user-data', destination: '/tmp/vagrantfile-user-data'
  config.vm.provision :file, source: './units', destination: '/media/state/units'
  config.vm.provision :shell, inline: 'mv /tmp/vagrantfile-user-data /var/lib/coreos-vagrant/', privileged: true
end
