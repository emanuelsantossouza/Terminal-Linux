# Caderno de anotação dos comandos no terminal do Linux🐧


## 1- Comando de listagem de arqivos e diretorios:

### 1.1 ls:<br> 
#### É usado para listar arquivos e diretorios. <br> 

### 1.2 ls -a:<br> 
#### O atributo a é usado para mostrar tudo. <br>

### 1.3 ls -R:<br> 
#### Mostra todos os arquivos e diretorios escondido. <br>

### 1.4 ls -l:<br> 
#### Mostra o formato de lista longa. <br>

### 1.5 ls /etc/*.conf:<br> 
#### A estrela no diretorio está fazendo uma busca ou referencia a uma  determinada quantidade de caracteres "No caso o .conf e poderia ser qualquer outro que você deseja buscar". <br>

### 1.6 ls /etc/?a*:<br> 
#### O ponto de interrogação faz uma busca pelo o diretorio "/etc" e busca apenas um caracter "a" e como a estrela esta apos do a pode vim qualquer arquivo ou pasta que contenha a. <br>

### 1.7 O uso dos Couchetes []:<br> 
#### Os couchetes tem função de realiza um intervalo de caracteres por exemplo "ls /etc/p[a-i]" o comando a vai buscar algum arquivo ou diretorio que começa com a letra "p" e tem a variação de a até "i".<br>

### 1.8 Couchetes [] com virgula ",":<br> 
#### As vigulas tem a função de delimitar apenas para um caráter apenas com no exemplo a seguir "ls /etc/p[a-i,e]".<br>

### 1.9 As chaves{} ou couchetes[]?<br> 
#### As chaves apenas buscam um padrão é um ou outro "caso coloque dois, sera buscado ambos" como no exemplo a seguir ls /etc/*.{tab,as}.<br>


## 2- Criacão de um arquivo de texto.<br>

### 1- Touch:<br>
#### É o comando usado para a criação de arquivos de texto.<br> Formula (touch + nome do aquivo + tipo). <br> Exemplo touch oi.txt<br>

### 2- Nano:<br>
#### É o comando usado para a edição de arquivos de texto. Mas caso esse arquivo não esteja criado o comando nano cria e logo em seguida realiza as modificações.<br> Formula (nano + nome do arquivo + tipo).<br> Exemplo (nano oi.txt)<br> 


## 3- PWD:<br> 
#### Mostra o caminho que você está no terminal.<br> 

## 4- Cat:<br> 
#### Pega as informaçoes de um determinado arquivos e exibi na tela.<br> Exemplo (cat /etc/services)

## 5- rm: é usado para Apagar
### 1.1 rm -rf: apaga tudo, diretorio e arquivos

## 6- tac: ele é igual a cat mais so que exibe ao contrario de traz para frente

## 7-cp: é para copiar arquivos e mover arquivos
exemplo cp Aulalinux.txt Faculdade
aula linux é o arquivo que eu estou copiando. Faculadade é o diretorio que eu estou movendo a copia.
cp /etc/s* /disk2/backup/ -r -v


## 8- mv: Caso precise mover use mv + nome do arquivo + novo diretorio
mv AulaLinux.txt Faculdade 
exemplo
mv /home/emanuellinux/* /disk2/ -i -v
mv arquivo1.txt Arquivo.txt


## 9- Usuarios:
1.1- useradd convidado -m -c "Benedito"
no codigo acima você esta passando o nome de usario, depois, o padrão -m para ser criado as pastas padrões, logo após vem o -c criar uma nova pasta para o novo usuario.

1.2-  userdel -f convidado
O codigo apresentado é usado para apagar o usario.

1.3- useradd convidado -m -c "Benedito" -e 18/08/2022
Temos um novo parametro o -e + data do termino, é usado para dar uma data de uso para o novo usario, ele pode usar até aquela determinada data depois a sua conta é expirada.

1.4- usermod convidado 
Com esse novo comando você pode realizar alterações, apenas passe o paramentro quw você deseja alterar.

1.5- usermod convidado -s /bin/bash
O parametro -s /bin/bash é utilizado para add o shell a pasta, o shell é que faz as configurações finais

1.6- passwd convidado -e 
O comando acima esta requerendo que o novo usario ao entra na conta, crie uma nova senha.
Caso deseje da uma data para a troca de senha, apenas coloque a data limite na frente do paramentro => passwd convidado -e 18/08/2022.

## 10- -G: <br>
é uma parametro que move um usario padrão para uma determinado grupo dando as permissoes que aquele grupo tem.<br>
=> usermod -G adm,sudo convidado
usermod + o parametro -G + os grupos "adm,sudo" + O usuario<br>

## 11- Grupos e permissões:
1.1 (chomd 750 /adm/) O codigo apresentado desta mudando as permissões do diretorio adm, o número 750 é uma soma, o primerio valor é para o responsalvel pelo o repositrio, o segundo valor é para usuarios que estão no grupo desse diretorio e o terceiro é para usuarios que não esão no grupo do diretorio.

Para criar um novo grupo voce utiliza 
"groupadd GRP_VEN"
groupadd + nome do grupo

1.2 - (chown root:GRP_ADM texto-adm.txt) O codigo é para transferir o para o root ser o dono do diretorio 

                     Tabela para a soma:
![image](https://user-images.githubusercontent.com/99850729/185762075-671690be-f54c-4d2f-84de-46fc3e6be7d7.png)




## 13- Scripts

### 1- Como criar scripts?<br>
####Para criar um script você deve adicionar a extensão .sh no fianl do nome do arquivo que voce esta criando.<br>
Exemplo script.sh

### 2- Como rodar o um script?<br> 
####È muito facil para rodar um script voçê deve utilzar o seguinte comando ./+ o nome do arquivo.<br>
Exemplo ./script.sh

3- Caso o de erro deve ser porque o usuario que você logado não tem permissão para rodar ele. Caso isso aconteça utilize o seguiente codigo (chmod +x script.sh) ou (chmod 744 script.sh)so lembrando para realizar modificações você deve estar de usuario root

## 4- Caso queira retirar a permissão do diretorio ser rodado utlize o seguiente codigo (chmod -x script.sh) ou (chmod 644 script.sh)

## 14- Abaixar pacotes no Linux:<br>

1- apt-get: é usado para abaixar programas e pacotes mas não é tão amigavel com o usuario é um codigo mais de baixo nivel "Linguaguem de maquina"

apt list: Apresenta todo os pacotes disponivies que voce pode instalar
apt list --unstalled: todos os pacotes instalados na sua maquina
apt list --upgradeable: mostra as atualizações que pode ser atualizado
apt search samba: o search é usado para buscar algum pacote para realizar o instal dele
apt install net-tools: Para realizar a instalação use o install + o nome do pacote

16- Para copiar um arquivo:
wget https://github.com/emanuelsantossouza/Terminal-Linux/archive/refs/heads/main.zip


17- Disco:<br>
lsblk demostra os disco e as repartições da maquina
fdisk -l igual o comando anterior mas com mais informações

18- Como derrubar um usuario:<br>
  Mostra que esta online e o que esta fazendo, use o "ps"
  Mostra o que ele esta fazendo "w"
  Mostra o ip e assim é possivel derrubar o usuario "who -a"
  Deruba o usario apenas com o ip "kill 1667"

19- Montando um disk 
root@linuxserver:/# mkdir /disk2
root@linuxserver:/# mount /dev/sdb /disk2/
root@linuxserver:/# cd disk2/
root@linuxserver:/disk2# ls
lost+found
root@linuxserver:/disk2# touch arquivo.txt
root@linuxserver:/disk2# touch arquivo2.txt
root@linuxserver:/disk2#







