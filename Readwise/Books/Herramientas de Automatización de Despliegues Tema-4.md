# Herramientas de Automatización de Despliegues Tema-4

deck:: [[UNI::Herramientas de Automatización de Despliegues Tema-4]]\
author:: [[UNIR]]\
full-title:: "Herramientas de Automatización de Despliegues Tema-4"\
category:: #books\
\
tags:: Herramientas-de-Automatización-de-Despliegues UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/edc3c94d-bca3-4fa2-89a7-0b0b46f46668.jpg)
## Highlights
- id:: 63c66a05-d749-4c9c-a450-c7be9af712cb
   Ejemplo de código en ChefSpec #flashcard 
    require 'chefspec' describe 'vim_pruebas_chef::default' do platform 'ubuntu' context 'with default attributes' do it "should have default install_method 'package'" do expect(chef_run.node['vim']['install_method']).to eq('package') end end end
  
     (Page 12)
-
- id:: 63c66a05-5fd2-497c-93d0-8d63ff89551f
   ¿Con qué comando puedes ejecutar los tests unitarios de ChefSpec? #flashcard 
    $ chef exec rspec .
  
     (Page 13)
-
- id:: 63c66a05-2f6d-4b45-a8ca-68b3c6e872d8
  
  Un nodo se puede representar en Test Kitchen con cualquier tipo de virtualización, a través de plugins denominados drivers. En la mayoría de los casos se suele utilizar Vagrant, pero hay diferentes alternativas tales como Docker o cualquiera de los muchos proveedores de nube soportados, como Amazon Web Services o DigitalOcean. #flashcard 
  
  
     (Page 18)
-
- id:: 63c66a05-e866-423b-b168-c2f5d1a57a06
  
  require'spec_helper' if os[:family] == 'ubuntu' describe package('vim') do it {should be_installed} end #flashcard 
  
  
     (Page 26)
-
- id:: 63c66a05-849c-4fb1-8a2a-31f040cb1e23
   CONTINUE #flashcard 
    end end end end end if os[:family] =='redhat' describe package('vim-minimal') do it {should be_installed} describe package('vim-enhanced') do it {should be_installed} describe command('vim --version') do its (:stdout) {should match /VIM - Vi IMproved/}
  
     (Page 27)
-
- id:: 63c66a05-b177-4dda-807a-f7182b5c650e
   ¿Cómo puedes aplicar los tests a una instancia ya aprovisionada con TestKitchen? #flashcard 
    Debido a que ya tenemos la instancia aprovisionada desde el paso anterior, se pueden aplicar nuevos cambios fácilmente para probarlos y comprobar el resultado de las pruebas. kitchen verify package-ubuntu-1804
  
     (Page 27)
-