# Análise de Gerenciamento de Memória no Windows

## Sobre o projeto

Este projeto apresenta uma análise prática do gerenciamento de memória no Windows, realizada como atividade acadêmica durante o curso de Tecnólogo em Cibersegurança.

O experimento teve como objetivo observar o comportamento da memória do sistema em duas situações: com o computador em estado inicial e após o aumento da carga de trabalho por meio da abertura de programas e várias abas do navegador.

## Objetivo

- Observar o uso da memória RAM no Windows;
- Comparar o estado do sistema antes e depois do aumento da carga;
- Identificar os processos que mais utilizavam memória;
- Observar o comportamento da memória confirmada;
- Relacionar a prática aos conceitos de paginação, segmentação e swapping;
- Avaliar o impacto do gerenciamento de memória no funcionamento do sistema.

## Ambiente e ferramentas

**Sistema operacional:** Windows  
**Memória RAM:** 16 GB  
**Ferramenta principal:** Gerenciador de Tarefas  
**Navegador utilizado:** Brave Browser

Durante a análise, foram observados indicadores como memória em uso, memória disponível, memória confirmada, uso da CPU e uso do disco.

## Metodologia

O experimento foi dividido em duas etapas.

### 1. Estado inicial

Primeiramente, foram registrados os indicadores de memória com o sistema em uma condição de uso normal.

Foram observados:

- Memória RAM em uso;
- Memória disponível;
- Memória confirmada;
- Processo que mais utilizava memória;
- Uso da CPU;
- Uso do disco.

### 2. Aumento da carga

Em seguida, foram abertas várias abas no navegador Brave e outros programas, aumentando a quantidade de processos em execução.

Após aguardar a estabilização do sistema, os mesmos indicadores foram observados novamente para possibilitar a comparação.

## Resultados

| Indicador | Antes | Depois |
|---|---:|---:|
| Memória física total | 16,0 GB | 16,0 GB |
| RAM em uso | 2,8 GB | 5,7 GB |
| Memória disponível | 12,5 GB | 9,5 GB |
| Memória confirmada | 3,1/17,8 GB | 6,5/17,8 GB |
| Maior processo por uso de memória | Antimalware Service Executable — 151,2 MB | Brave Browser — 2.463,3 MB |
| CPU | 3% | 11% |
| Disco | 0% | 0% |

### Estado inicial

No estado inicial, o sistema apresentava 2,8 GB de RAM em uso e 12,5 GB disponíveis.

O processo que mais utilizava memória era o Antimalware Service Executable, com aproximadamente 151,2 MB.

### Estado após o aumento da carga

Após a abertura de várias abas do Brave e outros programas, a RAM em uso aumentou para 5,7 GB, enquanto a memória disponível diminuiu para 9,5 GB.

A memória confirmada passou de 3,1/17,8 GB para 6,5/17,8 GB.

O Brave Browser passou a ser o processo que mais utilizava memória, com aproximadamente 2.463,3 MB.

Apesar do aumento da utilização dos recursos, não foi observada lentidão significativa durante o experimento.

## Análise dos resultados

Os resultados demonstraram que o aumento da quantidade de programas e abas abertas elevou a demanda por memória do sistema.

A RAM em uso aumentou em aproximadamente 2,9 GB, enquanto a memória disponível diminuiu em aproximadamente 3,0 GB.

Também houve aumento da memória confirmada. Entretanto, esse indicador isoladamente não é suficiente para afirmar que ocorreu swapping intenso.

Durante o experimento, não foram observados sinais claros de degradação significativa do desempenho. O uso do disco permaneceu em 0% nas medições realizadas.

## Conceitos estudados

### Paginação

A paginação é uma técnica de gerenciamento de memória que divide a memória em unidades menores, permitindo um gerenciamento mais eficiente dos recursos.

### Segmentação

A segmentação organiza a memória de acordo com segmentos lógicos, que podem possuir tamanhos diferentes.

### Swapping

Swapping é o processo relacionado à movimentação de informações entre a memória RAM e o armazenamento secundário quando é necessário liberar espaço na memória.

## O que aprendi

A atividade permitiu observar na prática como o uso da memória muda de acordo com a quantidade de programas e processos em execução.

Também foi possível compreender a diferença entre memória física e memória confirmada e perceber que um aumento na memória confirmada, por si só, não permite concluir que ocorreu swapping intenso.

Outro aprendizado foi a importância de analisar diferentes indicadores antes de chegar a uma conclusão sobre o comportamento do sistema.

## Conclusão

O experimento demonstrou, na prática, o comportamento do gerenciamento de memória do Windows diante do aumento da carga de trabalho.

Houve aumento significativo da RAM utilizada e da memória confirmada, principalmente devido à execução de mais programas e abas do navegador.

Mesmo com o aumento da utilização dos recursos, o sistema permaneceu responsivo durante a análise, não sendo observadas evidências suficientes para afirmar a ocorrência de swapping intenso.

A atividade contribuiu para relacionar os conceitos estudados sobre gerenciamento de memória com o comportamento observado em um sistema operacional real.

## Evidências

As evidências utilizadas durante o experimento estão organizadas na pasta `evidencias/`.

- [Memória — estado inicial](evidencias/antes/memoria-antes.png)
- [Processos — estado inicial](evidencias/antes/processos-antes.png)
- [Memória — após aumento da carga](evidencias/depois/memoria-depois.png)
- [Processos — após aumento da carga](evidencias/depois/processos-depois.png)

## Competências demonstradas

- Monitoramento de recursos do Windows;
- Análise de processos e consumo de memória;
- Gerenciamento de memória em sistemas operacionais;
- Interpretação de indicadores de desempenho;
- Comparação de dados antes e depois de uma alteração no sistema;
- Documentação e análise técnica baseada em evidências.
