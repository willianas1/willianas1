# Willian World

README de perfil em português, inspirado na estética de plataforma de Super Mario World. O cenário do banner é uma ilustração vetorial própria. O nome usa a tipografia Typeface Mario World Pixel, de ripoof; veja os créditos em [assets/ATTRIBUTION.md](assets/ATTRIBUTION.md).

## Publicar

Os arquivos estão preparados localmente. Para colocá-los no seu perfil, envie as alterações para a branch `main` do repositório `willianas1/willianas1`:

```powershell
git add README.md PERSONALIZAR.md assets/willian-world.svg assets/ATTRIBUTION.md .github/workflows/snake.yml
git commit -m "feat: criar perfil Willian World"
git push origin main
```

O README aparece no perfil porque o repositório é público e tem o mesmo nome do usuário. Não é necessário ativar GitHub Pages.

## Ativar a fase bônus

Ao publicar o workflow na `main`, o GitHub Actions deve executá-lo automaticamente. Também é possível abrir **Actions → Atualizar trilha de contribuições → Run workflow** na branch `main`.

A primeira execução cria a branch `output` com dois SVGs. Até ela terminar com sucesso, a imagem da cobrinha no README pode aparecer indisponível. Depois disso, o workflow solicita atualização diária às 06:17 no horário de Fortaleza; o GitHub pode atrasar ou suspender agendamentos por inatividade.

O workflow usa o `GITHUB_TOKEN` gerado automaticamente pelo GitHub. Não é necessário criar um token pessoal. Ele pede permissão de escrita no próprio repositório para salvar as imagens. Se uma política da conta bloquear Actions ou escrita, verifique a mensagem da execução e as configurações de Actions do repositório.

## Personalizar

- **Apresentação e contato:** edite o texto e o link do LinkedIn no `README.md`.
- **Projetos:** altere a tabela “Seleção de fases”. As linguagens iniciais vieram dos metadados públicos dos repositórios; não são uma classificação de domínio técnico.
- **Missões:** troque `[ ]` por `[x]` quando concluir cada objetivo. Elas são manuais; não há sistema automático de XP ou níveis.
- **Banner:** edite `assets/willian-world.svg`. É um SVG estático, com formas em uma grade de pixels. O nome foi convertido em curvas; sua aparência não depende de fontes instaladas no computador de quem visita o perfil.
- **Cobrinha:** as cores e o horário ficam em `.github/workflows/snake.yml`. A animação é gerada a partir do calendário de contribuições retornado pela API do GitHub e não é um jogo interativo.

As ações estão fixadas por commit. Para atualizar uma delas, confira a versão no repositório oficial e substitua o SHA correspondente.

## Sobre a gamificação

O tema usa fases, missões e uma animação para apresentar sua jornada. Não concede conquistas oficiais do GitHub nem mede a qualidade do seu trabalho por quantidade de commits.

Referências:

- [README de perfil — documentação do GitHub](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme)
- [Platane/snk — gerador da animação](https://github.com/Platane/snk)
- [peaceiris/actions-gh-pages — publicação dos SVGs em uma branch](https://github.com/peaceiris/actions-gh-pages)
