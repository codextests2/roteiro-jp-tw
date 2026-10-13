# Japão & Taiwan — Travel Board

Site estático e responsivo, em português (PT-BR), para consulta do roteiro de dezembro de 2026. Funciona diretamente no navegador e no GitHub Pages, sem instalação, banco de dados, login ou bibliotecas externas.

## Experiência

- Dashboard com partida, destinos, duração e reservas pendentes.
- Roteiro diário com navegação por data e linha do tempo vertical.
- Atividades separadas visualmente em passeio, alimentação, transporte e hospedagem.
- Gestão de reservas, lista de compras, roteiro detalhado de Alishan e orçamento.
- Links de pesquisa no Google Maps, sem uso de API paga.
- Filtros por destino, categoria, prioridade e status.
- Backup JSON completo e exportação CSV da seção visível.
- Navegação inferior otimizada para celulares.

## Somente consulta

A página pública não permite adicionar, editar, excluir ou importar registros. Todas as alterações são feitas no código e publicadas no repositório pelo Codex. Datas, horários e reservas não confirmados permanecem identificados como pendentes.

Hotéis são identificados apenas de forma genérica por cidade ou região. Telefones, códigos de reserva, identificadores pessoais e valores financeiros privados não fazem parte da versão pública. Consulte também [PRIVACY.md](PRIVACY.md).

## Dados

O bloco `<script id="seed" type="application/json">` de `index.html` preserva o roteiro, os detalhes de Alishan e os custos originais. As listas de reservas e compras também ficam no mesmo arquivo, sem armazenamento externo.

O botão de backup gera uma cópia completa dos dados visíveis no código. Valores em JPY, TWD, BRL e USD são mantidos separados, sem conversão automática.

## Publicação

O site é publicado pela branch `main`, pasta raiz, em:

https://codextests2.github.io/roteiro-jp-tw/

O HTML usa `noindex, nofollow` para desencorajar indexação por mecanismos de busca. O endereço continua tecnicamente público para quem possuir o link.

## Referências de UX

O design usa padrões gerais observados em projetos de planejamento de viagem: dashboard, navegação por dia, linha do tempo, cartões de atividade, status e navegação móvel. Nenhum código dos projetos de referência foi copiado. `travel-planner` usa MIT; `turistar` usa AGPL-3.0; não foi possível confirmar uma licença no repositório `travel-itinerary-app`, portanto ele foi usado apenas como referência conceitual.

## Verificação

O HTML e o JavaScript são validados sintaticamente. Testes automatizados com Chrome cobrem as versões móvel (390 × 844) e desktop (1440 × 1000), navegação entre páginas, linha do tempo, datas, links do Google Maps e ausência de controles públicos de edição.
