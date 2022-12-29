# Configurando o Gateway como NAT

  * Antes de iniciarmos o desenvolvimento do projeto é válido considerar as definições da rede externas ao nosso gateway server  nas tabelas abaixo:
  
<p><center>Tabela 1: Definições da rede externa: </center></p>  

| DESCRIÇÃO   | IP            |
|:------------|:------------- |
| rede        | 10.0.2.0      |
| máscara     | 255.255.255.0 |
| VirtualBox (gateway)     | 10.0.2.2      |
| Broadcast   | 10.0.2.255    |

   * As definições de rede da rede interna ao gateway server estão exemplificadas na Tabela 2.

<p><center> Tabela 2: Definições da rede interna</center></p>

| DESCRIÇÃO   | IP            |
|:------------|:------------- |
| rede        | 10.0.0.0      |
| máscara     | 255.255.255.0 |
| Gateway     | 10.0.0.1      |
| Broadcast   | 10.0.0.255    |
| NameServer1 | 10.0.0.101     |
| NameServer2 | 10.0.0.120     |
| samba | 10.0.0.132   |

# Configuração do firewall/NAT
 
 Pré-requisito
  * Configurar o firewall no linux;
  
  ## Como habilitar um firewall?
  
   1. Antes de qualquer coisa, precisamos estar logados da forma correta:
     Ao acessar o terminal, provavelmente a primeira coisa que você verá será o mesmo da imagem abaixo:
      
      /imagem do aluno@samba, ou algo assim/
      
      Precisaremos dar o seguinte comando para logarmos no usuário redes: `su redes` , sua senha é :
      
       | Senha: admin@Lab92|
       |-------------------|
      
       
       logo em seguidas devemos acessar nossa vpn:
       
       /imagem de vpn e link para acessar como fazer o acesso do openvpn/
       
       Parte de explicar o ssh do adm no Gw mais a imagem do ssh:
       
       /imagem e tals/
   
 2. habilitar o firewall e permitir o acesso ao ssh:
   Para isso digite o seguinte comando, como exemplifica a imagem:
   
     <p><center> Figura 1: Acessar ssh </center></p>   
        <img src="images_GW/img1_sudoenable_GW.png" alt=""
        title="Figura 1: Acessar sshr" width="800" height="auto"/> <br/>

 3. Alterar os parâmetros do arquivo abaixo. Para isso, remova a marca de comentário (#) da linha em questão, tal qual a figura abaixo:
