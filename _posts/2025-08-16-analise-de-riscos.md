---
layout: post
title: "Análise de riscos."
date: 2025-08-16 12:00:00 +0000
categories: [Governança de TI, Estratégia, Documentação]
tags: [Governança de TI, análise de riscos, gestão de riscos]
description: "Você sabe a importância da Gestão de Riscos?"
image: image: /assets/img/governanca/layout2.png
---

A capacidade de entender e medir os riscos que podem afetar a integridade da nossa vida foi o que definitivamente nos trouxe até aqui. E norteia a nossa sobrevivência, pois exatamente tudo envolve um certo grau de risco: *dirigir, sair na rua de madrugada, subir em uma árvore, fazer um investimento, decidir mudar de profissão, atravessar a rua*, enfim, riscos que fazem parte do nosso cotidiano como seres humanos, onde precisamos constantemente medir para garantir a nossa sobrevivência. 

Porém, de forma semelhante em um contexto empresarial medir todo o tipo de risco também é uma forma de garantir a sobrevivência dela, e hoje vou resumir sobre como foi a minha experiência criando um documento de Gestão de Riscos parte de um dos vários documentos de um cronograma de Governança de TI que estou desenvolvendo.

Para entender de fato tudo que envolve o conceito de risco, precisamos entender alguns outros termos que permeiam e fazem parte da análise de riscos, é importante entender para que possamos ser mais assertivos ao gerencia-los. O Risco em si trata-se da possibilidade ou a probabilidade de um evento adverso ocorrer e afetar negativamente os ativos críticos e estratégicos de uma empresa. E o **Risco** advém de uma **ameaça** que fica pairando à espreita procurando uma **vulnerabilidade**. A **vulnerabilidade** por sua vez é o ponto fraco de um ambiente ou sistema que será explorado pela ameaça.

A ameaça é a causa potencial de um incidente indesejado, que pode resultar em danos para um sistema, operação ou ambiente organizacional. A ameaça pode ser algo que ainda nem conhecemos *(como foi o caso da pandemia)* que engloba: desastres naturais, erros humanos, falhas em hardwares, e o mais comum atualmente: ataques cibernéticos.

Então ao analisar esses variados riscos *(claro que vamos considerar todo o contexto da empresa, onde cada uma tem o seu)* devemos pensar no **impacto**, outro termo importantíssimo na Gestão de Riscos, que nada mais é que o resultado de um evento de risco. O que irá impactar? O impacto é o grau do dano e consequências para a empresa caso a ameaça encontre a vulnerabilidade perfeita e se concretize. Os impactos vão desde perdas financeiras até a reputação da empresa.

E para entrar em contraste com o impacto para medir o nível de criticidade de determinado risco, temos a **probabilidade** que pode ser referenciada em porcentagens de 0% a 100%, (ou para uma análise mais simples de 1 a 5 já é suficiente). Para ilustrar melhor vou deixar uma imagem da que eu recriei utilizando referências de uma matriz de risco encontrada na internet obviamente. A **Matriz de Risco** é outro ponto importante, a partir dela podemos fazer uma análise visualmente mais palpável, além de ser mais rápida (de certa forma) também.

A que usei como referência é a *Matriz de Risco HFMEA (Healthcare Failure Mode and Effects Analysis)* muito utilizada na área da saúde, tornando-a muito mais completa trazendo um aspecto importantíssimo que é a "detectabilidade": a facilidade em detectar um risco ou uma falha, pois na grande maioria dos casos estamos avaliando sistemas, e em sistemas pode haver alguns riscos ocultos e precisamos ter a capacidade de **detecta-lo** o quanto antes, se não, o vazamento de água vai acontecendo e só vamos perceber quando o teto cair.

![Matriz de Risco](/assets/img/governança/Matriz-de-risco.png)

Outra coisa que achei bem interessante é que durante a análise de risco utilizando essa referência, temos um outro lado da matriz onde podemos identificar potenciais oportunidades. O que pode elevar o nível estratégico da empresa.

Após entender tudo isso e fazer o cruzamento entre impacto e probabilidade conseguimos dar um nível de criticidade ao risco, e dependendo do nível vamos decidir então como trata-los. Percebe que podemos aqui realizar uma tomada de decisão mais embasada, com base no nível criticidade? Dando assim prioridade principalmente para os riscos obviamente mais críticos. 

![Matriz de Risco-detalhes](/assets/img/governança/detalhes1.png)

![Matriz de Risco-detalhes](/assets/img/governança/detalhes2.png)

E para trata-los, aqui entra também algumas estratégias que dependem também do contexto da empresa e o seu apetite ao risco (Nível de risco que a empresa está disposta a aceitar para atingir seus objetivos).

A empresa pode escolher entre:
- **Mitigar o risco:** Implementando controles e ferramentas pra reduzir as probabilidades e os impactos de um determinado risco, como por exemplo a segurança em camada, entre muitos outros...
- **Aceitar:** Isso acontece geralmente quando os custos para mitigar e tratar excedem os custos do impacto. Essa ação com certeza é documentada e assinada formalmente.
- **Transferir:** Geralmente uma empresa terceira é colocado em jogo, como seguradoras etc...
- **Evitar:** Simplesmente eliminar a atividade que origina o risco. bastante radical mas possível caso o risco seja muito alto e origina-se de algo irrelevante para o funcionamento geral da empresa.

Lembrando que essa análise deve ser feita em novos projetos, ao implementar mudanças, nas operações diárias, ou para simplesmente entender melhor a sua postura de segurança com os processos organizacionais como um todo, ou seja: indispensável para que a empresa possa evoluir de forma segura e amplamente consciente dos potenciais riscos que a cercam, e que definitivamente definem a sua sobrevivência.