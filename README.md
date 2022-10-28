---
title: apiki - Devops challenge júnior


tags: 
author: 
source: 
---
# Devops challenge júnior - plugin
Segue resumidamente alguns dos pontos sobre o deploy e 
manutenção do plugin de wordpress **devops_challenge.php**

### **Infraestrutura homologada (opcional)**
A infraestrutura escolhida para a implantação foi uma máquina da AWS no serviço de lightsail, com a seguinte configuração:
- 1 vcpu
- 1 gb de ram
- 40 gb de armazenamento

Nos testes realizados, foi feita a tentativa em uma maquina de 500 mb de memória, porém, o banco de dados nao subia utilizando o docker, isso será corrigido no issues **#1**

### **Arquitetura**

A arquitetura de software consiste na utilização de 4 containers, sendo 1 **nginx** como servidor web, 1 banco de dados **mysql** , 1 *php-fpm* como servidores de aplicação e 1 bot para geração de certificados ssl para utilização de https, este ainda nao configurado, será consertado após analise no issues **2**, por enquanto, sem impacto na produção.
### Versões de software

- Mysql - 8.0.29
- Nginx - 1.22.0
- php-fpm - 8.1-fpm
- certbot - nightly


### Hotfix1 - issue **3**

versão_afetada: 1.0

- linha 1 
Faltou a flag de interpretação PHP

**<?php**
 
 - linha 35
 Faltou ponto e vírgula no final da linhapara o php interpretar a proxima função
         $lyrics = explode( "\n", $lyrics ) **;**
         
 - linha  54
 Faltou a função do próprio wordpress de adição de função nas notificações
 
 add_action( '**admin_notices**', 'devops_challenge' ); 
 
#############################fim da documentação

### CREDENCIAIS

- aws
link: https://938023195502.signin.aws.amazon.com/console
chave de acesso:AKIA5UZUKCNXPH3U4PO7
chave de acesso secreta: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
Usuario: contribuidor
Senha: apiki_1541tre
- wordpress
http://44.206.234.209/
Uwuario: iago
Senha: eKo9(V@@XK*gHc4w%!
