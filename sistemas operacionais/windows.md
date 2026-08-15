# Windows

## 📚 Introdução

O **Windows** é um sistema operacional desenvolvido pela Microsoft e é amplamente utilizado em computadores pessoais e ambientes corporativos.

Para profissionais de **Suporte Técnico**, conhecer o Windows é essencial, pois grande parte dos chamados envolve problemas relacionados ao sistema operacional, aplicativos, usuários, rede, armazenamento, drivers e configurações.

Este guia apresenta conceitos e ferramentas importantes para quem está iniciando na área de suporte.

---

## 🖥️ 1. O que é um sistema operacional?

O **Sistema Operacional (SO)** é o software responsável por gerenciar os recursos do computador e fornecer uma interface para que o usuário possa utilizar o equipamento.

Entre suas principais responsabilidades estão:

* Gerenciar processador.
* Gerenciar memória RAM.
* Gerenciar armazenamento.
* Gerenciar dispositivos.
* Gerenciar usuários e permissões.
* Executar aplicativos.
* Gerenciar conexões de rede.
* Fornecer mecanismos de segurança.

Exemplos de sistemas operacionais:

* Windows
* Linux
* macOS
* Android
* iOS

---

## 🪟 2. Principais versões do Windows

Algumas versões importantes da família Windows incluem:

* Windows 7
* Windows 8
* Windows 8.1
* Windows 10
* Windows 11

Em ambientes corporativos, também podem ser encontradas versões como:

* Windows 10/11 Pro
* Windows 10/11 Enterprise
* Windows Server

> 💡 No suporte técnico, é importante saber qual versão e edição do Windows o usuário está utilizando antes de iniciar um diagnóstico.

---

## 🔎 3. Como verificar informações do Windows

Existem várias maneiras de identificar a versão do sistema.

### Configurações

Acesse:

**Configurações → Sistema → Sobre**

É possível encontrar informações como:

* Edição do Windows.
* Versão.
* Build do sistema operacional.
* Processador.
* Memória RAM.
* Tipo de sistema.

### Comando `winver`

Pressione:

**Win + R**

Digite:

```cmd
winver
```

Esse comando abre uma janela com informações sobre a versão do Windows.

---

## ⚙️ 4. Configurações do Windows

O aplicativo **Configurações** concentra diversas opções administrativas do sistema.

Algumas categorias importantes para suporte são:

### Sistema

Permite acessar configurações relacionadas a:

* Tela.
* Som.
* Notificações.
* Energia.
* Armazenamento.
* Área de trabalho remota.
* Informações do sistema.

### Bluetooth e dispositivos

Utilizado para configurar:

* Bluetooth.
* Impressoras.
* Mouse.
* Teclado.
* Outros dispositivos.

### Rede e Internet

Permite configurar e diagnosticar:

* Wi-Fi.
* Ethernet.
* VPN.
* Proxy.
* Configurações de rede.

### Aplicativos

Permite:

* Instalar e desinstalar aplicativos.
* Gerenciar aplicativos instalados.
* Configurar aplicativos padrão.

### Contas

Permite gerenciar:

* Usuários.
* Opções de entrada.
* Contas corporativas.
* Contas de acesso.

### Windows Update

Utilizado para:

* Procurar atualizações.
* Instalar atualizações.
* Verificar histórico de atualizações.
* Configurar opções relacionadas às atualizações.

---

## 👤 5. Usuários e contas

O Windows permite criar diferentes tipos de contas.

### Conta padrão

Possui permissões limitadas e é adequada para uso cotidiano.

### Administrador

Possui permissões elevadas para realizar alterações no sistema.

> ⚠️ Não é uma boa prática utilizar uma conta com privilégios administrativos para todas as atividades sem necessidade.

---

## 🔐 6. Controle de Conta de Usuário — UAC

O **User Account Control (UAC)** ajuda a impedir que alterações importantes sejam realizadas silenciosamente.

Quando uma aplicação ou usuário tenta executar uma ação que exige privilégios elevados, o Windows pode solicitar confirmação.

Exemplo:

```text
Aplicativo solicita privilégio administrativo
              ↓
        UAC solicita confirmação
              ↓
       Usuário autoriza
              ↓
       Operação é executada
```

O UAC é uma camada adicional de segurança.

---

## 🛠️ 7. Gerenciador de Tarefas

O **Gerenciador de Tarefas** é uma das ferramentas mais importantes para suporte técnico.

Atalho:

**Ctrl + Shift + Esc**

Ele permite visualizar:

* Processos.
* Desempenho.
* Aplicativos de inicialização.
* Usuários.
* Serviços.
* Uso de CPU.
* Uso de memória.
* Uso de disco.
* Uso de rede.

### Exemplo

Se o computador estiver lento:

1. Abra o Gerenciador de Tarefas.
2. Verifique CPU.
3. Verifique memória.
4. Verifique disco.
5. Identifique processos que estão consumindo muitos recursos.

> 💡 Evite finalizar processos desconhecidos sem entender sua função.

---

## 🧩 8. Gerenciador de Dispositivos

O **Gerenciador de Dispositivos** permite visualizar o hardware instalado e seus respectivos drivers.

Para abrir:

**Win + X → Gerenciador de Dispositivos**

Também pode ser executado:

```cmd
devmgmt.msc
```

Categorias comuns:

* Adaptadores de vídeo.
* Adaptadores de rede.
* Controladores de som.
* Controladores USB.
* Unidades de disco.
* Teclados.
* Mouses.
* Processadores.

### Problemas comuns

Um dispositivo pode apresentar:

* Driver ausente.
* Driver incompatível.
* Driver desatualizado.
* Dispositivo desabilitado.
* Falha de hardware.

---

## 🔄 9. Windows Update

O **Windows Update** mantém o sistema operacional atualizado.

As atualizações podem incluir:

* Correções de segurança.
* Correções de bugs.
* Melhorias de estabilidade.
* Atualizações de drivers.
* Novos recursos.

### Boas práticas

* Manter o sistema atualizado.
* Reiniciar o computador quando solicitado.
* Verificar o histórico de atualizações quando surgir um problema após uma atualização.
* Evitar interromper uma atualização em andamento.

---

## 🛡️ 10. Segurança do Windows

O Windows possui recursos de segurança integrados.

Entre eles:

* Microsoft Defender.
* Firewall do Windows.
* Controle de Conta de Usuário.
* Windows Update.
* Secure Boot.
* BitLocker em edições compatíveis.

### Microsoft Defender

O Defender fornece proteção contra diferentes tipos de ameaças, incluindo malware.

O suporte técnico deve verificar:

* Se a proteção está ativa.
* Se as definições estão atualizadas.
* Se existem ameaças detectadas.

---

## 🔥 11. Firewall

O **Firewall do Windows** controla determinadas conexões de rede.

Ele pode ajudar a impedir que conexões não autorizadas alcancem o computador.

Uma aplicação pode apresentar problemas de conexão quando:

* Uma regra bloqueia a comunicação.
* O firewall está configurado incorretamente.
* A aplicação utiliza uma porta que não está permitida.

> ⚠️ Desativar o firewall não deve ser tratado como solução padrão para problemas de rede. Primeiro investigue as regras e a causa do bloqueio.

---

## 💾 12. Armazenamento

O Windows possui ferramentas para gerenciamento do armazenamento.

Acesse:

**Configurações → Sistema → Armazenamento**

É possível verificar:

* Espaço utilizado.
* Espaço disponível.
* Aplicativos instalados.
* Arquivos temporários.
* Documentos.
* Downloads.

### Ferramenta Limpeza de Disco

Pode ser executada com:

```cmd
cleanmgr
```

Ela pode ajudar a remover determinados arquivos desnecessários.

---

## 🗂️ 13. Explorador de Arquivos

O **Explorador de Arquivos** permite navegar e gerenciar arquivos e pastas.

Atalho:

**Win + E**

Operações comuns:

* Criar pastas.
* Copiar arquivos.
* Mover arquivos.
* Renomear arquivos.
* Excluir arquivos.
* Compactar arquivos.
* Acessar unidades de armazenamento.

### Extensões de arquivos

É importante reconhecer algumas extensões comuns:

| Extensão | Tipo               |
| -------- | ------------------ |
| `.exe`   | Executável         |
| `.msi`   | Instalador         |
| `.txt`   | Texto              |
| `.pdf`   | Documento PDF      |
| `.docx`  | Documento Word     |
| `.xlsx`  | Planilha Excel     |
| `.zip`   | Arquivo compactado |
| `.jpg`   | Imagem             |
| `.png`   | Imagem             |

> ⚠️ A extensão de um arquivo não garante que seu conteúdo seja seguro. Arquivos executáveis recebidos de fontes desconhecidas devem ser tratados com cautela.

---

## 💻 14. Prompt de Comando — CMD

O **Prompt de Comando** permite executar comandos administrativos e realizar diagnósticos.

Para abrir:

**Win + R → `cmd`**

Alguns comandos importantes para suporte:

### `ipconfig`

Exibe informações de rede.

```cmd
ipconfig
```

### `ipconfig /all`

Exibe informações mais detalhadas:

```cmd
ipconfig /all
```

### `ping`

Testa a conectividade com outro dispositivo.

```cmd
ping 8.8.8.8
```

### `tracert`

Mostra o caminho percorrido pelos pacotes até um destino.

```cmd
tracert google.com
```

### `nslookup`

Consulta informações relacionadas ao DNS.

```cmd
nslookup google.com
```

### `hostname`

Exibe o nome do computador.

```cmd
hostname
```

### `whoami`

Mostra o usuário atualmente conectado.

```cmd
whoami
```

### `systeminfo`

Exibe informações detalhadas sobre o sistema.

```cmd
systeminfo
```

---

## 🔧 15. PowerShell

O **PowerShell** é uma ferramenta mais avançada de automação e administração do Windows.

Ele permite:

* Executar comandos.
* Automatizar tarefas.
* Gerenciar arquivos.
* Administrar sistemas.
* Trabalhar com serviços.
* Consultar informações do sistema.

Para abrir:

**Win + X → Terminal**

Ou pesquise por:

**PowerShell**

Exemplo:

```powershell
Get-ComputerInfo
```

Lista processos:

```powershell
Get-Process
```

Lista serviços:

```powershell
Get-Service
```

> 💡 Para suporte técnico, aprender PowerShell pode ser um diferencial importante, principalmente em ambientes corporativos.

---

## ⚙️ 16. Serviços do Windows

Os **Serviços do Windows** são processos que executam determinadas funções em segundo plano.

Para abrir:

```cmd
services.msc
```

Exemplos:

* Windows Update.
* Print Spooler.
* DHCP Client.
* DNS Client.
* Windows Defender.

Um serviço pode apresentar estados como:

* Em execução.
* Parado.
* Desabilitado.

> ⚠️ Não altere serviços aleatoriamente. Desabilitar um serviço essencial pode causar problemas no sistema.

---

## 🚀 17. Inicialização do sistema

Programas configurados para iniciar automaticamente podem aumentar o tempo necessário para o Windows iniciar.

No Gerenciador de Tarefas:

**Gerenciador de Tarefas → Aplicativos de Inicialização**

É possível verificar:

* Nome do aplicativo.
* Status.
* Impacto na inicialização.

Desabilitar aplicativos desnecessários pode melhorar o tempo de inicialização.

---

## 🧹 18. Diagnóstico de lentidão

Quando o usuário relata que o computador está lento, não se deve assumir imediatamente que o problema é o hardware.

Investigue:

### Hardware

* CPU.
* RAM.
* Armazenamento.
* Temperatura.
* Saúde do SSD/HDD.

### Software

* Processos em segundo plano.
* Aplicativos iniciados automaticamente.
* Malware.
* Atualizações.
* Programas consumindo muitos recursos.

### Armazenamento

* Espaço disponível.
* Saúde da unidade.
* Utilização do disco.

### Rede

* Velocidade da conexão.
* Latência.
* Perda de pacotes.
* Problemas de DNS.

---

## 🔵 19. Tela Azul — BSOD

A **Blue Screen of Death (BSOD)** ocorre quando o Windows encontra um erro crítico que impede o funcionamento normal do sistema.

Possíveis causas:

* Drivers problemáticos.
* Falhas de hardware.
* Problemas de memória RAM.
* Problemas de armazenamento.
* Software incompatível.
* Corrupção de arquivos do sistema.

### Procedimento inicial

1. Anote o código ou nome do erro.
2. Verifique quando o problema começou.
3. Identifique alterações recentes.
4. Verifique drivers.
5. Verifique hardware.
6. Consulte os registros do sistema.
7. Pesquise o código específico do erro.

---

## 🧰 20. Verificação de arquivos do sistema

O Windows possui ferramentas para verificar e reparar arquivos do sistema.

### SFC

O **System File Checker** pode verificar arquivos protegidos do Windows.

Execute o Prompt de Comando como administrador e utilize:

```cmd
sfc /scannow
```

### DISM

O **Deployment Image Servicing and Management** pode ser utilizado para reparar componentes da imagem do Windows.

Exemplo:

```cmd
DISM /Online /Cleanup-Image /RestoreHealth
```

> ⚠️ Essas ferramentas devem ser utilizadas como parte de um diagnóstico, e não como solução automática para qualquer problema do Windows.

---

## 📋 21. Visualizador de Eventos

O **Event Viewer** permite consultar registros gerados pelo sistema e pelos aplicativos.

Para abrir:

```cmd
eventvwr.msc
```

Pode ajudar a investigar:

* Falhas de aplicativos.
* Erros do sistema.
* Problemas de serviços.
* Eventos de segurança.
* Problemas relacionados ao hardware.

Categorias importantes incluem:

* Application.
* Security.
* System.

> 💡 Os logs podem conter muitas informações. Procure relacionar o horário do evento com o momento em que o problema ocorreu.

---

## 🌐 22. Diagnóstico de rede no Windows

Quando o usuário não consegue acessar a internet, siga uma sequência lógica.

### Verifique:

1. Wi-Fi ou cabo Ethernet.
2. Conexão com o roteador.
3. Endereço IP.
4. Gateway.
5. DNS.
6. Conectividade externa.

Comandos úteis:

```cmd
ipconfig
```

```cmd
ping <gateway>
```

```cmd
ping 8.8.8.8
```

```cmd
nslookup google.com
```

### Interpretação simplificada

```text
Computador
    ↓
Gateway
    ↓
Internet
    ↓
DNS
```

Se o computador consegue alcançar o gateway, mas não consegue acessar a internet, o problema pode estar além da rede local.

---

## 🔄 23. Restauração do Sistema

A **Restauração do Sistema** permite retornar determinados componentes do Windows a um estado anterior por meio de pontos de restauração.

Pode ser útil após:

* Instalação problemática de software.
* Alterações de configuração.
* Instalação de determinados drivers.

> ⚠️ A Restauração do Sistema não deve ser confundida com um backup completo dos arquivos pessoais.

---

## 🔁 24. Modo de Segurança

O **Modo de Segurança** inicia o Windows com um conjunto limitado de recursos e drivers.

Pode ajudar a investigar problemas causados por:

* Drivers.
* Programas de inicialização.
* Software de terceiros.

É útil quando o Windows funciona normalmente em Modo de Segurança, mas apresenta problemas durante a inicialização normal.

---

## 💻 25. Área de Trabalho Remota

Em ambientes corporativos, ferramentas de acesso remoto podem ser utilizadas para prestar suporte.

O Windows possui o **Remote Desktop Protocol (RDP)**.

O acesso remoto permite que um técnico:

* Analise configurações.
* Execute comandos.
* Verifique logs.
* Auxilie o usuário.

> ⚠️ Acesso remoto deve ser realizado somente com autorização e seguindo as políticas de segurança da organização.

---

## 🧑‍💼 26. Windows em ambientes corporativos

Em empresas, o Windows pode estar integrado a serviços de gerenciamento e identidade.

Alguns conceitos importantes:

* Active Directory.
* Microsoft Entra ID.
* Group Policy.
* Domínio.
* Usuários e grupos.
* Permissões.
* Políticas de segurança.
* Gerenciamento de dispositivos.

Para quem deseja trabalhar com **Suporte Técnico**, estudar esses conceitos pode ser um diferencial importante.

---

## 🔐 27. Permissões de arquivos

O Windows utiliza permissões para controlar quem pode acessar determinados arquivos e pastas.

Permissões comuns incluem:

* Leitura.
* Gravação.
* Modificação.
* Controle total.

Em ambientes corporativos, problemas de acesso podem ocorrer devido a:

* Permissões incorretas.
* Usuário errado.
* Grupo incorreto.
* Herança de permissões.
* Políticas da organização.

---

## 🧑‍🔧 28. Metodologia de troubleshooting

Um bom profissional de suporte não deve simplesmente tentar soluções aleatórias.

Uma abordagem recomendada:

### 1. Identificar o problema

Pergunte:

* O que aconteceu?
* Quando começou?
* O problema acontece sempre?
* Existe alguma mensagem de erro?
* O que mudou recentemente?

### 2. Reproduzir o problema

Quando possível, tente reproduzir o comportamento.

### 3. Coletar informações

Verifique:

* Sistema operacional.
* Hardware.
* Logs.
* Mensagens de erro.
* Configurações.

### 4. Formular hipóteses

Liste possíveis causas.

### 5. Testar uma hipótese por vez

Evite realizar várias alterações simultaneamente.

### 6. Aplicar a solução

Depois de identificar a causa provável.

### 7. Validar

Confirme se o problema realmente foi resolvido.

### 8. Documentar

Registre:

* Problema.
* Causa.
* Solução.
* Procedimentos realizados.

---

## 📝 Checklist de suporte — Windows

* [ ] Identificar versão e build do Windows.
* [ ] Identificar o problema relatado pelo usuário.
* [ ] Verificar mensagens de erro.
* [ ] Verificar Gerenciador de Tarefas.
* [ ] Verificar Gerenciador de Dispositivos.
* [ ] Verificar Windows Update.
* [ ] Verificar armazenamento.
* [ ] Verificar serviços relacionados ao problema.
* [ ] Consultar Event Viewer quando necessário.
* [ ] Executar ferramentas de diagnóstico apropriadas.
* [ ] Confirmar se existe backup antes de procedimentos de risco.
* [ ] Testar a solução.
* [ ] Confirmar com o usuário que o problema foi resolvido.
* [ ] Documentar o atendimento.

---

## 🎯 O que um profissional de suporte deve saber

Para trabalhar com suporte técnico em ambientes Windows, é importante dominar:

1. Configurações básicas do Windows.
2. Gerenciador de Tarefas.
3. Gerenciador de Dispositivos.
4. Windows Update.
5. Gerenciamento de usuários.
6. Permissões.
7. Armazenamento.
8. Diagnóstico de rede.
9. CMD.
10. PowerShell básico.
11. Serviços do Windows.
12. Event Viewer.
13. Segurança do Windows.
14. Drivers.
15. Troubleshooting.
16. Backup e recuperação.
17. Conceitos básicos de Active Directory e Microsoft Entra ID.

---

## 📚 Comandos essenciais

| Comando        | Função                                           |
| -------------- | ------------------------------------------------ |
| `winver`       | Verifica versão do Windows                       |
| `ipconfig`     | Exibe configurações de rede                      |
| `ping`         | Testa conectividade                              |
| `tracert`      | Mostra o caminho até um destino                  |
| `nslookup`     | Consulta DNS                                     |
| `hostname`     | Mostra o nome do computador                      |
| `whoami`       | Mostra o usuário atual                           |
| `systeminfo`   | Exibe informações do sistema                     |
| `chkdsk`       | Verifica o sistema de arquivos                   |
| `sfc /scannow` | Verifica arquivos protegidos do Windows          |
| `DISM`         | Gerencia/repara componentes da imagem do Windows |
| `cleanmgr`     | Abre a Limpeza de Disco                          |
| `devmgmt.msc`  | Abre o Gerenciador de Dispositivos               |
| `services.msc` | Abre os Serviços                                 |
| `eventvwr.msc` | Abre o Visualizador de Eventos                   |

---

## 🎓 Resumo rápido

```text
WINDOWS
│
├── Sistema
│   ├── Configurações
│   ├── Atualizações
│   └── Segurança
│
├── Hardware
│   ├── Gerenciador de Dispositivos
│   ├── Drivers
│   └── Armazenamento
│
├── Diagnóstico
│   ├── Gerenciador de Tarefas
│   ├── Event Viewer
│   ├── SFC
│   └── DISM
│
├── Rede
│   ├── ipconfig
│   ├── ping
│   ├── tracert
│   └── nslookup
│
├── Administração
│   ├── CMD
│   ├── PowerShell
│   ├── Serviços
│   └── Usuários e permissões
│
└── Troubleshooting
    ├── Identificar
    ├── Investigar
    ├── Testar
    ├── Resolver
    └── Documentar
```

> 💡 **Para suporte técnico:** conhecer Windows vai muito além de saber utilizar a interface gráfica. Um bom profissional precisa entender **como investigar problemas, utilizar ferramentas administrativas, interpretar informações do sistema e solucionar incidentes de maneira organizada e segura**.
