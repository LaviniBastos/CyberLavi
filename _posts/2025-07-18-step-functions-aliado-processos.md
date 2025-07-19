---
layout: post
title: "Step Functions como aliado nos processos de execução."
date: 2025-07-18 20:00:00 +0000
categories: [AWS, Lambda, Serverless]
tags: [step-functions, aws, serverless, lambda, arquitetura]
description: "Como o AWS Step-Functions pode ajudar a orquestrar processos serverless com eficiência e visibilidade."
---

Estou me preparando para a certificação AWS Developer e, para consolidar os conhecimentos, venho praticando com laboratórios utilizando as principais ferramentas da AWS focadas no desenvolvimento seguro e escalável.

Recentemente, decidi testar o funcionamento do **Step Functions** na prática em um fluxo bem simples e o resultado me surpreendeu.

### Estrutura inicial do Lab

- Criei **duas roles IAM**:
- Uma para as **três funções Lambda** que compõem o processo
- E outra específica para o **Step Functions**, para garantir a permissão de execução correta.

O Step Functions foi utilizado como o **orquestrador** que ele é, centralizando o fluxo da lógica de negócio. O mais interessante foi observar na prática como ele consegue controlar o caminho de execução, tratando **sucesso**, **falha** e até mesmo caminhos alternativos.

Claro que para isso eu escolhi utilizar um código JSON para entender melhor como cada step são declaradas, mas podemos apenas selecionar os serviços e arrastar, montando o fluxo visualmente.

### Benefícios percebidos

Além da facilidade de implementação, notei os seguintes pontos positivos:

- **Visibilidade do fluxo**: Cada transição e estado são registrados.
- **Depuração facilitada**: Identificação rápida de falhas ou gargalos.
- **Escalabilidade**: Essencial em ambientes serverless, onde coordenação entre funções desacopladas é vital.
- **Performance**: O processamento foi feito em **nanosegundos**, achei incrível!


> Foi uma experiência muito bacana, acho importantíssimo aplicar o conhecimento teórico, porque ler sobre o funcionamento do serviço é bem diferente de vê-lo acontecendo, e melhor... Fazendo ele acontecer, quando ouvi falar do Step Functions a primeira vez durante os estudos para tirar a certificação Cloud Practitioner, já achei bastante interessante, agora então... Mudou completamente minha percepção sobre orquestração em ambientes distribuídos.

---

### Algumas evidências do Lab

**O fluxo funcionando:**

![Step Functions Exemplo](/assets/img/cloud/StepFunctions1.png)
![Step Functions Exemplo](/assets/img/cloud/StepFunctions2.png)
![Step Functions Exemplo](/assets/img/cloud/StepFunctions3.png)