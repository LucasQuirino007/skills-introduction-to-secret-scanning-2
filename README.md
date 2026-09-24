# Introdução ao secret protection

_Aprenda a configurar o secret protection para identificar segredos e evitar que novos sejam commitados no seu repositório._

## Boas-vindas

Credenciais em texto puro armazenadas acidentalmente em repositórios no GitHub são um alvo comum para atacantes. Na prática, encontramos bem mais de um milhão de tokens armazenados na plataforma do GitHub todos os anos. Vamos aprender a evitar isso!

- **Para quem é este exercício**: Pessoas desenvolvedoras, engenheiras de DevOps e times de segurança.
- **O que você vai aprender**: Como identificar credenciais em texto puro no seu repositório e como evitar que elas sejam expostas no GitHub em pushes futuros.
- **Pré-requisitos**: Noções básicas de git e das funcionalidades do GitHub. Recomendamos que você conclua o [Introduction to GitHub](https://github.com/skills/introduction-to-github).
- **Duração**: Este curso leva menos de 15 minutos para ser concluído.

Neste curso, você vai:

1. Habilitar o secret protection
2. Identificar segredos armazenados no seu repositório
3. Habilitar o push protection
4. Impedir que segredos sejam gravados no seu repositório

### Como iniciar este exercício

Basta copiar o exercício para a sua conta, dar à sua Octocat favorita (Mona) **cerca de 20 segundos** para preparar a primeira lição e depois **atualizar a página**.

[![start-exercise](https://img.shields.io/badge/Copy%20Exercise-%E2%86%92-1f883d?style=for-the-badge&logo=github&labelColor=197935)](https://github.com/new?template_owner=dev-pods&template_name=skills-introduction-to-secret-scanning&owner=%40me&name=skills-introduction-to-secret-scanning&description=GitHub+Skills:+Introdu%C3%A7%C3%A3o+ao+Secret+Scanning&visibility=public)

<details>
<summary>Está com problemas? 🤷</summary><br/>

Ao copiar o exercício, recomendamos as seguintes configurações:

- Em owner, escolha sua conta pessoal ou uma organização para hospedar o repositório.

- Recomendamos criar um repositório público, pois repositórios privados consomem minutos do Actions.

Se o exercício não estiver pronto em 20 segundos, verifique a aba [Actions](../../actions).

- Veja se há um job em execução. Às vezes simplesmente demora um pouco mais.

- Se a página mostrar um job com falha, por favor abra uma issue. Muito bem, você encontrou um bug! 🐛

</details>

---

&copy; 2025 GitHub &bull; [Código de Conduta](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [Licença MIT](https://gh.io/mit)
