# Gerenciamento de Usuários

## 📚 Introdução

O **gerenciamento de usuários** consiste na criação, configuração, manutenção e controle das contas utilizadas para acessar computadores, sistemas e recursos de uma organização.

No **Suporte Técnico**, essa é uma atividade muito comum. Um chamado pode envolver:

* Criação de usuário.
* Alteração de senha.
* Bloqueio ou desbloqueio de conta.
* Problemas de login.
* Permissões de acesso.
* Acesso a arquivos e pastas.
* Acesso a sistemas corporativos.
* Configuração de contas em computadores.
* Problemas relacionados a domínio.

O gerenciamento adequado de usuários também é importante para **segurança da informação**, pois cada pessoa deve possuir apenas os acessos necessários para realizar suas atividades.

---

## 👤 1. O que é uma conta de usuário?

Uma **conta de usuário** é uma identidade utilizada para autenticar uma pessoa ou serviço em um sistema.

Uma conta normalmente possui:

* Nome de usuário.
* Senha ou outro método de autenticação.
* Identificador.
* Grupos.
* Permissões.
* Políticas de segurança.

De forma simplificada:

```text id="v7q8z1"
Usuário
   ↓
Autenticação
   ↓
Conta
   ↓
Grupos e permissões
   ↓
Recursos disponíveis
```

---

## 🔐 2. Autenticação x autorização

Esses dois conceitos são fundamentais para suporte técnico.

### Autenticação

Responde:

> **"Quem é você?"**

Exemplo:

```text id="f2g8ac"
Usuário + senha
       ↓
Identidade confirmada
```

### Autorização

Responde:

> **"O que você pode fazer?"**

Exemplo:

```text id="8v7n4m"
Usuário autenticado
       ↓
Permissões
       ↓
Pode acessar determinada pasta
```

### Resumo

| Conceito     | Pergunta                 |
| ------------ | ------------------------ |
| Autenticação | Quem é você?             |
| Autorização  | O que você pode acessar? |

---

## 👥 3. Tipos de contas

Dependendo do ambiente, podem existir diferentes tipos de contas.

### Conta de usuário comum

Utilizada por uma pessoa para realizar suas atividades.

### Conta administrativa

Possui privilégios elevados para realizar tarefas administrativas.

### Conta de serviço

Utilizada por aplicações e serviços para executar determinadas funções.

### Conta convidado

Possui acesso limitado e é destinada a situações específicas.

> ⚠️ Contas administrativas e de serviço devem ser tratadas com cuidado devido ao nível de privilégio que podem possuir.

---

## 🪟 4. Usuários no Windows

O Windows permite gerenciar contas localmente ou por meio de uma infraestrutura corporativa.

Em um computador pessoal, pode existir uma conta local:

```text id="s5b5xx"
Computador
│
├── Carolina
├── Técnico
└── Convidado
```

Em uma organização, os usuários podem ser administrados por serviços centralizados de identidade.

---

## ⚙️ 5. Gerenciamento de contas locais no Windows

É possível acessar algumas configurações de contas através de:

**Configurações → Contas**

Também existem ferramentas administrativas específicas.

### Usuários e Grupos Locais

Em versões do Windows que oferecem esse recurso, pode-se executar:

```cmd id="7j3xq1"
lusrmgr.msc
```

Essa ferramenta permite administrar:

* Usuários.
* Grupos.
* Membros dos grupos.
* Algumas propriedades das contas.

> ⚠️ Algumas edições do Windows, especialmente versões Home, possuem limitações para determinadas ferramentas administrativas.

---

## 👤 6. Criando uma conta local

O processo pode variar conforme a versão do Windows, mas normalmente envolve:

1. Abrir as configurações de contas.
2. Selecionar a opção para adicionar um usuário.
3. Escolher o tipo de conta.
4. Definir as credenciais.
5. Configurar permissões quando necessário.

### Boa prática

Crie a conta com **os privilégios mínimos necessários**.

Evite transformar todos os usuários em administradores.

---

## 🔑 7. Senhas

As senhas são um dos principais mecanismos de autenticação.

Uma política adequada deve considerar:

* Comprimento.
* Complexidade quando apropriado.
* Proteção contra reutilização.
* Bloqueio após tentativas malsucedidas, conforme a política.
* MFA quando disponível.
* Não compartilhamento de credenciais.

### O que o suporte nunca deve fazer

* Pedir a senha do usuário sem necessidade.
* Armazenar senhas em arquivos não protegidos.
* Compartilhar senhas por canais inseguros.
* Utilizar a mesma senha para várias contas administrativas.

---

## 🔄 8. Redefinição de senha

Um dos chamados mais comuns é:

> "Esqueci minha senha."

O procedimento depende do ambiente.

### Conta local

Pode ser necessário utilizar as ferramentas administrativas apropriadas.

### Ambiente corporativo

A redefinição pode ser realizada através do sistema de gerenciamento de identidade utilizado pela organização.

> 🔐 O suporte deve seguir o procedimento oficial de verificação de identidade antes de redefinir uma senha.

---

## 🔒 9. Bloqueio e desbloqueio de contas

Uma conta pode ser bloqueada por diferentes motivos:

* Muitas tentativas de login incorretas.
* Política de segurança.
* Ação administrativa.
* Suspeita de comprometimento.
* Conta desativada.

Antes de desbloquear uma conta, o suporte deve verificar o motivo do bloqueio.

---

## 🛡️ 10. Princípio do menor privilégio

O **Princípio do Menor Privilégio (Least Privilege)** determina que um usuário deve possuir apenas os privilégios necessários para executar suas atividades.

Exemplo inadequado:

```text id="8a6x4r"
Funcionário
   ↓
Administrador do computador
   ↓
Acesso irrestrito
```

Exemplo mais adequado:

```text id="2h4g8z"
Funcionário
   ↓
Conta padrão
   ↓
Acessos necessários para sua função
```

Isso reduz o impacto de:

* Malware.
* Erros humanos.
* Uso indevido.
* Comprometimento de credenciais.

---

## 👥 11. Grupos

Grupos permitem organizar usuários e atribuir permissões de maneira mais eficiente.

Em vez de conceder uma permissão individualmente:

```text id="a9m1sp"
Carolina → acesso
João     → acesso
Maria    → acesso
Pedro    → acesso
```

Podemos utilizar um grupo:

```text id="n4w7ex"
Grupo: Financeiro
│
├── Carolina
├── João
├── Maria
└── Pedro

Grupo → Permissão
```

Essa abordagem facilita a administração.

---

## 🗂️ 12. Permissões de arquivos e pastas

O acesso a arquivos e pastas pode ser controlado por permissões.

Exemplo:

```text id="e8z1da"
Pasta: Financeiro

Financeiro
    ↓
Grupo Financeiro
    ↓
Permissão de leitura e escrita
```

Um usuário que não pertence ao grupo pode não possuir acesso.

### Permissões comuns

* Leitura.
* Escrita.
* Modificação.
* Controle total.

> 💡 Em ambientes corporativos, normalmente é melhor conceder permissões a grupos do que configurar cada usuário individualmente.

---

## 🏢 13. Active Directory

O **Active Directory (AD)** é uma tecnologia da Microsoft utilizada para gerenciamento centralizado de identidades, computadores, grupos e recursos em ambientes corporativos.

Um ambiente Active Directory pode permitir que a organização gerencie:

* Usuários.
* Computadores.
* Grupos.
* Políticas.
* Permissões.
* Autenticação.
* Recursos compartilhados.

Exemplo:

```text id="j4t0wy"
Empresa
│
└── Domínio
    │
    ├── Usuários
    ├── Computadores
    ├── Grupos
    └── Políticas
```

---

## 🌐 14. Domínio

Em ambientes corporativos, computadores podem estar associados a um **domínio**.

Isso permite centralizar determinados aspectos de gerenciamento.

Exemplo:

```text id="k7u2cd"
Computador
      ↓
Domínio corporativo
      ↓
Autenticação
      ↓
Recursos da empresa
```

Um usuário pode utilizar suas credenciais corporativas para acessar diferentes recursos autorizados.

---

## 🏗️ 15. Organizational Units — OUs

No Active Directory, as **Organizational Units (OUs)** permitem organizar objetos.

Exemplo:

```text id="2h0w6d"
Empresa
│
├── TI
│   ├── Usuários
│   └── Computadores
│
├── Financeiro
│   ├── Usuários
│   └── Computadores
│
└── RH
    ├── Usuários
    └── Computadores
```

Essa organização pode facilitar a aplicação de políticas e a administração.

---

## 📜 16. Group Policy

A **Group Policy (GPO)** permite aplicar configurações de maneira centralizada em ambientes Windows corporativos.

Pode ser utilizada para configurar:

* Políticas de senha.
* Configurações de segurança.
* Restrições.
* Scripts.
* Configurações do Windows.
* Recursos do sistema.

Exemplo:

```text id="u5n6sa"
Política corporativa
       ↓
GPO
       ↓
Grupo/OU
       ↓
Computadores e usuários
```

---

## ☁️ 17. Microsoft Entra ID

O **Microsoft Entra ID** é o serviço de identidade e gerenciamento de acesso baseado em nuvem da Microsoft.

É importante diferenciá-lo do Active Directory tradicional.

De forma simplificada:

| Tecnologia                       | Foco                                 |
| -------------------------------- | ------------------------------------ |
| Active Directory Domain Services | Diretório e domínio tradicional      |
| Microsoft Entra ID               | Identidade e acesso baseado em nuvem |

O Entra ID é utilizado em ambientes com serviços como:

* Microsoft 365.
* Aplicações corporativas.
* Recursos de nuvem.
* Autenticação baseada em identidade.

---

## 🔐 18. MFA

**MFA (Multi-Factor Authentication)** adiciona uma camada adicional de autenticação.

Em vez de depender somente de uma senha:

```text id="g6v2hx"
Senha
  +
Segundo fator
  ↓
Acesso
```

O segundo fator pode envolver:

* Aplicativo autenticador.
* Código temporário.
* Chave de segurança.
* Biometria, dependendo da solução.

> 💡 MFA reduz o impacto de uma senha comprometida, embora não elimine todos os riscos.

---

## 🧑‍💻 19. Usuários no Linux

O Linux também possui um sistema de gerenciamento de usuários.

Comandos importantes:

### `whoami`

Mostra o usuário atual.

```bash id="g6h4zv"
whoami
```

### `id`

Exibe informações sobre o usuário e seus grupos.

```bash id="0k4v3s"
id
```

### `who`

Mostra usuários atualmente conectados.

```bash id="9s2h7d"
who
```

---

## ➕ 20. Criar usuários no Linux

O comando `useradd` pode ser utilizado para criar usuários.

Exemplo:

```bash id="4v7j0x"
sudo useradd usuario
```

Em algumas distribuições, `adduser` fornece uma interface mais amigável:

```bash id="x1f6yd"
sudo adduser usuario
```

---

## 🔑 21. Alterar senha no Linux

O comando `passwd` pode ser utilizado para alterar a senha.

```bash id="x0a9f7"
passwd
```

Para alterar a senha de outro usuário, quando autorizado:

```bash id="c6g2nz"
sudo passwd usuario
```

---

## 👥 22. Grupos no Linux

Criar um grupo:

```bash id="3r8c4h"
sudo groupadd suporte
```

Adicionar um usuário a um grupo:

```bash id="7j1x8v"
sudo usermod -aG suporte usuario
```

Verificar grupos:

```bash id="m3q9az"
groups usuario
```

> ⚠️ O parâmetro `-aG` é importante para adicionar o usuário ao grupo sem substituir os grupos suplementares existentes.

---

## 🔒 23. Bloquear e desbloquear usuários no Linux

Para bloquear uma conta:

```bash id="q4n7mw"
sudo passwd -l usuario
```

Para desbloquear:

```bash id="v5b1pk"
sudo passwd -u usuario
```

Esses comandos devem ser utilizados de acordo com as políticas administrativas do ambiente.

---

## 🗑️ 24. Remover usuários no Linux

Para remover uma conta:

```bash id="e7y2qp"
sudo userdel usuario
```

Em algumas situações, também pode ser necessário remover o diretório pessoal, dependendo do procedimento adotado.

> ⚠️ A remoção de uma conta pode afetar arquivos e processos associados ao usuário. Sempre verifique a necessidade de preservar os dados antes de realizar a operação.

---

## 📄 25. Arquivos importantes no Linux

Em sistemas Linux tradicionais, algumas informações de usuários são armazenadas em arquivos como:

```text id="0d1v9c"
/etc/passwd
/etc/shadow
/etc/group
```

### `/etc/passwd`

Contém informações básicas das contas.

### `/etc/shadow`

Armazena informações relacionadas às credenciais de autenticação de maneira protegida.

### `/etc/group`

Contém informações sobre grupos.

> 🔐 O arquivo `/etc/shadow` possui informações sensíveis e deve ser protegido contra acesso indevido.

---

## 🔍 26. Diagnóstico de problemas de login

Quando um usuário não consegue entrar no sistema, siga uma sequência lógica.

### Windows

Verifique:

* Nome de usuário.
* Senha.
* Status da conta.
* Conectividade.
* Domínio.
* Bloqueio da conta.
* MFA.
* Mensagem de erro.
* Eventos de autenticação.

### Linux

Verifique:

* Usuário correto.
* Senha.
* Status da conta.
* Permissões.
* Grupos.
* SSH, caso o acesso seja remoto.
* Logs de autenticação.

---

## 🧪 27. Troubleshooting de acesso

Uma abordagem recomendada:

### 1. Identifique o recurso

O usuário não consegue acessar:

* Computador?
* Sistema?
* Pasta?
* Servidor?
* VPN?
* E-mail?

### 2. Identifique a identidade

Verifique:

* Usuário.
* Grupo.
* Domínio.
* Método de autenticação.

### 3. Verifique a autorização

Pergunte:

> O usuário deveria ter acesso a esse recurso?

### 4. Verifique configurações

Analise:

* Permissões.
* Políticas.
* Conta bloqueada.
* Expiração.
* MFA.

### 5. Teste

Realize o procedimento adequado.

### 6. Documente

Registre o problema e a solução.

---

## 🛡️ 28. Princípio do Zero Trust

O conceito de **Zero Trust** parte da ideia de que o acesso não deve ser confiado automaticamente apenas porque o usuário está dentro da rede corporativa.

Uma abordagem simplificada:

```text id="5tq6ae"
Usuário solicita acesso
        ↓
Verificar identidade
        ↓
Verificar dispositivo
        ↓
Verificar contexto
        ↓
Verificar autorização
        ↓
Conceder acesso necessário
```

Esse conceito é especialmente importante em ambientes modernos de cloud e trabalho remoto.

---

## 🚨 29. Segurança no gerenciamento de usuários

Um profissional de suporte deve:

* Nunca compartilhar credenciais.
* Verificar a identidade antes de redefinir senhas.
* Evitar privilégios administrativos desnecessários.
* Utilizar grupos para facilitar o gerenciamento.
* Revogar acessos quando eles não forem mais necessários.
* Não criar contas sem autorização.
* Não ignorar políticas de segurança.
* Registrar alterações administrativas.
* Utilizar MFA quando disponível.
* Seguir o princípio do menor privilégio.

---

## 🔄 30. Ciclo de vida de uma conta

O gerenciamento de usuários não termina na criação da conta.

Um ciclo comum é:

```text id="2w5f0d"
Criação
   ↓
Configuração
   ↓
Utilização
   ↓
Alterações
   ↓
Revisão de acessos
   ↓
Bloqueio/Desativação
   ↓
Remoção
```

Esse processo é especialmente importante em organizações.

Quando um funcionário entra na empresa:

**Onboarding**

Quando muda de função:

**Alteração de acessos**

Quando deixa a empresa:

**Offboarding**

---

## 🏢 31. Onboarding

Durante o onboarding, o suporte pode participar de atividades como:

* Criação da conta.
* Configuração do computador.
* Inclusão em grupos.
* Configuração de e-mail.
* Acesso a sistemas.
* Configuração de MFA.
* Instalação de aplicativos.
* Configuração de VPN.

Sempre seguindo as políticas da organização.

---

## 🚪 32. Offboarding

Quando um funcionário deixa a empresa, é importante garantir que os acessos sejam tratados corretamente.

Possíveis ações:

* Bloquear conta.
* Revogar sessões.
* Remover acessos.
* Desativar MFA quando apropriado.
* Recuperar equipamentos.
* Transferir propriedade de dados conforme política.
* Preservar informações necessárias.
* Registrar o procedimento.

> ⚠️ O offboarding deve ser coordenado com RH, segurança e outras áreas responsáveis, conforme os processos internos da organização.

---

## 📝 Checklist de gerenciamento de usuários

### Criação

* [ ] Confirmar autorização para criação da conta.
* [ ] Confirmar identidade e função do usuário.
* [ ] Criar conta.
* [ ] Definir grupos apropriados.
* [ ] Aplicar somente as permissões necessárias.
* [ ] Configurar MFA quando disponível.
* [ ] Testar acesso.

### Problemas de acesso

* [ ] Identificar usuário.
* [ ] Identificar recurso.
* [ ] Verificar autenticação.
* [ ] Verificar autorização.
* [ ] Verificar grupos.
* [ ] Verificar bloqueios.
* [ ] Verificar políticas.
* [ ] Testar novamente.
* [ ] Documentar.

### Desligamento

* [ ] Confirmar autorização para desativação.
* [ ] Bloquear conta.
* [ ] Revogar acessos conforme procedimento.
* [ ] Preservar dados necessários.
* [ ] Recuperar equipamentos quando aplicável.
* [ ] Documentar o processo.

---

## 🎯 O que um profissional de suporte deve saber

Para trabalhar com gerenciamento de usuários, é importante compreender:

1. Diferença entre autenticação e autorização.
2. Contas locais.
3. Usuários e grupos.
4. Permissões.
5. Princípio do menor privilégio.
6. Redefinição de senhas.
7. Bloqueio e desbloqueio de contas.
8. Active Directory.
9. Domínios.
10. Organizational Units.
11. Group Policy.
12. Microsoft Entra ID.
13. MFA.
14. Conceitos básicos de Zero Trust.
15. Gerenciamento de usuários no Linux.
16. Troubleshooting de problemas de login.
17. Onboarding e offboarding.
18. Boas práticas de segurança.

---

## 📚 Comandos essenciais

### Windows

| Comando          | Função                                                           |
| ---------------- | ---------------------------------------------------------------- |
| `lusrmgr.msc`    | Gerenciamento de usuários e grupos locais em edições compatíveis |
| `whoami`         | Identifica o usuário atual                                       |
| `whoami /groups` | Exibe grupos do usuário atual                                    |
| `net user`       | Consulta e gerencia contas locais                                |
| `net localgroup` | Consulta e gerencia grupos locais                                |

### Linux

| Comando    | Função                                                      |
| ---------- | ----------------------------------------------------------- |
| `whoami`   | Mostra o usuário atual                                      |
| `id`       | Mostra UID, GID e grupos                                    |
| `who`      | Mostra usuários conectados                                  |
| `useradd`  | Cria usuários                                               |
| `adduser`  | Cria usuários em distribuições que oferecem esse utilitário |
| `passwd`   | Gerencia senhas                                             |
| `usermod`  | Modifica contas                                             |
| `userdel`  | Remove contas                                               |
| `groupadd` | Cria grupos                                                 |
| `groups`   | Mostra grupos                                               |
| `sudo`     | Executa comandos com privilégios elevados                   |

---

## 🧠 Resumo rápido

```text id="7x4z3a"
GERENCIAMENTO DE USUÁRIOS
│
├── Autenticação
│   └── Quem é você?
│
├── Autorização
│   └── O que você pode acessar?
│
├── Contas
│   ├── Usuário
│   ├── Administrador
│   └── Serviço
│
├── Grupos
│   └── Permissões centralizadas
│
├── Segurança
│   ├── Menor privilégio
│   ├── MFA
│   └── Zero Trust
│
├── Windows
│   ├── Contas locais
│   ├── Active Directory
│   ├── GPO
│   └── Entra ID
│
├── Linux
│   ├── Usuários
│   ├── Grupos
│   ├── sudo
│   └── Permissões
│
└── Ciclo de vida
    ├── Onboarding
    ├── Alterações
    ├── Revisão
    └── Offboarding
```

> 💡 **Para suporte técnico:** gerenciamento de usuários não é apenas criar contas e redefinir senhas. O profissional precisa entender **identidade, autenticação, autorização, grupos, permissões e segurança**, garantindo que cada usuário tenha acesso aos recursos necessários — e nada além do necessário.
