# Checklist técnico

Use como roteiro adaptável, não como substituto da análise do projeto.

## Imagens

- Converter PNG/JPG fotográficos para WebP ou AVIF quando houver ganho real.
- Manter SVG para vetores e transparências simples quando mais eficiente.
- Atualizar todas as referências antes de remover originais.
- Não aplicar lazy loading à imagem LCP; aplicá-lo às imagens abaixo da dobra.
- Definir dimensões ou aspect-ratio e usar `srcset`/`sizes` quando necessário.
- Priorizar somente o recurso principal acima da dobra.
- Criar imagem social 1200 × 630 quando o projeto exigir compartilhamento.

## Fontes e CSS

- Preferir WOFF2, `font-display: swap` e apenas famílias, pesos e subsets usados.
- Evitar CSS e animações que provoquem layout ou pintura excessiva.
- Usar CSS para animações contínuas simples e respeitar `prefers-reduced-motion`.
- Aplicar `will-change` apenas perto da animação e removê-lo quando desnecessário.
- Remover CSS não utilizado somente com validação visual e funcional.

## JavaScript e terceiros

- Remover dependências e código não utilizados.
- Dividir ou adiar código que não seja necessário na carga inicial.
- Usar `defer`/`async` de acordo com dependências e ordem de execução.
- Medir scripts de analytics, chat, mapas, fontes e widgets antes de alterá-los.
- Preservar consentimento, analytics e integrações essenciais.

## HTML e acessibilidade

- Definir `lang`, landmarks e hierarquia H1 → H2 → H3.
- Usar HTML semântico, labels associados e controles nativos.
- Escrever `alt` descritivo para conteúdo e `alt=""` para decoração.
- Garantir foco visível, teclado, nomes acessíveis e contraste WCAG AA.
- Manter alvos de toque adequados e evitar conteúdo inacessível em hover.

## SEO técnico

- Title único e descritivo, normalmente até cerca de 60 caracteres.
- Description útil e específica, normalmente entre 120 e 160 caracteres.
- Canonical absoluto e coerente com a URL pública.
- Robots adequado ao ambiente; nunca indexar preview ou staging por acidente.
- Sitemap e robots.txt coerentes quando aplicáveis.
- Open Graph e Twitter Card completos, com imagem absoluta e texto alternativo.
- Favicons, apple-touch-icon e theme-color.
- JSON-LD com tipo compatível com o negócio e apenas dados verdadeiros.
- Conteúdo rastreável, links internos claros e ausência de duplicação evitável.

## Segurança e qualidade

- HTTPS e ausência de mixed content.
- `rel="noopener noreferrer"` em links externos com nova aba.
- Dependências sem vulnerabilidades conhecidas relevantes.
- Sem erros novos no console, links quebrados ou falhas de build.
- Cabeçalhos de segurança avaliados conforme a hospedagem.

## Relatório final

- Informar ambiente, rota, modo mobile/desktop e ferramenta usada.
- Separar medição observada de estimativa.
- Listar arquivos adicionados, modificados e removidos.
- Comparar bytes antes/depois para assets otimizados.
- Explicar itens não aplicados e fatores externos que limitam a nota.
