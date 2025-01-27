# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

# Debemos tomar nota de cual es el path o ruta desde la que se ejecuta gunicorn
# /home/vagrant/.local/share/virtualenvs/trobmor-3Xol3Vsb/bin/gunicorn

Vagrant.configure("2") do |config|
  config.vm.box = "debian/bullseye64"
  config.vm.define "project" do |project|
    project.vm.hostname = "project"
    project.vm.network "forwarded_port", guest: 8080, host: 8080
    project.vm.network "private_network", ip: "192.168.50.20"
    project.vm.provision "shell", name: "basic_provision", inline: <<-SHELL
        sudo apt-get update
        sudo apt-get install -y python3-pip
        apt-get install -y nginx
        sudo mkdir -p /var/www/trobmor
        sudo chown -R $USER:www-data /var/www/trobmor
        sudo chmod -R 775 /var/www/trobmor
        sudo cp /vagrant/conf_project/.env /var/www/trobmor/
        sudo cp /vagrant/conf_project/wsgi.py /var/www/trobmor/
        sudo cp /vagrant/conf_project/application.py /var/www/trobmor/
        sudo cp /vagrant/conf_project/flask_app.service /var/www/trobmor/
        sudo cp /vagrant/conf_project/trobmor.conf /var/www/trobmor/

    SHELL
    project.vm.provision "shell", name: "basic_provision", privileged: false, inline: <<-SHELL
        pip3 install pipenv
        pip3 install python-dotenv
      SHELL
  end #project
end
