---
title: Changelog
permalink: /changelog/
---

**[🏠 Início](/) · [📋 Farms](/farms/) · [🧪 Tanque de XP](/tanque-xp/) · [🧴 Frasco de Alma](/frasco-alma/) · [⚙️ Config](/config/) · [📜 Changelog](/changelog/) — [🇬🇧 English](/en/changelog/)**

# Changelog

## AFK Farms — v1.2.0

### Novidades

- **Tanque de XP** — novo bloco que armazena automaticamente o XP gerado por todas as Farms AFK do mesmo chunk. Não precisa encostar em cada farm individualmente — basta colocar em qualquer lugar do chunk que ele coleta de todas elas.
- Guarda até o equivalente ao **nível 30** de XP. Depois de cheio, o XP extra das farms é perdido até você coletar (igual a um baú lotado).
- Uma exibição flutuante acima do tanque mostra o **Nível** atual e uma barra de progresso até o próximo, e o vidro vai enchendo com um líquido verde conforme o XP acumula. Só aparece quando você está mirando no tanque e a até 8 blocos de distância.
- Três formas de usar, dependendo do que você está segurando ao clicar com o botão direito:
  - **Mão vazia** — absorve todo o XP guardado na hora, em níveis.
  - **Frasco de Vidro** — consome 1 frasco + XP do tanque e entrega um Frasco de Experiência (Bottle o' Enchanting).
  - **Item danificado com Remendo (Mending)** — repara a durabilidade do item instantaneamente usando o XP do tanque (mesma taxa do vanilla: 2 de durabilidade por 1 xp).
- **Receita do Tanque de XP** — 4 Lingotes de Ferro (cantos) + 4 Vidros (bordas) + 1 Frasco de Experiência (centro).

### Reformulação das Farms

- Todos os drops das farms foram refeitos pra bater com as **loot tables reais do vanilla**, extraídas direto dos dados do próprio jogo. Várias farms ficaram mais precisas (Bruxa agora solta corretamente 4-8 Redstone; Golem de Ferro sempre solta Lingote de Ferro E Papoula; Blaze não solta mais Pólvora de Blaze, já que isso nunca existiu no vanilla).
- **O item de ativação não dura mais pra sempre.** Cada farm tem um número limitado de usos no item de ativação (64 por padrão) e ele quebra quando acaba — você vai precisar repor, igual ao combustível. Dá pra desligar essa mecânica no config.
- **2 farms novas**: Breeze (Carga de Vento, na Farm AFK normal) e Wither Skeleton (Farm AFK do Nether — alimentada pelo novo Frasco de Alma, não por um item comum).
- Combustível agora é configurável por tipo: Carvão/Carvão Vegetal (60s/drop), Balde de Lava (30s/drop), e dois novos combustíveis de alto nível pros mobs mais difíceis do Nether — Pólvora de Blaze (15s/drop) e Estrela do Nether (5s/drop).
- **Novo `config.json`** permite ajustar tudo isso sem mexer em código: chance de drop, xp por drop, tempo de combustível, durabilidade, e até quais mobs existem.

### Frasco de Alma

- Pros mobs mais perigosos do Nether (começando pelo Wither Skeleton), um item de ativação simples não basta. Fabrique um Frasco de Alma vazio (Frasco de Vidro + Areia das Almas), carregue no inventário, e desfira o golpe fatal no mob de verdade — ele vira um Frasco de Alma preenchido daquele mob específico, que aí sim alimenta a farm no lugar de um item comum.
- O Frasco de Alma segue a mesma regra de durabilidade de qualquer item de ativação: cada um vale por um número limitado de ciclos de drop antes de esvaziar.
- O modelo do frasco troca sozinho entre a aparência vazia e uma versão brilhante cheia de essência assim que a alma é capturada.

### Correções

- Corrigido Esqueletos e Wither Skeletons no terrário da Farm AFK girando o braço errado em vez de mirar (Esqueleto) ou erguer a arma (Wither Skeleton) corretamente.
- O Guia das Farms agora cobre o Tanque de XP, o Frasco de Alma e a durabilidade dos itens, além de listar Breeze/Wither Skeleton nas tabelas de mobs.
- Corrigido a Farm AFK do Nether aceitando item de ativação de qualquer farm (ex: Couro fazendo aparecer uma Vaca lá dentro). Agora cada farm só funciona no bloco certo.

### 15 Farms Novas

**9 farms simples** — igual antes, só colocar o item de ativação no slot de cima:

| Mob | Item de ativação | Bloco |
|---|---|---|
| Zumbi | Carne Podre | Farm AFK |
| Husk | Areia | Farm AFK |
| Aranha da Caverna | Olho de Aranha Fermentado | Farm AFK |
| Lula | Saco de Tinta | Farm AFK |
| Lula Brilhante | Saco de Tinta Brilhante | Farm AFK |
| Cubo de Magma | Creme de Magma | Farm AFK |
| Fantasma | Membrana de Fantasma | Farm AFK |
| Tartaruga | Escama de Tartaruga | Farm AFK |
| Piglin Zumbi | Lingote de Ouro | Farm AFK do Nether |

**6 farms novas com Frasco de Alma** — as valiosas/perigosas. Um item comum não ativa essas; precisa de um **Frasco de Alma preenchido** daquele mob específico:

| Mob | Drop de destaque | Bloco |
|---|---|---|
| Afogado | Lingote de Cobre (~11%) | Farm AFK |
| Guardião | Fragmento/Cristal de Prismarine + Bacalhau | Farm AFK |
| Guardião Ancião | Igual ao Guardião + Esponja Molhada garantida | Farm AFK |
| Ghast | Lágrima de Ghast + Pólvora | Farm AFK do Nether |
| Shulker | Casco de Shulker (~50%) | Farm AFK do Nether |
| Hoglin | Costeleta + Couro | Farm AFK do Nether |

### 🚧 Próximas atualizações

- A definir
