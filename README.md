[README.md](https://github.com/user-attachments/files/35211949/README.md)
# Teste – Espiritualidade · versão 0.2

## Conteúdo
- `index.html`: página interativa, responsiva e em português brasileiro.
- Questionário original preservado: 30 afirmações Likert + 6 questões complementares.
- Aprofundamento adaptativo: seleciona perguntas adicionais conforme respostas e afinidades preliminares.
- Mapa comparativo: tradições religiosas, correntes filosóficas/metafísicas, perspectivas não religiosas e espiritualidades independentes.
- Resultado local: dimensões descritivas, afinidades indicativas, explicações, pontos de aproximação e possíveis divergências.
- Exportação: copiar e baixar a síntese em texto.

## Como testar
Abra `index.html` em um navegador moderno. As respostas ficam na sessão da página e não são enviadas a um banco de dados.

## Publicação pública
Para disponibilizar por um endereço público, publique o arquivo `index.html` em um serviço de hospedagem de páginas estáticas (por exemplo, GitHub Pages, Netlify ou Cloudflare Pages). Esta entrega não cria nem registra um domínio e não publica o site automaticamente.

## Modalidade híbrida: estado desta versão
A versão 0.2 já inclui análise determinística local e o ponto de integração opcional com IA (`window.ANALYSIS_ENDPOINT`). A análise generativa ainda não está ativada: requer um endpoint de servidor próprio.

O endpoint deve:
1. Receber `POST` JSON com `answers`, `deepAnswers`, `scores`, `affinities`, `instrument` e `version`.
2. Validar e limitar o tamanho dos dados recebidos.
3. Chamar o modelo de IA no servidor, nunca diretamente do navegador.
4. Manter a chave da API em variável de ambiente no servidor.
5. Retornar JSON no formato `{ "analysis": "texto da análise" }`.
6. Não armazenar respostas pessoais por padrão; se houver armazenamento, informar finalidade, retenção e obter consentimento apropriado.

Para ativar a integração depois de publicar, configure `window.ANALYSIS_ENDPOINT` no arquivo antes do script principal, apontando para a URL HTTPS do endpoint seguro. Não coloque chaves ou segredos no HTML.

## Limites metodológicos
- O questionário é exploratório, não é teste psicológico, diagnóstico ou instrumento psicométrico validado.
- Os índices de afinidade são heurísticos e servem para comparação orientativa; não representam probabilidade de pertencimento, identidade ou verdade religiosa.
- As tradições são internamente diversas. As descrições são introdutórias e não substituem estudo das tradições nem diálogo com seus praticantes.
- A página não afirma que “energia universal”, cura energética ou influência mental à distância tenham comprovação científica.
- Uma afinidade parcial não implica adesão, e baixa afinidade não significa incompatibilidade absoluta.
