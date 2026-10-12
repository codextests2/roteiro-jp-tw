# Japão & Taiwan — roteiro interativo

Página responsiva em português, baseada no roteiro de dezembro de 2026 da Monica. Funciona sem instalação e não depende de bibliotecas externas.

## Usar

Abra `index.html` no navegador, ou acesse a página depois de publicar no GitHub Pages.

- Roteiro e programação detalhada de Alishan.
- Busca, filtros por destino e planejamento.
- Adicionar, editar e excluir atividades ou custos.
- Notas de Alishan editáveis; orçamento antigo preservado em seção de referência.
- Totais de custos separados por moeda (JPY, TWD, BRL e USD), sem conversão automática.
- Salvamento automático no armazenamento local do navegador.
- Backup JSON completo, importação e exportação CSV por seção.

O navegador guarda as edições **somente naquele aparelho e naquela origem**. A página não altera arquivos do repositório nem a planilha. Para transferir as edições, baixe o backup no aparelho de origem e importe no outro. Limpar os dados do navegador pode remover as edições; mantenha um backup. Os dados iniciais só aparecem quando não há uma versão local salva.

Abrir como arquivo local pode restringir a persistência em alguns navegadores. A página informa quando não consegue salvar. Use o backup para conservar as alterações.

## Publicar no GitHub Pages

1. Crie um repositório ou selecione um existente para este roteiro. A conexão atual do ChatGPT precisa ter acesso ao repositório para enviar os arquivos diretamente.
2. Envie `index.html` e `.nojekyll` para a raiz do repositório. `README.md` é opcional.
3. Em **Settings → Pages → Build and deployment**, selecione **Deploy from a branch**, a branch que contém os arquivos (normalmente `main`) e **/(root)**. Salve.
4. Aguarde o GitHub mostrar o endereço da página. Abra esse endereço no celular ou computador.

Documentação oficial: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

A disponibilidade do Pages em repositórios privados depende do plano GitHub. O endereço publicado pode ser acessível ao público; o roteiro contém datas e hotéis. Repositório privado não significa automaticamente página privada.

## Atualizar dados iniciais no repositório

O bloco `<script id="seed" type="application/json">` dentro de `index.html` contém os dados iniciais. Para atualizar a versão para novos leitores, substitua esse JSON por um backup exportado (sem alterar a estrutura `version: 1`). Ao inserir manualmente, escape `<` como `\u003c` dentro do JSON para não encerrar a tag de script.

Uma edição feita na interface fica no navegador e não publica mudanças para outras pessoas. Sincronização automática entre aparelhos exige uma etapa adicional com login e armazenamento compartilhado.

## Verificação realizada

Código JavaScript validado sintaticamente e regras de dados verificadas: importação, datas, filtros, inserção, edição, exclusão, totais por moeda e proteção de exportação CSV. Sem dependências externas, tokens ou credenciais no projeto. A interface não foi testada em navegador nesta sessão.
