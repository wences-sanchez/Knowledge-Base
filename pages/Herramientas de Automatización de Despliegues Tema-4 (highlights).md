title:: Herramientas de Automatización de Despliegues Tema-4 (highlights)
author:: [[UNIR]]
full-title:: "Herramientas de Automatización de Despliegues Tema-4"
category:: #books

tags:: #[[Herramientas-de-Automatización-de-Despliegues]] #[[UNI]]

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/edc3c94d-bca3-4fa2-89a7-0b0b46f46668.jpg)
- Highlights first synced by [[Readwise]] [[Friday, 28-10-2022]]
	- require 'chefspec' describe 'vim_pruebas_chef::default' do platform 'ubuntu' context 'with default attributes' do it "should have default install_method 'package'" do expect(chef_run.node['vim']['install_method']).to eq('package') end end end (Page 12)
		- **Note**: Ejemplo de código en ChefSpec
	- $ chef exec rspec . (Page 13)
		- **Note**: ¿Con qué comando puedes ejecutar los tests unitarios de ChefSpec?
	- Un nodo se puede representar en Test Kitchen con cualquier tipo de virtualización, a través de plugins denominados drivers. En la mayoría de los casos se suele utilizar Vagrant,  pero  hay  diferentes  alternativas  tales  como  Docker  o  cualquiera  de  los muchos  proveedores  de  nube  soportados,  como  Amazon  Web  Services  o DigitalOcean. (Page 18)
	- require'spec_helper' if os[:family] == 'ubuntu' describe package('vim') do it {should be_installed} end (Page 26)
	- end end end end end if os[:family] =='redhat' describe package('vim-minimal') do it {should be_installed} describe package('vim-enhanced') do it {should be_installed} describe command('vim --version') do its (:stdout) {should match /VIM - Vi IMproved/} (Page 27)
		- **Note**: CONTINUE
	- Debido  a  que  ya  tenemos  la  instancia  aprovisionada  desde  el  paso  anterior,  se pueden aplicar nuevos cambios fácilmente para probarlos y comprobar el resultado de las pruebas. kitchen verify package-ubuntu-1804 (Page 27)
		- **Note**: ¿Cómo puedes aplicar los tests a una instancia ya aprovisionada con TestKitchen?