# Bora Correr

**Do sofá à linha de chegada, um treino de cada vez.**

👉 **Teste aqui:** https://jotadablio.github.io/bora-correr/ (melhor no celular)

---

## A ideia

Muita gente quer correr uma prova e trava logo no começo. Não sabe por onde começar, acha que precisa estar em forma antes de tentar ou começa animada, exagera na primeira semana e desiste com a canela doendo.

Também tem quem até corre, mas sem constância. A semana aperta, um treino vira dois, depois três, e quando vê já passou um mês.

O Bora Correr é a minha tentativa de resolver isso do jeito que o Duolingo resolveu para idiomas. Os treinos são curtos, há um plano claro, cada dia cumprido vira uma pequena vitória e existe uma ofensiva que dá vontade de não quebrar. Você escolhe a meta (2, 5, 10 ou 21 km), diz quantos dias por semana consegue treinar e quando é a prova. O app monta um calendário até lá, que vai se ajustando conforme você conta como foi cada treino.

Ainda **não é um app de verdade**. É um protótipo de uma página só, feito para eu colocar na mão de pessoas reais e descobrir se a ideia funciona antes de investir no desenvolvimento.

## Se você veio testar, obrigado! 🧡

Leva uns 5 minutos:

1. Abra o link no celular e escolha uma meta. Pode ser a sua meta de verdade, se tiver uma.
2. Responda as perguntas e veja o plano que aparece.
3. Coloque o Bora na tela inicial do celular (o próprio app mostra como). Assim ele abre como um aplicativo.
4. Registre o treino de hoje com um dos três botões do semáforo.
5. Quer ver o plano se adaptando sem esperar semanas? Toque no ícone de ajustes (canto superior direito) e use **+1 dia** / **+7 dias** para avançar no tempo.

Se você topar seguir o plano de verdade, melhor ainda. Depois do terceiro treino o app faz 3 perguntinhas rápidas, e essa é a resposta que eu mais quero ler.

Depois, eu adoraria saber:

- O plano pareceu possível de cumprir? Ou assustou?
- Registrar o treino foi rápido e óbvio?
- A ofensiva e os pontos dariam vontade de voltar no dia seguinte?
- O que você sentiu falta? O que sobrou?

Pode me responder por onde você recebeu o link ou [abrir uma issue aqui](../../issues). Crítica sincera vale mais que elogio.

## Como o plano funciona

Por enquanto não tem inteligência artificial. São regras fixas, pensadas para não machucar ninguém:

- **Quem nunca correu começa alternando corrida e caminhada** (1 minuto correndo, 2 andando) e sobe um degrau por semana, até conseguir correr direto.
- **O tempo total da semana cresce no máximo 10%.** É uma regra clássica para evitar lesão por excesso.
- **Nunca dois treinos puxados em dias seguidos.** Para iniciantes, sempre tem pelo menos um dia de descanso entre um treino e outro.
- **A última semana antes da prova é mais leve** (o famoso polimento), e a véspera é sempre descanso.
- **Se o prazo for curto demais para a meta**, o app avisa com jeitinho e muda o objetivo para *completar a prova alternando corrida e caminhada*. Terminar a primeira prova já é uma vitória enorme.

E quem fez anamnese marcando problema cardíaco recebe um aviso para buscar liberação médica antes de começar.

### O semáforo

Depois de cada treino, um toque:

| | Significa | O que acontece |
|---|---|---|
| 🟢 | Fiz bem | O plano segue normalmente |
| 🟡 | Fiz, mas no limite | Também conta! Dois amarelos seguidos fazem a semana seguinte repetir o nível atual |
| 🔴 | Faltei | O treino se repete no próximo dia de treino |
| 🔴 | Tentei e não consegui | O plano volta um nível para você ganhar confiança |

### Pontos, ofensiva e conquistas

Aqui o que conta é **aparecer**, não correr muito.

- **Ofensiva:** quantos treinos seguidos você cumpriu. Dia de descanso não quebra, só faltar num dia de treino.
- **Pontos:** verde e amarelo valem o mesmo (10). O amarelo pontua de propósito, porque ouvir o corpo também é treino. Tentar e não conseguir vale 5. Semana completa ganha bônus de 20.
- **Conquistas:** primeiro treino, primeira semana completa, metade do caminho e dia da prova.

## Coisas técnicas (curtas)

- É um único `index.html`, sem build, sem framework, sem servidor. Junto vêm o manifesto, os ícones e um service worker para ele funcionar como app na tela inicial (e abrir mesmo sem internet).
- Seu plano fica **só no seu celular** (localStorage). Se limpar os dados do navegador ou trocar de aparelho, ele some.
- Para rodar localmente, basta abrir o `index.html` no navegador.

### Sobre os dados de uso

Para descobrir se a ideia funciona, o protótipo registra **de forma anônima** o que acontece nele: telas vistas, meta escolhida, treinos marcados no semáforo e as respostas da pesquisa. Uso o [PostHog](https://posthog.com) para isso.

O que **não** sai do seu celular: nome, e-mail, peso e problemas de saúde. A idade vai só como faixa (30-39, por exemplo). Dá para desligar a qualquer momento em *Ajustes → Dados de uso anônimos*.

Quando alguém usa o botão de avançar dias, os eventos vão marcados como `data_simulada`, para não misturar teste com uso real.

## Aviso importante

Este é um protótipo para testar uma ideia de produto. **Não substitui orientação médica nem de um profissional de educação física.** Se você tem alguma condição de saúde, converse com seu médico antes de começar a correr.

---

Feito com tênis velho e muita vontade de ver mais gente cruzando a linha de chegada. 🏁
