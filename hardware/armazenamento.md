# Armazenamento

## 📚 Introdução

Os dispositivos de armazenamento são responsáveis por **guardar dados de forma permanente ou temporária** em computadores, notebooks e outros equipamentos.

No suporte técnico, compreender os diferentes tipos de armazenamento é fundamental para identificar problemas de **lentidão, falta de espaço, falhas de inicialização, perda de dados e desempenho**.

Os principais dispositivos encontrados atualmente são:

* **HDD (Hard Disk Drive)**
* **SSD SATA**
* **SSD NVMe**
* **HD externo**
* **SSD externo**
* **Pen drives**
* **Cartões de memória**

---

## 💾 1. HDD

O **HDD (Hard Disk Drive)** utiliza discos magnéticos que giram fisicamente para armazenar os dados.

### Características

* Possui partes mecânicas móveis.
* Geralmente possui grande capacidade por um custo menor.
* É mais lento que um SSD.
* É mais suscetível a danos causados por impactos.
* Pode apresentar ruídos durante o funcionamento.

### Vantagens

* Grande capacidade de armazenamento.
* Custo por GB geralmente mais baixo.
* Boa opção para armazenamento de grandes volumes de arquivos.

### Desvantagens

* Menor velocidade.
* Maior consumo de energia.
* Mais sensível a impactos.
* Pode apresentar ruídos.
* Maior tempo de inicialização e carregamento do sistema.

---

## ⚡ 2. SSD

O **SSD (Solid State Drive)** utiliza memória flash para armazenar dados e não possui partes mecânicas móveis.

Isso proporciona maior velocidade e resistência física em comparação com HDDs.

### Características

* Inicialização rápida do sistema.
* Maior velocidade de leitura e escrita.
* Operação silenciosa.
* Menor consumo de energia.
* Maior resistência a impactos.

---

## 🔌 3. SSD SATA

O **SSD SATA** utiliza a interface SATA, sendo uma alternativa comum para substituir HDDs.

A interface SATA III possui uma velocidade teórica máxima de aproximadamente **6 Gb/s**.

### Uso comum

* Upgrade de notebooks antigos.
* Computadores que possuem baias SATA.
* Substituição de HDDs.

### 💡 Dica de suporte

Trocar um HDD por um SSD SATA costuma proporcionar uma **grande melhoria na percepção de velocidade do computador**, mesmo sem trocar processador ou memória RAM.

---

## 🚀 4. SSD NVMe

O **NVMe (Non-Volatile Memory Express)** é um protocolo desenvolvido para aproveitar melhor a velocidade das unidades de armazenamento que utilizam PCIe.

Os SSDs NVMe normalmente utilizam o formato **M.2** em computadores e notebooks modernos.

> ⚠️ M.2 e NVMe não são sinônimos. **M.2 é um formato físico**, enquanto **NVMe é um protocolo de comunicação**. Existem unidades M.2 SATA e M.2 NVMe.

### Vantagens

* Alta velocidade de leitura e escrita.
* Baixa latência.
* Excelente desempenho em tarefas que realizam muitas operações de armazenamento.
* Não utiliza cabos SATA quando instalado diretamente no slot M.2.

---

## 🔎 5. HDD x SSD SATA x SSD NVMe

| Característica         | HDD                      | SSD SATA               | SSD NVMe                       |
| ---------------------- | ------------------------ | ---------------------- | ------------------------------ |
| Tecnologia             | Magnética                | Flash                  | Flash                          |
| Partes móveis          | Sim                      | Não                    | Não                            |
| Velocidade             | Baixa                    | Alta                   | Muito alta                     |
| Interface              | SATA                     | SATA                   | PCIe                           |
| Ruído                  | Sim                      | Não                    | Não                            |
| Resistência a impactos | Menor                    | Maior                  | Maior                          |
| Consumo                | Maior                    | Menor                  | Menor                          |
| Uso comum              | Arquivos e armazenamento | Upgrade de PCs antigos | PCs modernos e alto desempenho |

---

## 📦 6. Capacidade de armazenamento

A capacidade é normalmente apresentada em:

* **KB** — Kilobyte
* **MB** — Megabyte
* **GB** — Gigabyte
* **TB** — Terabyte

Uma forma simplificada de visualizar:

```text
1 TB
↓
1.000 GB
↓
1.000.000 MB
↓
1.000.000.000 KB
```

> 💡 Fabricantes de armazenamento normalmente utilizam unidades decimais. O sistema operacional pode apresentar uma capacidade diferente devido à forma como calcula e exibe os valores.

---

## 🧩 7. Partições

Uma unidade física pode ser dividida em diferentes **partições**.

Por exemplo:

```text
SSD de 1 TB
│
├── C: → Sistema operacional
└── D: → Arquivos pessoais
```

As partições permitem organizar o armazenamento e separar diferentes tipos de dados.

### No Windows

A ferramenta **Gerenciamento de Disco** permite:

* Criar partições.
* Excluir partições.
* Formatar volumes.
* Alterar letras de unidade.
* Reduzir volumes.
* Estender volumes.

> ⚠️ Operações como exclusão e formatação podem causar perda de dados. Sempre confirme o conteúdo da unidade antes de realizar essas operações.

---

## 🗂️ 8. Sistemas de arquivos

O sistema de arquivos determina como os dados são organizados e armazenados em uma unidade.

No Windows, os mais importantes para suporte são:

### NTFS

É o sistema de arquivos mais utilizado nas instalações modernas do Windows.

Características:

* Suporta arquivos grandes.
* Possui recursos de segurança e permissões.
* Adequado para unidades internas do sistema.

### exFAT

Muito utilizado em:

* Pen drives.
* Cartões de memória.
* HDs e SSDs externos.

É uma boa opção quando existe necessidade de compatibilidade entre diferentes sistemas operacionais.

### FAT32

É um sistema de arquivos antigo e bastante compatível.

Uma limitação importante é que **um único arquivo não pode ultrapassar aproximadamente 4 GB**.

---

## 🩺 9. Sintomas de problemas no armazenamento

Um dispositivo de armazenamento com problemas pode apresentar:

* Computador muito lento.
* Sistema operacional demorando para iniciar.
* Aplicativos demorando para abrir.
* Arquivos corrompidos.
* Erros ao copiar arquivos.
* Arquivos desaparecendo.
* Tela azul.
* Travamentos frequentes.
* Sistema operacional não inicializando.
* Unidade não sendo reconhecida.
* HDD produzindo ruídos incomuns.

### ⚠️ Atenção

Se houver suspeita de falha física e os dados forem importantes, **evite realizar procedimentos que possam agravar a situação**.

Priorize a preservação dos dados e, quando necessário, encaminhe o equipamento para recuperação especializada.

---

## 🔍 10. Diagnóstico básico no suporte técnico

Ao investigar problemas relacionados ao armazenamento, siga uma sequência lógica.

### 1. Verifique o espaço disponível

No Windows:

**Configurações → Sistema → Armazenamento**

Pouco espaço disponível pode causar problemas de desempenho.

---

### 2. Verifique se a unidade é reconhecida

Abra:

**Gerenciamento de Disco**

Verifique se a unidade aparece corretamente.

---

### 3. Verifique o Gerenciador de Dispositivos

Procure por:

**Unidades de disco**

Isso pode ajudar a identificar problemas de reconhecimento do dispositivo.

---

### 4. Verifique a saúde da unidade

Ferramentas de monitoramento podem apresentar informações relacionadas ao **S.M.A.R.T. (Self-Monitoring, Analysis and Reporting Technology)**.

Esses dados podem ajudar a identificar sinais de degradação do dispositivo.

---

### 5. Verifique o desempenho

O **Gerenciador de Tarefas** pode mostrar a utilização do disco.

Caminho:

**Ctrl + Shift + Esc → Desempenho → Disco**

Observe:

* Utilização do disco.
* Velocidade de leitura.
* Velocidade de gravação.
* Tempo de atividade.

> ⚠️ Disco em 100% de utilização não significa automaticamente que o armazenamento está com defeito. É necessário identificar qual processo está causando a atividade.

---

## 🛠️ 11. Comandos úteis no Windows

### CHKDSK

O `chkdsk` pode verificar problemas relacionados ao sistema de arquivos.

Exemplo:

```cmd
chkdsk C:
```

Para verificar e tentar corrigir erros:

```cmd
chkdsk C: /f
```

> ⚠️ Antes de utilizar parâmetros de reparo, entenda o impacto da operação e certifique-se de que os dados importantes estejam protegidos.

---

## 📊 12. Armazenamento cheio

Quando uma unidade está quase cheia, algumas tarefas podem apresentar problemas.

Possíveis causas:

* Arquivos temporários.
* Downloads antigos.
* Programas desnecessários.
* Arquivos pessoais grandes.
* Lixeira cheia.
* Atualizações antigas.
* Arquivos de cache.

### Procedimento básico

1. Identificar o que está ocupando espaço.
2. Remover arquivos desnecessários.
3. Esvaziar a Lixeira quando apropriado.
4. Desinstalar programas que não são utilizados.
5. Transferir arquivos grandes para outro armazenamento.
6. Considerar um upgrade de armazenamento quando necessário.

---

## 💽 13. Desfragmentação e SSD

A **desfragmentação tradicional** foi desenvolvida principalmente para HDDs.

Em SSDs, o gerenciamento é diferente.

O Windows possui mecanismos de **otimização de unidades** que tratam HDDs e SSDs de maneira diferente.

> ❌ Não é recomendado tratar um SSD como se fosse um HDD e executar processos de desfragmentação tradicional indiscriminadamente.

---

## 🔐 14. Backup

Um armazenamento saudável não substitui um **backup**.

Uma estratégia de backup deve considerar:

* O que precisa ser protegido.
* Com que frequência o backup será realizado.
* Onde as cópias serão armazenadas.
* Como os dados serão restaurados.

### Regra 3-2-1

Uma estratégia conhecida é manter:

**3** cópias dos dados
**2** tipos diferentes de mídia
**1** cópia fora do equipamento ou local principal

Exemplo:

```text
Computador
   │
   ├── SSD interno
   │
   ├── HD externo
   │
   └── Backup em nuvem
```

---

## 🧑‍💻 15. Boas práticas para suporte técnico

Ao trabalhar com problemas de armazenamento:

* Nunca formate uma unidade sem confirmar a necessidade.
* Pergunte se existem dados importantes antes de realizar alterações.
* Faça backup antes de procedimentos de risco.
* Verifique primeiro se o problema é lógico ou físico.
* Não presuma que uma unidade em 100% de uso está defeituosa.
* Verifique cabos e conexões em unidades SATA.
* Confirme a compatibilidade antes de instalar um novo SSD.
* Consulte a documentação do fabricante.
* Registre os procedimentos realizados no chamado.
* Oriente o usuário sobre a importância de backups.

---

## 📝 Checklist de diagnóstico

* [ ] Verificar o espaço disponível.
* [ ] Confirmar se a unidade é reconhecida pelo sistema.
* [ ] Verificar o Gerenciamento de Disco.
* [ ] Verificar o Gerenciador de Dispositivos.
* [ ] Identificar se a unidade é HDD, SSD SATA ou SSD NVMe.
* [ ] Verificar sinais de falha.
* [ ] Consultar informações S.M.A.R.T. quando disponíveis.
* [ ] Verificar processos que utilizam o disco.
* [ ] Confirmar a existência de backup antes de procedimentos de risco.
* [ ] Registrar o diagnóstico e as ações realizadas.

---

## 🎯 O que um profissional de suporte deve saber

Para trabalhar com suporte técnico, é importante saber:

1. Diferenciar **HDD, SSD SATA e SSD NVMe**.
2. Entender a diferença entre **M.2 e NVMe**.
3. Identificar problemas de espaço em disco.
4. Reconhecer sinais de falha de armazenamento.
5. Entender o conceito de **partição**.
6. Conhecer os principais sistemas de arquivos.
7. Utilizar ferramentas básicas de diagnóstico do Windows.
8. Entender a importância do backup.
9. Saber quando **não** realizar procedimentos que possam causar perda de dados.
10. Saber identificar quando um problema deve ser encaminhado para uma equipe especializada.

---

## 📚 Resumo rápido

```text
HDD
└── Magnético + partes móveis
    └── Mais barato por GB
    └── Mais lento

SSD SATA
└── Memória flash
    └── Mais rápido que HDD
    └── Interface SATA

SSD NVMe
└── Memória flash
    └── Utiliza PCIe
    └── Alta velocidade
    └── Geralmente utiliza M.2

M.2
└── Formato físico
    ├── Pode ser SATA
    └── Pode ser NVMe

Backup
└── Protege os dados contra falhas
```

> 💡 **Para suporte técnico:** entender armazenamento não significa apenas saber qual SSD é mais rápido. O mais importante é conseguir **diagnosticar problemas, preservar os dados do usuário e escolher o procedimento adequado para cada situação**.
