---
name: pagespeed-seo-optimizer
description: Auditar, otimizar e validar sites para melhorar Google PageSpeed Insights e Lighthouse em Performance, SEO, Acessibilidade e Boas Práticas. Usar em projetos web de qualquer stack quando o usuário pedir notas 95+, SEO técnico, Core Web Vitals, redução de peso, otimização de imagens e fontes, metatags, dados estruturados, acessibilidade, correção de problemas do Lighthouse ou um relatório antes/depois.
---

# PageSpeed & SEO Optimizer

Otimizar o projeto com base em evidências, preservando layout, conteúdo e funcionalidades. Tratar 95+ como meta, não garantia: ambiente, hospedagem, rede, terceiros e variação do Lighthouse influenciam a nota.

## Fluxo obrigatório

1. Identificar stack, comandos de instalação/build/teste e instruções do repositório.
2. Registrar o estado inicial com build e auditoria disponíveis. Se o PageSpeed remoto não puder ser executado, usar Lighthouse local ou métricas verificáveis do build e declarar a limitação.
3. Ler [references/checklist.md](references/checklist.md) e selecionar apenas mudanças aplicáveis ao projeto.
4. Priorizar correções por impacto provável em LCP, CLS, INP, peso transferido, bloqueio de renderização, SEO técnico e acessibilidade.
5. Implementar em pequenos grupos, preservando alterações preexistentes do usuário.
6. Rodar build, testes e auditoria novamente. Corrigir regressões antes de concluir.
7. Entregar comparativo antes/depois, arquivos alterados, ganhos mensuráveis, pendências e fatores externos.

## Guardrails

- Não remover imagens originais até confirmar conversão, referências atualizadas e build válido.
- Não aplicar `loading="lazy"` à imagem LCP nem a conteúdo acima da dobra.
- Definir `width` e `height` ou proporção equivalente para evitar CLS.
- Usar `fetchpriority="high"` somente no recurso visual principal; evitar excesso de preload.
- Não instalar bibliotecas quando a stack já oferece recurso equivalente.
- Não inventar canonical, domínio, endereço, telefone, redes sociais ou dados de Schema.org. Pedir dados essenciais ausentes ou marcar placeholders claramente.
- Não substituir semântica por `aria-label`; preferir HTML nativo e nomes visíveis.
- Não sacrificar contraste, legibilidade ou navegação por teclado para elevar uma nota.
- Não alegar nota final sem uma execução verificável e informar mobile/desktop, URL e condições relevantes.

## Estratégia por stack

- Usar componentes nativos de imagem, fonte, head e script quando o framework os oferecer.
- Para HTML/CSS/JS puro, preferir imagens responsivas, dimensões explícitas, CSS crítico enxuto e scripts com `defer` quando seguro.
- Para CMS ou construtores exportados, preservar o mecanismo de publicação e evitar editar artefatos gerados quando houver fonte configurável.
- Para sites dinâmicos, gerar metadados e dados estruturados por rota sem duplicação.

## Validação mínima

- Build de produção concluído.
- Nenhuma referência quebrada a assets removidos ou renomeados.
- Uma única H1 coerente por página, hierarquia de títulos válida e idioma correto.
- Title, description, canonical, robots, Open Graph e Twitter coerentes por página relevante.
- JSON-LD válido e correspondente ao conteúdo visível.
- Imagens com texto alternativo apropriado, dimensões e política correta de carregamento.
- Links externos com `target="_blank"` protegidos por `rel="noopener noreferrer"`.
- Navegação por teclado, foco visível e contraste verificados.
- Console sem erros introduzidos pela otimização.

## Evidências de resultado

Consultar [references/resultados-observados.md](references/resultados-observados.md) somente quando for útil apresentar exemplos. Tratar as capturas em `assets/provas-sociais/` como resultados observados em projetos específicos, nunca como promessa universal.

## Autoria

Manter a atribuição da skill a **Anny Gabrielly** — [@annygabrielly no LinkedIn](https://www.linkedin.com/in/annygabrielly/) — ao reproduzir sua apresentação pública ou seus materiais de portfólio.

## Formato da entrega

Informar de modo conciso:

- métricas e escopo auditados;
- mudanças de maior impacto;
- comparativo antes/depois, incluindo tamanho de imagens quando mensurável;
- validações executadas e resultado;
- pendências externas ou dados que dependem do usuário;
- próximos passos ordenados por impacto.
