# Contexto e Motivação

Aplicativos de delivery são uns dos mais usados na sociedade atual, alguns se destacam pela boa usabilidade outros são complicados de usar
pra alguns usuários, pela grande demanda de apps de delivery hoje em dia, decidimos que a LLM deveria gerar uma base de dados sobre a 
**Satisfação de usuários em aplicativos de delivery**

## Atributos Preditores:

1- tempo_entrega (numérico, em minutos, entre 15 e 90)

2- comunicacao_entregador (numérico, escala de 1 a 5) - educação e clareza

3- atualizacoes_status (numérico, quantidade, entre 0 e 10) - notificações recebidas

4- facilidade_contato (categórico: facil, media, dificil) - para falar com suporte/entregador

5- resposta_suporte (numérico, em minutos, entre 0 e 30) - tempo para responder dúvidas

6- problema_resolvido (categórico: sim, nao, nao_houve) - se houve problema e foi resolvido

## Classe Alvo:

**satisfacao (Alta, Media, Baixa)**

regras:

* Alta: comunicacao_entregador >= 4 E atualizacoes_status >= 3 E (problema_resolvido = sim OU problema_resolvido = nao_houve)

* Baixa: comunicacao_entregador <= 2 OU facilidade_contato = dificil OU (problema_resolvido = nao)

* Media: todos os outros casos

**A classe-alvo escolhida foi satisfacao, do tipo multiclasse com três valores possíveis: Alta, Media e Baixa. Esta classificação permite capturar níveis intermediários de satisfação do usuário, proporcionando uma análise mais detalhada da experiência no aplicativo de delivery.**

