# Resolução dos desafios:

A resolução foi dividida em duas partes, assim como o desafio original:

### Challenge Ops:

1. Foi criada uma instância de WordPress na plataforma Unix/Linux utilizando Amazon Lightsail, seguindo o tutorial que foi indicado.

![image](https://github.com/mzsmatheus/devops-challenge-junior/assets/63678546/12275388-66d1-40a3-8f31-6bde26e058e5)


2. Após configuração da senha inicial, foi implementada a configuração para manter um IP estático.

Informações de acesso da página WordPress:
> URL: http://3.210.174.60/wp-login.php <br>
>   Username: user <br>
>   Password: /=5BQswsdFfQ

![image](https://github.com/mzsmatheus/devops-challenge-junior/assets/63678546/16042df3-2de3-45aa-a7f1-e57068cb99d0)



3. Depois da resolução dos erros no código (Challenge Dev), o plugin [devops_challenge.php](devops_challenge.php) foi compactado em formato [.zip](plugin_correcao.zip) e implementado via aba de plugins do WordPress.

![image](https://github.com/mzsmatheus/devops-challenge-junior/assets/63678546/419d6cd9-3542-44e5-823f-c4299cf1b24f)


### Challenge Dev:
Os 3 erros seguintes foram encontrados no código do arquivo [devops_challenge.php](devops_challenge.php):

1. Falta da abertura e fechamento da TAG padrão do PHP.
2. Na linha 34 do código, estava faltando ";" após o final da função "$lyrics = explode( "\n", $lyrics )".
3. Na linha 55, a função "devops_challenge" não estava sendo chamada por nenhum hook, foi inserido o hook 'admin_notices' para cumprir com o que foi solicitado (função deve ser executada no contexto de avisos no admin WordPress).

#### Observações: 

O CSS do arquivo PHP não foi alterado. <br>
Os prints desta descrição podem ser acessados individualmente na pasta "prints". <br>
O arquivo de texto somente da resolução está salvo com o nome "resolucao.md".