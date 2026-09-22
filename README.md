# Fernando Brum Advogados Associados — landing page

Site de página única do escritório, em <https://fernandobrumadvassociados.com.br/>.

Direito rural e agrário. Sede em Santo Ângelo/RS, atuação no RS, SC, PR, GO, DF e BA.
OAB/RS 458.

## Arquivos

| Arquivo | O que é |
|---|---|
| `index.html` | a página inteira: CSS, JavaScript e as duas fotos embutidas em base64. Não depende de pasta de assets nem de build. |
| `og-capa.jpg` | capa 1200×630 para a prévia de link do WhatsApp, Facebook, LinkedIn e Google. A página não a carrega. |

Não há dependências, `package.json` nem etapa de build. A Vercel serve os dois
arquivos estáticos direto da raiz.

## Como editar

Abra o `index.html` em qualquer editor. O topo do arquivo traz um comentário com
os pontos que costumam mudar (telefone, domínio) e onde cada um aparece.

O telefone atual é **(55) 99698-7100** — internacional `5555996987100` — e aparece
em 5 lugares: os 3 botões de WhatsApp, o link `tel:` do rodapé, a constante
`WHATSAPP` no `<script>` e o JSON-LD.

Se o domínio mudar, procure por `fernandobrumadvassociados.com.br`: são 6
ocorrências funcionais (canonical, `og:url`, `og:image`, `twitter:image` e os
campos `url` e `image` do JSON-LD).

## Decisões que não são óbvias no código

- **Arquivo único.** As fotos estão em base64 para a página abrir por duplo
  clique, sem servidor. Foi um requisito do projeto e ficou mantido.
- **Sem animação em loop.** O reveal ao rolar acontece uma vez por elemento e o
  observer é desconectado. `prefers-reduced-motion` desliga tudo.
- **Sem JavaScript nada desaparece.** O estado inicial do reveal só é aplicado
  quando a classe `.js-enabled` existe, e os `href` dos botões estão escritos no
  HTML, não montados pelo script.
- **Provimento 205/2021 da OAB.** O texto é informativo: sem promessa de
  resultado, valores, depoimentos, superlativos ou urgência comercial. Qualquer
  alteração de copy precisa respeitar isso.
