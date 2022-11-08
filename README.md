# Devops challenge júnior


### → Challenge Ops:
> Iniciar e configurar uma instância do WordPress no Amazon Lightsail <br>
https://lightsail.aws.amazon.com/ls/docs/pt_br/articles/amazon-lightsail-tutorial-launching-and-configuring-wordpress <br>
Fazer da etapa 1 até a 5 somente.

Seguir até etapa 5.

http://44.197.47.8/wp-admin

Login user
Senha: 9WBbp7k3RFHh

![image](https://user-images.githubusercontent.com/2781316/200460878-f1807430-b1e0-4d19-a342-3d5a6153ac4c.png)


### → Challenge Dev:
> Resolva os 3 erros no plugin<br>
[Plugin DevOps Challenge](devops_challenge.php)

O codigo do Plugin é uma copia do Hello.php do plugin Hello Dolly, que vem padrão no Wordpress então vi o que faltava e corrigir os erros de Sintax.

Encontrei os 3 erros e também consertei o cabeçalho da aplicação por esta fora do padrão de plugin.

✔ Primeiro erro falta do <?php tag padrão de abertura de arquivo php.

✔ Segundo falta de ;  na linha 33 ``` $lyrics = explode( "\n", $lyrics ); ```

✔ Terceira foi falta da função ('admin_notices') na linha 54 ``` add_action( 'admin_notices', 'devops_challenge' ); ```

✔ Extra o padrão de plugins é cabeçalho comentado com nome do plugin e outras informações.
``` /**
 * @package Devops_challenge_Junior
 * @version 1.0
* Plugin Name: Devops challenge Júnior
* Plugin URI: https://apiki.com/
* Description: Sabe de nada, inocente! Ordinária!!
* Author: Apiki WordPress
* Version: 1.0
*/

```

### →  Instalação do Plugin 
Pode criar uma pasta dentro de /wp-content/plugins/ com nome do plugin sem espaço e caracteres especiais. 
Dentro da pasta criar ou transferi o artigo PHP com mesmo nome da pasta.

Pode também usar o comando no terminal.

```
sudo wp scaffold plugin Devops-challenge-Junior --skip-tests 

```
Com esse comando ele criar todos os arquivos necessario para um plugin, (--skip-tests) para retirar parte de teste unitários.
Como foi usado Sudo tive que usar CHMOD 777 para liberar os arquivos para serem acessados com usuário padrão que conexão SSH.


### → Ativa do plugin 


![image](https://user-images.githubusercontent.com/2781316/200460641-5ed3b89e-bfbe-4423-ae7d-5c6d23140b29.png)

* Plugin funcionando:

![image](https://user-images.githubusercontent.com/2781316/200460972-8e58edd5-d214-4bec-9c78-a70c262cbb26.png)



### Entrega
1. Efetue o fork deste repositório e crie um branch com o seu nome e sobrenome. (exemplo: fulano-dasilva)
2. Após finalizar o desafio, crie um Pull Request.
3. Aguarde algum contribuidor realizar o review.
4. Dados de acesso do WordPress e Lightsail com tudo configurado e funcionando
5. Prints e url "http://PublicIpAddress/wp-login.php"
6. Documentação (Opcional)
7. Arquitetura (Opcional)
8. Plugin informado arrumado e versionado
9. Suba o plugin para a sua instalação WordPress Lightsail e ative o mesmo.
