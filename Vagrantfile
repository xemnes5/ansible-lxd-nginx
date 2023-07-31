

ENV['VAGRANT_SERVER_URL'] = 'https://vagrant.elab.pro'

  HOSTS=[
    { :hostname => 'stage1', :box => 'ubuntu/focal64', :ip => '192.168.57.100', :cpu => 1, :memory => 1024, :ssh_port => 2257 },
    { :hostname => 'prod1',  :box => 'ubuntu/focal64', :ip => '192.168.58.100', :cpu => 1, :memory => 1024, :ssh_port => 2258 },
  ]

Vagrant.configure("2") do |config|

  HOSTS.each do |vmcfg|
    config.vm.define vmcfg[:hostname] do |node|
      node.vm.box = vmcfg[:box]
      node.vm.hostname = vmcfg[:hostname]
      node.vm.network :private_network, ip: vmcfg[:ip]
      node.vm.network 'forwarded_port', guest: 22, host: vmcfg[:ssh_port], id: 'ssh'
        
      node.vm.provider :virtualbox do |vb|
	vb.cpus = vmcfg[:cpu]
	vb.memory = vmcfg[:memory]
      end
    end
  end
end	
