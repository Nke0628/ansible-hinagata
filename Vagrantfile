Vagrant.configure("2") do |config|

    config.vm.box = "centos/7"

    # IPは開発環境毎に変更する
    config.vm.network "private_network", ip: "192.168.33.10"

    # フォルダも設定する
    config.vm.synced_folder './shared', '/home/vagrant/shared'

    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "provisioning/site.yml"
      ansible.inventory_path = "provisioning/hosts"
      ansible.limit = 'all'
    end

end
