# ACTRA — Site WordPress (Hostinger)

Repositório para versionar e editar o tema/plugins do site **actra.com.br**, hospedado na Hostinger, com apoio do Claude Code.

## O que fica neste repositório

Só código próprio (tema customizado, plugins próprios, scripts). O core do WordPress, uploads e configurações sensíveis **não** são versionados (ver `.gitignore`).

Estrutura esperada:

```
wp-content/
  themes/
    <tema-actra>/
  plugins/
    <plugins-proprios>/
```

## Credenciais

- `HOSTINGER_API_TOKEN`: configurado como variável de ambiente no Environment do Claude Code (não fica no código).
- Acesso à rede do Environment liberado para `actra.com.br` e `www.actra.com.br`.

## Fluxo de trabalho

1. Pedir a alteração no Claude Code (ex: "ajusta o CSS do header").
2. Claude edita os arquivos do tema/plugin aqui no repo, commita e faz push.
3. Deploy para o Hostinger:
   - **Opção A (recomendada)**: Git integrado no hPanel da Hostinger, conectado a este repositório/branch — auto-deploy a cada push.
   - **Opção B**: deploy manual via SFTP/SSH.

## Pendências de configuração

- [ ] Confirmar se o plano Hostinger tem a opção **Git** no hPanel (Advanced → Git)
- [ ] Trazer os arquivos atuais do tema/plugins do servidor para este repositório
- [ ] Definir ambiente de staging (opcional, recomendado antes de ir para produção)
