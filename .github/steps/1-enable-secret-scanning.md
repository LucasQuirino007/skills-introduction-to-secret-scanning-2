## Passo 1: Habilitar o Secret Protection

Se você checar seu e-mail, provavelmente acabou de receber um alerta do GitHub com o assunto "Possible valid secrets detected". Ah, não! 😮

Fique tranquilo! Colocamos algumas credenciais expiradas no exercício de propósito, já que repositórios públicos têm secret protection gratuitamente. Legal! 🕵️

Neste passo, você vai habilitar o secret protection no seu repositório. Depois de habilitá-lo, você vai adicionar uma nova credencial para ver como o secret protection identifica a credencial e te alerta.

> [!WARNING]
> Se o seu repositório for privado, você precisará do [GitHub Advanced Security](https://docs.github.com/en/enterprise-cloud@latest/get-started/learning-about-github/about-github-advanced-security) para continuar. Recomendamos [alterar o repositório deste exercício para público](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/setting-repository-visibility) para habilitá-lo.

### O que é um segredo?

No nosso contexto, um segredo (ou credencial) é uma string em texto puro, ou um par de strings, que autoriza o acesso a um serviço. Exemplos incluem AWS secret access keys/IDs, Google API keys ou GitHub Personal Access Tokens (PATs).

A documentação do GitHub traz a lista de [todos os padrões suportados](https://docs.github.com/en/code-security/secret-scanning/secret-scanning-patterns#supported-secrets).

### O que é secret protection?

O secret protection é uma ferramenta poderosa que permite aos times identificar essas credenciais em texto puro, removê-las e criar regras para evitar que elas sejam gravadas no GitHub logo de início.

O secret protection está disponível **gratuitamente para repositórios públicos** em todos os planos. Empresas que precisam dos recursos de secret protection em repositórios privados devem conhecer o [GitHub Advanced Security](https://github.com/security/advanced-security). Além do secret protection, ele também oferece análise estática avançada, software composition analysis (SCA) e ferramentas corporativas para gerenciar todo o seu pipeline de AppSec e reduzir seu perfil de risco.

### :keyboard: Atividade: Configurar o secret protection

1. No cabeçalho do seu repositório, abra **Settings** em uma nova aba do navegador.

1. Na navegação lateral esquerda, na seção **Security**, selecione **Advanced Security**.

1. Role a página para baixo, passando pelas seções **Code Scanning** e **Dependabot**, até encontrar a seção **Secret Protection**.

   > 💡 **Dica:** Também temos exercícios sobre [code scanning](https://github.com/skills/introduction-to-codeql) e [proteção da cadeia de suprimentos](https://github.com/skills/secure-repository-supply-chain)!

1. Ajuste a configuração padrão conforme abaixo.

   - **Secret Protection:** `enabled`
   - **Push Protection:** `disabled`

   <img width="400" alt="Configurações do secret protection" src="../images/secret-protection-configuration-settings.png" />

### :keyboard: Atividade: Commitar um arquivo sensível

Agora vamos (acidentalmente) commitar um arquivo sensível para ver como funciona. Não se preocupe, estas credenciais estão inativas.

1. No cabeçalho do seu repositório, clique na aba **Code**.

1. Acima da lista de arquivos, clique no menu suspenso **Add file** e selecione **Create new file**.

   <img width="350" alt="Botão de novo arquivo" src="../images/add-new-file-button.png"/>

1. Informe o nome de arquivo `credentials.yml` e copie para dentro dele as credenciais de exemplo **inativas** abaixo.

   <img width="400" alt="Criação do arquivo credentials.yml" src="../images/credentials-yml-file-creation.png"/>

   ```yaml
   default:
     aws_access_key_id: AKIAQYLPMN5HNM4OZ56B
     aws_secret_access_key: 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
     mongodb: mongodb+srv://svc-admin:kLeioeBne5lsopPf@mergington-high.avocado.mongodb.net
     output: json
     region: us-east-2
   ```

1. No canto superior direito, use o botão **Commit changes...** para commitar diretamente na branch `main`.

   > ❗️ **Importante:** Commitar na sua branch padrão normalmente não é uma prática recomendada. Fazemos isso apenas para simplificar o exercício.

1. Com o nosso arquivo de credenciais (acidentalmente) compartilhado, a Mona deve perceber rapidamente e preparar o próximo passo.
