## Configurando o SendGrid

O **SendGrid** é um serviço para o envio de e-mails transacionais e de marketing.

Além de bem simples, ele possui um plano gratuito para testes. Acesse [https://signup.sendgrid.com](https://signup.sendgrid.com) para criar uma conta gratuitamente.

<p style="text-align: center">
  <img src="../images/60.png" style="width: 45%"/>
</p>

Agora é preciso autenticar o domínio que será utilizado como remetente. Para isso, acesse o painel [Sender Authentication](https://app.sendgrid.com/settings/sender_auth) e clique em **Authenticate Your Domain**.

<p style="text-align: center">
  <img src="../images/61.png" style="width: 50%"/>
</p>

No primeiro item, **Which Domain Name Server (DNS) host do you use?**, informe o provedor onde o seu domínio está registrado. Se ele não estiver na lista, informe **Other Host (Not Listed)**.

Em **Which DNS Host?**, informe a URL do seu provedor. No nosso caso, informamos **Registro.br**.

No segundo item, **Would you also like to brand the links for this domain?**, mantenha a opção **No** selecionada e clique em **Next**.

<p style="text-align: center">
  <img src="../images/62.png" style="width: 55%"/>
</p>

Em **Domain You Send From**, informe o domínio que será utilizado como remetente do e-mail. No nosso caso, usamos *alganews.com.br*.

Para prosseguir, clique em **Next**.

<p style="text-align: center">
  <img src="../images/63.png" style="width: 50%"/>
</p>

Serão exibidos registros de DNS do tipo CNAME a serem configurados. Mantenha a tela aberta, pois vamos utilizá-la em seguida.

<p style="text-align: center">
  <img src="../images/64.png" style="width: 90%"/>
</p>

Abra o painel de configuração de Zona de DNS do seu provedor e insira os registros exibidos na tela anterior. No nosso caso, estamos usando o Registro.br, portanto adicionamos as entradas como você pode ver abaixo:

<p style="text-align: center">
  <img src="../images/65.png" style="width: 90%"/>
</p>

Volte na tela do SendGrid, selecione a opção **I've added these records** e clique em **Verify**.

Importante: Se a verificação falhar, tente novamente dentro de alguns minutos, por conta da propagação do DNS estar sendo realizada.

<p style="text-align: center">
  <img src="../images/66.png" style="width: 45%"/>
</p>

Feito a verificação, a tela de sucesso será exibida.

<p style="text-align: center">
  <img src="../images/67.png" style="width: 90%"/>
</p>

Agora precisamos gerar uma chave de API para o nosso back-end. Acesse a [listagem de chaves](https://app.sendgrid.com/settings/api_keys) e em seguida clique em **Create API Key**.

<p style="text-align: center">
  <img src="../images/68.png" style="width: 65%"/>
</p>

Adicione um nome qualquer para a chave, selecione a opção **Full Access** e em seguida clique em **Create & View**. 

Copie a chave gerada e guarde em um local seguro, porque vamos usá-la mais a frente.

<p style="text-align: center">
  <img src="../images/69.png" style="width: 70%"/>
</p>


#### Referências

- [Documentação do SendGrid](https://docs.sendgrid.com/)
