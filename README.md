Uma biblioteca de autenticação simples para [CodeIgniter 4](https://codeigniter.com).

**Recursos:**
- V1.0.0 <br />
&nbsp;&nbsp; Cadastro <br />
&nbsp;&nbsp; Ativação de email <br />
&nbsp;&nbsp; Login/Logout <br />
&nbsp;&nbsp; Senha esquecida <br />
&nbsp;&nbsp; Configurações da conta (com opções de alteração de senha e e-mail adequadas) <br />
&nbsp;&nbsp; Proteção CSRF <br />
&nbsp;&nbsp; localização <br />
- V1.0.2 <br />
&nbsp;&nbsp; Fix  <br />
&nbsp;&nbsp; Recaptcha [NEW]  <br />
&nbsp;&nbsp; Sistema de rank  <br />
&nbsp;&nbsp; Novas funções (Area Administrativa) <br />
&nbsp;&nbsp; &nbsp;&nbsp; Banir  <br />
&nbsp;&nbsp; &nbsp;&nbsp; Deletar  <br />
&nbsp;&nbsp; &nbsp;&nbsp; Ativar/Desativar  <br />

## Instalar

Baixe o pacote e coloque na pasta `app/ThirdParty/`.
Abra `app/Config/Autoload.php` e adicione ao autoload assim:

```
$psr4 = [
    'Config'        => APPPATH . 'Config',
    APP_NAMESPACE   => APPPATH,
    'App'           => APPPATH,
    'Auth'          => APPPATH . 'ThirdParty/VAuth',
];
```

Configure o e-mail em `app/Config/Email`. 
**Preencha os campos `$fromEmail` e `$fromName` também!** 
Eu sugiro que você use [mailtrap.io] (https://mailtrap.io) para desenvolvimento local.

Habilite CSRF em `app/Config/Filters`.

Certifique-se de que seu banco de dados está configurado no arquivo `.env` ou em `app/Config/Database.php`. 
Instale a tabela de usuários executando o seguinte comando na raiz do projeto:

**`php spark migrate`**

Visite `/register` em seu servidor local para começar.

## Lista de afazeres

- use a nova regra de validação `is_not_unique` sempre que possível.
