---
title: Atualizar credenciais de acesso do GitHub
intro: 'As credenciais de {% data variables.product.product_name %} incluem{% ifversion not ghae %} não apenas sua senha, mas também{% endif %} os tokens de acesso, Chaves SSH e tokens do aplicativo da API que você usa para se comunicar com {% data variables.product.product_name %}. Se houver necessidade, você mesmo pode redefinir todas essas credenciais de acesso.'
redirect_from:
  - /articles/rolling-your-credentials
  - /articles/how-can-i-reset-my-password
  - /articles/updating-your-github-access-credentials
  - /github/authenticating-to-github/updating-your-github-access-credentials
  - /github/authenticating-to-github/keeping-your-account-and-data-secure/updating-your-github-access-credentials
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Identity
  - Access management
shortTitle: Atualizar credenciais de acesso
---

{% ifversion not ghae %}
## Solicitar uma nova senha

1. Para solicitar uma nova senha, acesse {% ifversion fpt or ghec %}https://{% data variables.product.product_url %}/password_reset{% else %}`https://{% data variables.product.product_url %}/password_reset`{% endif %}.
2. Insira o endereço de e-mail associado à sua conta em {% ifversion ghae %}{% data variables.product.product_name %}{% else %}{% data variables.product.product_location %}{% endif %} e, em seguida, clique em **em Enviar e-mail de redefinição de senha.** O e-mail será enviado para o endereço de e-mail de backup, se você tiver um configurado. ![Caixa de diálogo para solicitar e-mail de redefinição de senha](/assets/images/help/settings/password-recovery-email-request.png)
3. Nós enviaremos por e-mail um link para você redefinir sua senha. Clique nele em até 3 horas após o recebimento do e-mail. Se você não receber o e-mail com o link, verifique sua pasta de spam.
4. Se você tiver habilitado a autenticação de dois fatores, será solicitado que você crie suas credenciais de 2FA:
   * If you have {% data variables.product.prodname_mobile %}, you will be sent a push notification to verify your identity. Open the push notification or the {% data variables.product.prodname_mobile %} app and enter the two-digit code shown to you on the password reset page in your browser. ![Two-factor {% data variables.product.prodname_mobile %} authentication prompt](/assets/images/help/2fa/2fa-mobile-challenge-password-reset.png)
      * To skip using GitHub Mobile to verify, click **Enter two-factor authentication or recovery code**. ![Two-factor GitHub Mobile authentication prompt on {% data variables.product.product_name %} with "Enter two-factor authentication or recovery code" highlighted](/assets/images/help/2fa/2fa-github-mobile-password-reset.png)
   * Digite o seu código de autenticação ou um dos seus códigos de recuperação e clique em **Verificar**. ![Instrução de autenticação de dois fatores](/assets/images/help/2fa/2fa-password-reset.png)
     * If you have added a security key to your account, click **Use security key** instead of typing an authentication code.
     * If you have set up [{% data variables.product.prodname_mobile %}](https://github.com/mobile), click **Authenticate with GitHub Mobile** instead.
5. Digite uma nova senha, confirme a sua nova senha e clique em **Alterar senha**. Para ajudar a criar uma senha forte, consulte "[Criar uma senha forte](/articles/creating-a-strong-password)".
  {% ifversion fpt or ghec %}![Password recovery box](/assets/images/help/settings/password-recovery-page.png){% else %}
  ![Caixa para recuperar senha](/assets/images/enterprise/settings/password-recovery-page.png){% endif %}

{% tip %}

Para evitar perder a sua senha no futuro, sugerimos o uso de um gerenciador de senhas seguro, como [LastPass](https://lastpass.com/) ou [1Password](https://1password.com/).

{% endtip %}

## Alterar uma senha existente

{% data reusables.repositories.blocked-passwords %}

1. {% data variables.product.signin_link %} para o {% data variables.product.product_name %}.
{% data reusables.user-settings.access_settings %}
{% data reusables.user-settings.security %}
4. Em "Change password" (Alterar senha), insira a senha antiga, digite uma nova senha forte e confirme a nova senha. Consulte "[Criar uma senha forte](/articles/creating-a-strong-password)" para obter ajuda sobre esse assunto.
5. Clique em **Update password** (Atualizar senha).

{% tip %}

Para maior segurança, além de alterar a senha, habilite também a autenticação de dois fatores. Consulte [Sobre a autenticação de dois fatores](/articles/about-two-factor-authentication) para ver mais detalhes.

{% endtip %}
{% endif %}
## Atualizar tokens de acesso

Consulte "[Revisar integrações autorizadas](/articles/reviewing-your-authorized-integrations)" para ver instruções sobre como revisar e excluir tokens de acesso. Para gerar novos tokens de acesso, consulte "[Criar um token de acesso pessoal](/github/authenticating-to-github/creating-a-personal-access-token)."

{% ifversion not ghae %}

Se você redefiniu sua senha da conta e gostaria de acionar um logout do aplicativo de {% data variables.product.prodname_mobile %}, você pode revogar a sua autorização do aplicativo OAuth "GitHub iOS" ou "GitHub Android". Isso encerrará todas as instâncias do aplicativo de {% data variables.product.prodname_mobile %} associado à sua conta. Para obter mais informações, consulte "[Revisar integrações autorizadas](/authentication/keeping-your-account-and-data-secure/reviewing-your-authorized-integrations)".

{% endif %}

## Atualizar chaves SSH

Consulte "[Revisar as chaves SSH](/articles/reviewing-your-ssh-keys)" para ver instruções sobre como revisar e excluir chaves SSH. Para gerar e adicionar novas chaves SSH, consulte "[Gerar uma chave SSH](/articles/generating-an-ssh-key)".

## Redefinir tokens da API

Se você tiver algum aplicativo registrado no {% data variables.product.product_name %}, talvez precise redefinir os tokens OAuth dele. Para obter mais informações, consulte o ponto de extremidade "[Redefinir uma autorização](/rest/reference/apps#reset-an-authorization)".

{% ifversion not ghae %}
## Impedir acesso não autorizado

Consulte "[Impedir acesso não autorizado](/articles/preventing-unauthorized-access)" para obter mais dicas sobre como proteger a conta e impedir acesso não autorizado.
{% endif %}
