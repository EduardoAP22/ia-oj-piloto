# IA-OJ Piloto — Guia do Testador (v1.0)

**Protótipo funcional das 5 funções do MVP** — Assistente Inteligente do Oficial de Justiça.
Piloto independente, **dados 100% sintéticos**, uso restrito a servidores federais.

---

## O que você vai testar

| Função do MVP | Onde no app |
|---|---|
| 1. Leitor/checklist de mandados | Aba **Central** → abrir mandado |
| 2. Fila operacional inteligente | Aba **Central** (ordenada por prazo) |
| 3. Gravador de diligência (voz) | Tela da diligência → 🎤 botão vermelho |
| 4. Gerador de certidão | "Salvar e gerar certidão" |
| 5. Validador antes do protocolo | Botão "Validar minuta" |

## Instalação (2 minutos, sem custo)

### Opção A — no computador
1. Descompacte a pasta `iaoj_piloto`
2. Abra o arquivo `index.html` no **Chrome** ou **Edge**
3. Pronto. Os dados ficam salvos no próprio navegador

### Opção B — no celular (recomendado para testar a voz)
1. Hospede a pasta em qualquer host estático gratuito (GitHub Pages, Netlify Drop — arrastar e soltar)
2. Abra o link no **Chrome do Android**
3. Menu ⋮ → **"Adicionar à tela inicial"** → o app instala como aplicativo
4. O microfone (ditado) funciona direto no Chrome Android

> Cada testador usa a **sua própria cópia** — os dados ficam no dispositivo de cada um (local-first). Nada é enviado a servidor algum.

## Roteiro de teste (30 min por testador)

1. **Config** → preencha seu nome e matrícula (para a assinatura)
2. **Central** → "Gerar 12 mandados sintéticos"
3. Abra o mandado mais urgente → confira o **checklist da diligência**
4. "Iniciar diligência" → selecione o resultado → **dite o relato** (botão 🎤) ou digite
5. "Salvar e gerar certidão" → leia a minuta
6. **"Validar minuta"** → veja os apontamentos do validador
7. Corrija se necessário → **assine** → baixe o pacote
8. Faça isso com **pelo menos 5 mandados**, variando os resultados (positivo, negativo, recusa, fechado…)
9. Teste também a **ponte Adapta One**: na certidão, botão 🤖 "Refinar com Adapta One" → copie o prompt → cole no Adapta → cole a resposta → **"Auditar"** (respostas com fatos inventados são rejeitadas!)
10. Ao final: aba **Relatório** → **"Exportar JSON"** → envie o arquivo ao coordenador do piloto

## Regras do piloto

- 🧪 **Somente dados fictícios** — nunca insira número de processo, nome ou endereço reais
- 🔒 No piloto, **nenhum documento vai ao PJe** — modo sombra: o trabalho real continua como sempre
- 📝 Anote toda correção que você fizer numa minuta — é o dado de qualidade do piloto
- ⚠️ Sugestões do app (fila, prioridade) são **auxiliares** — a ordem das diligências é sempre sua

## Métricas coletadas automaticamente

O app registra: tempo de cada etapa, minutas geradas × aprovadas sem correção, apontamentos do validador, completude média, resultados por tipo e trilha de auditoria completa. O JSON exportado alimenta o relatório final do piloto para apresentação institucional.

**Dúvidas?** Coordenação do piloto — IA-OJ · Justiça Federal
