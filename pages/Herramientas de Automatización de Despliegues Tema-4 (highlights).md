title:: Herramientas de Automatización de Despliegues Tema-4 (highlights)

author:: [[UNIR]]
full-title:: "Herramientas de Automatización de Despliegues Tema-4"
category:: #books

tags:: Herramientas-de-Automatización-de-Despliegues UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/edc3c94d-bca3-4fa2-89a7-0b0b46f46668.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Ejemplo de código en ChefSpec #flashcard
		  id:: 96a3c9d5-8aea-41d1-bfab-f5268008c7aa
			- require 'chefspec' describe 'vim_pruebas_chef::default' do platform 'ubuntu' context 'with default attributes' do it "should have default install_method 'package'" do expect(chef_run.node['vim']['install_method']).to eq('package') end end end
		- (Page 12)
	- -
	- -
		- ¿Con qué comando puedes ejecutar los tests unitarios de ChefSpec? #flashcard
		  id:: 3ba093c3-fee0-46d4-81ee-bc29a07012db
			- $ chef exec rspec .
		- (Page 13)
	- -
	- -
		- Un nodo se puede representar en Test Kitchen con cualquier tipo de virtualización, a través de plugins denominados drivers. En la mayoría de los casos se suele utilizar Vagrant,  pero  hay  diferentes  alternativas  tales  como  Docker  o  cualquiera  de  los muchos  proveedores  de  nube  soportados,  como  Amazon  Web  Services  o DigitalOcean. #flashcard
		  id:: f65bda54-b785-42ac-bd0e-49f1252a09ed
		- (Page 18)
	- -
	- -
		- require'spec_helper' if os[:family] == 'ubuntu' describe package('vim') do it {should be_installed} end #flashcard
		  id:: 7340869c-75e4-402a-91f2-91aeaea6fcca
		- (Page 26)
	- -
	- -
		- CONTINUE #flashcard
		  id:: 7cd99cad-20fb-4c89-baf4-134174306a7a
			- end end end end end if os[:family] =='redhat' describe package('vim-minimal') do it {should be_installed} describe package('vim-enhanced') do it {should be_installed} describe command('vim --version') do its (:stdout) {should match /VIM - Vi IMproved/}
		- (Page 27)
	- -
	- -
		- ¿Cómo puedes aplicar los tests a una instancia ya aprovisionada con TestKitchen? #flashcard
		  id:: 0d1435e3-a534-44fc-8ab4-2e0562d1888a
			- Debido  a  que  ya  tenemos  la  instancia  aprovisionada  desde  el  paso  anterior,  se pueden aplicar nuevos cambios fácilmente para probarlos y comprobar el resultado de las pruebas. kitchen verify package-ubuntu-1804
		- (Page 27)
	- -