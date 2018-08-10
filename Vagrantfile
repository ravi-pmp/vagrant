Vagrant.configure("2") do |config|
  config.ssh.insert_key = false

  config.vm.define "nn1" do |nn1|
    nn1.vm.box = "generic/rhel7"
    nn1.vm.hostname = "nn1.ravi.local"
    nn1.vm.network :forwarded_port, guest: 22, host: 2222, id: "ssh", disabled: true
    nn1.vm.network :forwarded_port, guest: 22, host: 2230, auto_correct: true
  end

  config.vm.define "dn1" do |dn1|
    dn1.vm.box = "generic/rhel7"
    dn1.vm.hostname = "dn1.ravi.local"
    dn1.vm.network :forwarded_port, guest: 22, host: 2222, id: "ssh", disabled: true
    dn1.vm.network :forwarded_port, guest: 22, host: 2231, auto_correct: true
  end

  config.vm.define "dn2" do |dn2|
    dn2.vm.box = "generic/rhel7"
    dn2.vm.hostname = "dn2.ravi.local"
    dn2.vm.network :forwarded_port, guest: 22, host: 2222, id: "ssh", disabled: true
    dn2.vm.network :forwarded_port, guest: 22, host: 2232, auto_correct: true
  end
  config.vm.provider "vmware_workstation" do |v|
     v.vmx["memsize"] = "3000"
     v.vmx["numvcpus"] = "2"
  end
end
