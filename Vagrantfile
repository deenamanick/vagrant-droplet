VAGRANT_TOKEN = ""
Vagrant.configure(2) do |config|
    config.vm.define "droplet" do |node|
      node.vm.host_name = "droplet.digitalocean.com"
      node.vm.provider :digital_ocean do |provider, override|
        override.ssh.private_key_path = 'id_rsa'
        override.vm.box = 'digital_ocean'
        override.vm.box_url = "https://github.com/devopsgroup-io/vagrant-digitalocean/raw/master/box/digital_ocean.box"
        provider.token = "#{VAGRANT_TOKEN}"
        provider.private_networking = true
        provider.image = "ubuntu-14-04-x64"
        provider.region = "sgp1"
        provider.size = "4gb"
      end
    end
  end
