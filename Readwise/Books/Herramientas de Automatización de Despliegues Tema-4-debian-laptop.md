# Herramientas de Automatización de Despliegues Tema-4

deck:: [[UNI::Herramientas de Automatización de Despliegues Tema-4]]\
author:: [[UNIR]]\
full-title:: "Herramientas de Automatización de Despliegues Tema-4"\
category:: #books\
\
tags:: Herramientas-de-Automatización-de-Despliegues UNI  

![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/edc3c94d-bca3-4fa2-89a7-0b0b46f46668.jpg)
## Highlights
- id:: 6363991c-b9d1-4361-b7f6-0f7ce3a3b840
   Ejemplo de código en ChefSpec #flashcard 
    require 'chefspec' describe 'vim_pruebas_chef::default' do platform 'ubuntu' context 'with default attributes' do it "should have default install_method 'package'" do expect(chef_run.node['vim']['install_method']).to eq('package') end end end
  
     (Page 12)
-
- id:: 6363991c-1ff1-49cb-b8aa-f4dff189313f
   ¿Con qué comando puedes ejecutar los tests unitarios de ChefSpec? #flashcard 
    $ chef exec rspec .
  
     (Page 13)
-
- id:: 6363991c-3cac-4e9a-935b-ca322098e641
  
  Un nodo se puede representar en Test Kitchen con cualquier tipo de virtualización, a través de plugins denominados drivers. En la mayoría de los casos se suele utilizar Vagrant, pero hay diferentes alternativas tales como Docker o cualquiera de los muchos proveedores de nube soportados, como Amazon Web Services o DigitalOcean. #flashcard 
  
  
     (Page 18)
-
- id:: 6363991c-fafc-4dac-8305-747fbef3d878
  
  require'spec_helper' if os[:family] == 'ubuntu' describe package('vim') do it {should be_installed} end #flashcard 
  
  
     (Page 26)
-
- id:: 6363991c-7e37-4df1-90e0-c1b81f3797b0
   CONTINUE #flashcard 
    end end end end end if os[:family] =='redhat' describe package('vim-minimal') do it {should be_installed} describe package('vim-enhanced') do it {should be_installed} describe command('vim --version') do its (:stdout) {should match /VIM - Vi IMproved/}
  
     (Page 27)
-
- id:: 6363991c-ded1-432c-93d3-d578147ed309
   ¿Cómo puedes aplicar los tests a una instancia ya aprovisionada con TestKitchen? #flashcard 
    Debido a que ya tenemos la instancia aprovisionada desde el paso anterior, se pueden aplicar nuevos cambios fácilmente para probarlos y comprobar el resultado de las pruebas. kitchen verify package-ubuntu-1804
  
     (Page 27)
-