# Processadores (CPU) — Guia para Suporte Técnico

> **Categoria:** Hardware
> **Nível:** Iniciante → Intermediário
> **Público-alvo:** Aspirantes e profissionais de Suporte Técnico
> **Objetivo:** Entender o funcionamento dos processadores, identificar suas principais características e realizar diagnósticos básicos relacionados à CPU.

---

## 1. O que é o processador?

O **processador**, também chamado de **CPU (Central Processing Unit)**, é um dos principais componentes de um computador.

Ele é responsável por executar instruções e realizar operações necessárias para que programas e sistemas funcionem.

De forma simplificada:

```text
Usuário
   ↓
Aplicativo
   ↓
Sistema Operacional
   ↓
CPU
   ↓
Processamento das instruções
   ↓
Resultado
```

A CPU trabalha em conjunto com outros componentes, principalmente:

* Memória RAM;
* SSD/HDD;
* Placa-mãe;
* GPU;
* Sistema operacional.

---

# 2. CPU x computador

É comum usuários dizerem:

> "Meu processador está lento."

Porém, o desempenho de um computador não depende exclusivamente da CPU.

Um computador pode apresentar lentidão devido a:

* Pouca RAM;
* SSD/HDD com problemas;
* Falta de espaço em disco;
* Temperatura elevada;
* Drivers;
* Sistema operacional;
* Malware;
* Aplicativos em segundo plano;
* Problemas de rede;
* Fonte de alimentação;
* Problemas na placa-mãe;
* Processador inadequado para determinada tarefa.

Por isso:

> **Não associe automaticamente lentidão ao processador.**

O suporte técnico deve investigar o sistema como um todo.

---

# 3. Principais fabricantes

No mercado de computadores pessoais, os principais fabricantes de processadores são:

* **Intel**
* **AMD**

Existem também outros fabricantes e arquiteturas, especialmente em dispositivos móveis, servidores e equipamentos especializados.

Exemplos de famílias conhecidas:

### Intel

* Core
* Core Ultra
* Xeon
* Pentium
* Celeron

### AMD

* Ryzen
* Threadripper
* EPYC
* Athlon

> ⚠️ As linhas e nomenclaturas dos fabricantes mudam ao longo do tempo. Sempre consulte a documentação oficial para verificar especificações atuais.

---

# 4. O que é um núcleo?

Um **core**, ou núcleo, é uma unidade de processamento dentro da CPU.

Um processador pode possuir:

```text
1 núcleo
2 núcleos
4 núcleos
6 núcleos
8 núcleos
12 núcleos
16 núcleos
...
```

Quanto maior o número de núcleos, maior pode ser a capacidade do processador de executar múltiplas tarefas em paralelo.

Entretanto:

> **Mais núcleos não significa necessariamente mais desempenho em todas as situações.**

O desempenho também depende de:

* Arquitetura;
* Frequência;
* Cache;
* Eficiência;
* Software;
* Tipo de tarefa.

---

# 5. Threads

Uma **thread** representa uma sequência de instruções que pode ser executada pelo processador.

Algumas CPUs possuem tecnologias que permitem que um núcleo físico trabalhe com múltiplas threads simultaneamente.

Exemplo:

```text
4 cores
8 threads
```

Isso não significa que o processador possui 8 núcleos físicos.

Nesse caso:

```text
4 núcleos físicos
        ↓
8 threads lógicas
```

Intel utiliza tecnologias como **Hyper-Threading** em determinados processadores, enquanto a AMD utiliza tecnologias de processamento multithread em suas arquiteturas.

---

# 6. Cores x Threads

| Característica | Core                           | Thread                     |
| -------------- | ------------------------------ | -------------------------- |
| Representa     | Núcleo físico de processamento | Unidade lógica de execução |
| É físico?      | Sim                            | Não necessariamente        |
| Função         | Processar instruções           | Permitir maior paralelismo |
| Exemplo        | 8 cores                        | 16 threads                 |

Uma especificação como:

```text
8 cores / 16 threads
```

significa que existem:

```text
8 núcleos físicos
16 threads lógicas
```

---

# 7. Frequência do processador

A frequência da CPU normalmente é medida em:

**GHz — Gigahertz**

Exemplos:

```text
2.4 GHz
3.2 GHz
4.0 GHz
5.0 GHz
```

A frequência representa a velocidade de clock do processador.

Porém:

> **Não é correto comparar dois processadores apenas pelo número de GHz.**

Por exemplo:

```text
CPU A → 4.0 GHz
CPU B → 3.5 GHz
```

Não significa automaticamente que a CPU A seja mais rápida.

A arquitetura, IPC, quantidade de núcleos, cache e outras características também influenciam o desempenho.

---

# 8. Clock base e Boost

Processadores modernos podem trabalhar com diferentes frequências.

### Clock base

É uma frequência de referência para operação do processador.

### Boost / Turbo

É uma frequência mais alta que pode ser alcançada em determinadas condições.

Dependendo do fabricante, diferentes nomes podem ser utilizados.

Exemplo conceitual:

```text
Clock base
3.2 GHz

Boost
4.8 GHz
```

O processador pode aumentar sua frequência automaticamente quando houver demanda e condições adequadas.

---

# 9. Temperatura do processador

A CPU gera calor durante seu funcionamento.

Quanto maior a carga de processamento, normalmente maior será a quantidade de calor produzida.

Por isso, computadores utilizam sistemas de refrigeração.

Exemplos:

* Dissipador;
* Cooler;
* Ventoinha;
* Heat pipes;
* Pasta térmica;
* Sistemas de refrigeração líquida.

---

# 10. Thermal Throttling

Quando a temperatura do processador fica muito elevada, o sistema pode reduzir seu desempenho para evitar danos.

Esse comportamento é chamado de:

**Thermal Throttling**

De forma simplificada:

```text
Alta carga
   ↓
Temperatura aumenta
   ↓
Limite térmico atingido
   ↓
CPU reduz desempenho
   ↓
Temperatura diminui
```

O usuário pode perceber:

* Quedas de desempenho;
* Travamentos;
* Aplicativos mais lentos;
* Redução de frequência;
* Ventoinha funcionando em alta velocidade.

---

# 11. Possíveis causas de superaquecimento

Uma CPU operando em temperatura elevada pode estar relacionada a:

* Cooler inadequado;
* Ventoinha com defeito;
* Dissipador obstruído;
* Acúmulo de poeira;
* Pasta térmica deteriorada;
* Fluxo de ar inadequado;
* Temperatura ambiente elevada;
* Overclock;
* Processos consumindo muita CPU;
* Problemas no sistema de refrigeração.

O diagnóstico deve considerar o equipamento e suas condições de uso.

---

# 12. Uso da CPU

No Windows, o uso do processador pode ser verificado pelo:

```text
Ctrl + Shift + Esc
```

Depois:

```text
Desempenho
→ CPU
```

Também é possível verificar o uso por processo:

```text
Processos
→ CPU
```

---

# 13. CPU em 100% significa defeito?

**Não necessariamente.**

Uma CPU pode atingir 100% de utilização durante atividades intensivas, como:

* Compilação de código;
* Renderização;
* Jogos;
* Compressão de arquivos;
* Atualizações;
* Processamento de vídeo;
* Execução de máquinas virtuais.

O problema está em identificar se o uso elevado é:

```text
Esperado
ou
Anormal
```

---

# 14. Diagnóstico de CPU em 100%

Quando o usuário informa que a CPU está constantemente em 100%, investigue:

### 1. Qual processo está consumindo CPU?

Abra:

```text
Gerenciador de Tarefas
→ Processos
→ CPU
```

### 2. O consumo é temporário?

Pergunte:

> "O uso fica em 100% o tempo todo ou apenas durante determinadas tarefas?"

### 3. Qual aplicativo está causando o problema?

Identifique o processo.

### 4. O comportamento começou recentemente?

Pergunte sobre:

* Atualizações;
* Novos programas;
* Drivers;
* Alterações no sistema.

### 5. Existe possibilidade de malware?

Considere essa hipótese caso existam processos desconhecidos ou comportamento suspeito.

---

# 15. Processos em segundo plano

Nem todo processo executado em segundo plano é um problema.

O sistema operacional possui diversos serviços necessários para seu funcionamento.

Exemplos:

```text
Windows Update
Antivírus
Serviços de rede
Serviços do sistema
Drivers
Aplicativos sincronizadores
```

Antes de finalizar um processo, verifique sua função.

> ⚠️ **Não encerre processos desconhecidos ou críticos do sistema sem saber o impacto da ação.**

---

# 16. Cache da CPU

A CPU possui memória cache extremamente rápida utilizada para armazenar dados e instruções frequentemente acessados.

Os níveis mais conhecidos são:

```text
L1
L2
L3
```

### L1

Normalmente é a menor e mais rápida.

### L2

Possui maior capacidade que a L1, mantendo alta velocidade.

### L3

Normalmente é maior e pode ser compartilhada entre múltiplos núcleos, dependendo da arquitetura.

Representação simplificada:

```text
CPU
│
├── L1
│
├── L2
│
└── L3
```

A implementação exata varia entre arquiteturas.

---

# 17. CPU x RAM x armazenamento

Esses três componentes possuem funções diferentes.

| Componente | Função                                   |
| ---------- | ---------------------------------------- |
| CPU        | Processa instruções                      |
| RAM        | Mantém dados temporariamente disponíveis |
| SSD/HDD    | Armazena dados permanentemente           |

Analogia:

```text
CPU = trabalhador
RAM = mesa de trabalho
SSD/HDD = armário
```

O trabalhador busca arquivos no armário, coloca-os sobre a mesa e trabalha com eles.

---

# 18. Socket

O **socket** é a interface física e elétrica utilizada para conectar determinados processadores à placa-mãe.

Exemplos de sockets podem incluir diferentes padrões utilizados por Intel e AMD.

O socket deve ser compatível com:

```text
Processador
+
Placa-mãe
+
BIOS/UEFI
```

> ⚠️ Ter o mesmo socket não garante que qualquer processador seja compatível com qualquer placa-mãe.

É necessário verificar a documentação do fabricante.

---

# 19. Processadores soldados

Alguns notebooks e computadores compactos utilizam processadores soldados diretamente à placa-mãe.

Nesse caso:

```text
CPU
↓
Soldada à placa-mãe
```

O processador não pode ser simplesmente removido e substituído como uma CPU instalada em socket.

Essa característica é comum em determinados equipamentos compactos e notebooks.

---

# 20. TDP

**TDP** significa:

**Thermal Design Power**

É uma especificação relacionada ao projeto térmico do processador.

Ela ajuda fabricantes a projetarem sistemas de refrigeração adequados.

> ⚠️ TDP não deve ser interpretado simplesmente como "consumo máximo de energia".

O consumo real pode variar de acordo com:

* Modelo;
* Carga;
* Configuração;
* Limites de potência;
* Temperatura;
* Firmware;
* Plataforma.

---

# 21. GPU integrada

Alguns processadores possuem uma GPU integrada.

Nesse caso:

```text
CPU
├── Núcleos de processamento
└── GPU integrada
```

Uma GPU integrada pode ser suficiente para:

* Navegação;
* Aplicações de escritório;
* Reprodução de vídeo;
* Algumas tarefas gráficas;
* Jogos leves, dependendo do hardware.

Computadores voltados para tarefas gráficas mais pesadas podem utilizar uma GPU dedicada.

---

# 22. CPU x GPU

| CPU                                    | GPU                                      |
| -------------------------------------- | ---------------------------------------- |
| Processamento geral                    | Processamento altamente paralelo         |
| Poucos núcleos relativamente complexos | Muitos núcleos/unidades de processamento |
| Sistemas operacionais                  | Gráficos                                 |
| Aplicações                             | IA e computação paralela                 |
| Processamento geral                    | Jogos e renderização                     |

Essa divisão é simplificada. CPUs e GPUs modernas possuem arquiteturas complexas e podem participar de diversos tipos de processamento.

---

# 23. Arquitetura do processador

A arquitetura define características fundamentais de como o processador funciona.

Entre os conceitos importantes estão:

* Conjunto de instruções;
* Organização interna;
* Núcleos;
* Cache;
* Pipeline;
* IPC;
* Processo de fabricação.

Algumas arquiteturas conhecidas incluem:

* x86-64;
* ARM;
* RISC-V.

---

# 24. 32 bits x 64 bits

Um sistema operacional pode utilizar diferentes arquiteturas.

Atualmente, sistemas de **64 bits** são predominantes em computadores pessoais modernos.

Um sistema 64-bit consegue trabalhar com um espaço de endereçamento muito maior do que sistemas 32-bit.

Para suporte técnico, é importante saber verificar a arquitetura do sistema.

No Windows:

```text
Configurações
→ Sistema
→ Sobre
→ Tipo de sistema
```

---

# 25. Como identificar o processador no Windows

Existem várias maneiras.

## Método 1 — Configurações

Acesse:

```text
Configurações
→ Sistema
→ Sobre
```

Procure:

```text
Processador
```

---

## Método 2 — Gerenciador de Tarefas

Pressione:

```text
Ctrl + Shift + Esc
```

Depois:

```text
Desempenho
→ CPU
```

É possível visualizar informações como:

* Modelo;
* Velocidade;
* Núcleos;
* Processadores lógicos;
* Utilização;
* Cache;
* Tempo de atividade.

---

## Método 3 — Informações do Sistema

Pressione:

```text
Win + R
```

Digite:

```text
msinfo32
```

Procure pelas informações do processador.

---

## Método 4 — Terminal

No Windows Terminal ou PowerShell, comandos podem ser utilizados para consultar informações do hardware.

Exemplo:

```powershell
Get-CimInstance Win32_Processor
```

Para obter informações mais específicas:

```powershell
Get-CimInstance Win32_Processor |
Select-Object Name, NumberOfCores, NumberOfLogicalProcessors, MaxClockSpeed
```

---

# 26. Problemas comuns relacionados à CPU

Alguns problemas encontrados no suporte técnico incluem:

* Uso excessivo da CPU;
* Superaquecimento;
* Thermal throttling;
* Travamentos;
* Desligamentos inesperados;
* Reinicializações;
* Quedas de desempenho;
* Cooler com defeito;
* Pasta térmica deteriorada;
* BIOS/UEFI desatualizada;
* Incompatibilidade entre CPU e placa-mãe;
* Problemas de energia;
* Overclock instável.

---

# 27. Sintomas que podem parecer problema de CPU

Nem todo travamento ou lentidão é causado pelo processador.

Outros componentes podem apresentar sintomas semelhantes.

| Sintoma             | Possíveis causas                      |
| ------------------- | ------------------------------------- |
| Computador lento    | RAM, SSD, CPU, software               |
| Travamentos         | RAM, temperatura, drivers, CPU, GPU   |
| Reinicialização     | Fonte, temperatura, RAM, placa-mãe    |
| Tela azul           | RAM, drivers, hardware, sistema       |
| CPU em 100%         | Aplicativo, atualização, malware, CPU |
| Queda de desempenho | Temperatura, energia, software        |
| Desligamento        | Temperatura, fonte, placa-mãe         |

> O objetivo do suporte é encontrar a **causa raiz**, não apenas o componente que apresenta o sintoma.

---

# 28. Diagnóstico de superaquecimento

Quando houver suspeita de temperatura elevada:

### Passo 1

Verifique a utilização da CPU.

### Passo 2

Identifique quais processos estão utilizando o processador.

### Passo 3

Verifique as temperaturas utilizando ferramentas apropriadas.

### Passo 4

Observe o comportamento das ventoinhas.

### Passo 5

Verifique se existem obstruções ou acúmulo de poeira, quando a manutenção física estiver dentro do escopo autorizado.

### Passo 6

Verifique o sistema de refrigeração.

### Passo 7

Analise se existe redução de frequência relacionada à temperatura.

---

# 29. Manutenção preventiva

A manutenção preventiva ajuda a evitar problemas relacionados à temperatura e ao desempenho.

Boas práticas:

* Manter entradas e saídas de ar desobstruídas;
* Limpar o equipamento conforme as orientações do fabricante;
* Manter o sistema operacional atualizado;
* Manter drivers atualizados quando apropriado;
* Monitorar temperaturas quando houver suspeita de problema;
* Evitar bloquear as entradas de ar de notebooks;
* Utilizar o carregador/fonte adequado;
* Evitar overclock sem conhecimento técnico.

---

# 30. Pasta térmica

A pasta térmica ajuda a melhorar a transferência de calor entre o processador e o sistema de dissipação.

Representação simplificada:

```text
CPU
↓
Pasta térmica
↓
Dissipador
↓
Ventoinha / sistema de refrigeração
↓
Ambiente
```

Com o tempo, dependendo do equipamento e das condições de uso, pode ser necessário realizar manutenção do sistema térmico.

> ⚠️ A troca da pasta térmica deve seguir o procedimento recomendado pelo fabricante e ser realizada somente quando estiver dentro do escopo técnico e de garantia.

---

# 31. Overclock

**Overclock** consiste em operar determinados componentes acima das configurações padrão estabelecidas pelo fabricante.

Pode envolver:

* CPU;
* RAM;
* GPU.

Possíveis consequências:

* Maior temperatura;
* Maior consumo;
* Instabilidade;
* Redução da vida útil em determinadas condições;
* Travamentos;
* Perda de garantia, dependendo do fabricante e das condições.

Em ambientes corporativos, alterações de overclock normalmente não fazem parte dos procedimentos padrão de suporte.

---

# 32. BIOS/UEFI e processador

A BIOS/UEFI é responsável por inicializar e configurar diversos componentes do computador.

Uma atualização de BIOS/UEFI pode, em alguns casos, adicionar suporte a novos processadores ou corrigir problemas de compatibilidade.

Porém:

> ⚠️ Atualizar BIOS/UEFI é um procedimento sensível.

Nunca realize uma atualização sem:

1. Confirmar o modelo exato da placa-mãe/equipamento;
2. Conferir a versão atual;
3. Consultar a documentação oficial;
4. Baixar o firmware correto;
5. Seguir exatamente as instruções do fabricante;
6. Garantir alimentação adequada.

---

# 33. Diagnóstico estruturado de CPU

Utilize uma abordagem sistemática.

```text
Problema relatado
       ↓
Coletar informações
       ↓
Verificar utilização da CPU
       ↓
Identificar processos
       ↓
Verificar temperatura
       ↓
Verificar frequência
       ↓
Verificar memória RAM
       ↓
Verificar armazenamento
       ↓
Verificar drivers
       ↓
Verificar atualizações
       ↓
Testar hipóteses
       ↓
Aplicar solução
       ↓
Validar
       ↓
Documentar
```

---

# 34. Exemplo de atendimento

### Problema

Usuário informa:

> "Meu computador está muito lento."

### Primeiro diagnóstico

O técnico abre o Gerenciador de Tarefas:

```text
CPU: 98%
RAM: 52%
Disco: 12%
```

O técnico identifica um aplicativo utilizando:

```text
CPU: 85%
```

### Próximo passo

Verificar:

* Qual é o aplicativo;
* Se ele deveria estar executando;
* Se existe atualização;
* Se o comportamento é conhecido;
* Se há processos relacionados.

### Possível conclusão

O problema pode estar relacionado ao aplicativo e não à CPU.

Esse exemplo demonstra por que:

> **CPU em 100% é um sintoma, não um diagnóstico.**

---

# 35. Checklist de diagnóstico

### Informações do equipamento

* [ ] Modelo do computador
* [ ] Modelo do processador
* [ ] Sistema operacional
* [ ] Arquitetura 32/64 bits
* [ ] Quantidade de núcleos
* [ ] Quantidade de threads
* [ ] GPU integrada ou dedicada

### Sintomas

* [ ] Lentidão
* [ ] Travamentos
* [ ] Reinicializações
* [ ] Desligamentos
* [ ] Temperatura elevada
* [ ] Ventoinha em alta rotação
* [ ] CPU em 100%

### Diagnóstico

* [ ] Verificar processos
* [ ] Verificar temperatura
* [ ] Verificar frequência
* [ ] Verificar RAM
* [ ] Verificar armazenamento
* [ ] Verificar drivers
* [ ] Verificar atualizações
* [ ] Verificar BIOS/UEFI quando necessário

### Manutenção

* [ ] Verificar ventilação
* [ ] Verificar acúmulo de poeira
* [ ] Verificar cooler
* [ ] Verificar pasta térmica quando aplicável
* [ ] Seguir procedimentos ESD
* [ ] Seguir documentação do fabricante

---

# 36. Perguntas importantes durante o atendimento

Perguntas simples podem ajudar bastante no diagnóstico:

> "Quando o problema começou?"

> "O computador fica lento o tempo todo?"

> "O problema acontece durante algum programa específico?"

> "O computador reinicia ou desliga sozinho?"

> "A ventoinha está fazendo muito barulho?"

> "O computador fica quente?"

> "Foi instalado algum programa recentemente?"

> "O problema começou depois de alguma atualização?"

> "O problema acontece quando o computador está conectado ao carregador?"

---

# 37. Boas práticas para o profissional de Suporte Técnico

### Não faça:

* Troque a CPU sem diagnóstico;
* Atualize BIOS/UEFI sem verificar o modelo;
* Encerre processos desconhecidos indiscriminadamente;
* Assuma que 100% de CPU significa defeito;
* Recomende um processador apenas pelo número de GHz;
* Ignore temperatura;
* Ignore RAM e armazenamento durante o diagnóstico.

### Faça:

* Colete evidências;
* Identifique o modelo exato;
* Consulte documentação;
* Teste uma hipótese por vez;
* Registre os procedimentos;
* Valide a solução;
* Documente a causa raiz.

---

# 38. Conceitos que o profissional deve dominar

Para trabalhar com suporte técnico, é importante conhecer:

* CPU;
* Core;
* Thread;
* Clock;
* Boost/Turbo;
* Cache;
* L1;
* L2;
* L3;
* IPC;
* GHz;
* TDP;
* Thermal Throttling;
* Socket;
* BIOS;
* UEFI;
* GPU integrada;
* Arquitetura x86-64;
* ARM;
* 32 bits;
* 64 bits;
* Overclock;
* Sistema de refrigeração;
* Pasta térmica.

---

# 39. Resumo rápido

```text
PROCESSADOR (CPU)
│
├── Executa instruções
│
├── Principais características
│   ├── Cores
│   ├── Threads
│   ├── Clock
│   ├── Boost
│   ├── Cache
│   └── Arquitetura
│
├── Trabalha em conjunto com
│   ├── RAM
│   ├── SSD/HDD
│   ├── GPU
│   └── Placa-mãe
│
├── Problemas comuns
│   ├── Uso elevado
│   ├── Superaquecimento
│   ├── Thermal Throttling
│   ├── Travamentos
│   └── Incompatibilidade
│
└── Diagnóstico
    ├── Verificar processos
    ├── Verificar temperatura
    ├── Verificar frequência
    ├── Verificar RAM
    ├── Verificar armazenamento
    ├── Verificar drivers
    └── Validar solução
```

---

# 40. Glossário

| Termo                  | Significado                                                             |
| ---------------------- | ----------------------------------------------------------------------- |
| **CPU**                | Central Processing Unit                                                 |
| **Core**               | Núcleo físico de processamento                                          |
| **Thread**             | Unidade lógica de execução                                              |
| **Clock**              | Frequência de operação do processador                                   |
| **GHz**                | Gigahertz                                                               |
| **Boost**              | Aumento automático da frequência em determinadas condições              |
| **Cache**              | Memória rápida utilizada pela CPU                                       |
| **IPC**                | Instructions Per Cycle                                                  |
| **TDP**                | Thermal Design Power                                                    |
| **Socket**             | Interface física e elétrica para determinados processadores             |
| **Thermal Throttling** | Redução de desempenho para controlar temperatura                        |
| **GPU**                | Graphics Processing Unit                                                |
| **BIOS**               | Basic Input/Output System                                               |
| **UEFI**               | Unified Extensible Firmware Interface                                   |
| **Overclock**          | Operação acima das configurações padrão                                 |
| **CPU integrada**      | Processador instalado diretamente na placa-mãe, sem socket substituível |
| **Arquitetura**        | Organização e conjunto de instruções utilizados pelo processador        |

---

# 41. Boas práticas de estudo

Para quem está se preparando para trabalhar com Suporte Técnico:

1. Identifique o processador do seu computador.
2. Descubra quantos cores e threads ele possui.
3. Verifique a utilização da CPU pelo Gerenciador de Tarefas.
4. Identifique qual processo está consumindo mais CPU.
5. Pesquise a temperatura do processador.
6. Identifique o socket de uma CPU desktop.
7. Pesquise quais processadores são compatíveis com uma determinada placa-mãe.
8. Diferencie CPU, RAM, SSD e GPU.
9. Aprenda a interpretar especificações de processadores.
10. Pratique a criação de hipóteses durante um diagnóstico.

---

## Conclusão

O processador é um dos componentes fundamentais de um computador, mas o profissional de Suporte Técnico deve evitar enxergá-lo de forma isolada.

Um bom diagnóstico considera:

```text
Hardware
+
Software
+
Sistema Operacional
+
Drivers
+
Temperatura
+
Energia
+
Comportamento do usuário
```

A habilidade mais importante não é decorar modelos de processadores, mas saber **investigar sintomas, coletar evidências, testar hipóteses e identificar a causa raiz do problema**.

> **Diagnostique antes de substituir. Documente antes de encerrar. Valide antes de concluir.**
