# GIGGER CRM — PWA offline

Aplicativo web instalável (PWA) para músicos, bandas, produtores e empresários organizarem a venda de shows. Ele é responsivo para computador e celular, funciona offline depois da primeira abertura e guarda os dados no navegador do usuário via IndexedDB.

## Já implementado

- Painel com contratantes, oportunidades abertas, cachê em negociação e follow-ups.
- Cadastro/edição de contratantes.
- Funil Kanban de oportunidades para shows.
- Agenda básica baseada em follow-ups e datas de show.
- Limite Free: **10 contratantes** e **10 oportunidades abertas**.
- Versão Pro (estrutura de interface; a licença segura deve ser concluída antes da venda).
- Backup local `.giggerbackup` e restauração.
- PWA instalável, cache offline e layout para celular.
- GitHub Action incluída para publicar no GitHub Pages.

## Publicar gratuitamente no GitHub Pages

1. Crie uma conta em [GitHub](https://github.com) e um repositório novo, por exemplo `gigger-crm`.
2. Escolha **Private** enquanto estiver desenvolvendo. Para usar GitHub Pages gratuitamente na conta pessoal, talvez seja necessário tornar o repositório público, conforme a disponibilidade/configuração da conta.
3. Envie todos os arquivos desta pasta à raiz do repositório.
4. No GitHub, abra **Settings → Pages**.
5. Em **Build and deployment**, selecione **GitHub Actions**.
6. Faça um `push` na branch `main`. O workflow `.github/workflows/pages.yml` publicará o app.
7. Em alguns minutos, a URL do app aparece em **Settings → Pages** e também na aba **Actions**.

## Como usar

- Primeira abertura: exige internet para carregar o app e registrar o cache.
- Depois: o usuário pode instalar pelo navegador (botão `Instalar app`) e usar offline.
- Dados: ficam somente no navegador/dispositivo usado.
- Segurança: exporte backup regularmente em Configurações. Limpar os dados do navegador sem backup elimina os cadastros locais.

## Antes de vender a versão Pro

A ativação atual está propositalmente marcada como demonstração e salva uma chave local simples. Antes de comercializar, implemente licença criptografada com assinatura digital assimétrica: uma ferramenta privada gera as licenças com a chave privada e o PWA valida com chave pública. Não coloque chaves privadas no repositório nem no navegador.

## Limitação sem servidor

Sem nuvem, notebook e celular não se sincronizam automaticamente. Para mudar de dispositivo, o usuário deve exportar e importar o arquivo de backup. Isso atende à proposta offline e sem custo de hospedagem.
