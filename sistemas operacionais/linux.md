# Linux

## 📚 Introdução

O **Linux** é um sistema operacional de código aberto baseado no kernel Linux. É amplamente utilizado em servidores, computadores pessoais, dispositivos embarcados, ambientes de nuvem e infraestrutura de TI.

Para profissionais de **Suporte Técnico**, conhecer Linux é um diferencial importante, especialmente para trabalhar com servidores, redes, cloud computing, desenvolvimento e ambientes corporativos.

Este guia apresenta os principais conceitos e comandos que um profissional iniciante deve conhecer.

---

## 🐧 1. O que é Linux?

Tecnicamente, **Linux é o kernel**, ou seja, o componente central responsável pela comunicação entre o hardware e o restante do sistema.

Quando falamos em sistemas como Ubuntu, Debian ou Fedora, estamos normalmente falando de **distribuições Linux**, que combinam o kernel com ferramentas, bibliotecas, aplicativos e sistemas de gerenciamento.

Exemplos de distribuições:

* Ubuntu
* Debian
* Fedora
* Linux Mint
* Arch Linux
* openSUSE
* Red Hat Enterprise Linux (RHEL)
* Rocky Linux
* AlmaLinux

---

## 🧩 2. O que é uma distribuição Linux?

Uma **distribuição Linux (distro)** é um sistema baseado no kernel Linux acompanhado de outros componentes necessários para utilização do sistema.

Uma distribuição geralmente inclui:

* Kernel Linux.
* Gerenciador de pacotes.
* Bibliotecas.
* Ferramentas administrativas.
* Shell.
* Interface gráfica, quando aplicável.
* Aplicativos.

### Exemplos

```text
Ubuntu
│
├── Kernel Linux
├── GNU utilities
├── APT
├── Shell
├── Desktop Environment
└── Aplicativos
```

---

## 🖥️ 3. Interface gráfica x Terminal

Linux pode ser utilizado com uma interface gráfica ou diretamente pelo terminal.

### Interface gráfica

Ambientes conhecidos:

* GNOME
* KDE Plasma
* Xfce
* Cinnamon

### Terminal

O terminal permite executar comandos diretamente.

Exemplo:

```bash
ls
```

O terminal é extremamente importante para administração e suporte de sistemas Linux.

> 💡 Para quem trabalha com suporte técnico, aprender a utilizar o terminal é uma das habilidades mais importantes no Linux.

---

## ⌨️ 4. Shell

O **shell** é um programa que interpreta comandos digitados pelo usuário.

Um dos shells mais utilizados é o **Bash (Bourne Again Shell)**.

Outros exemplos:

* Zsh
* Fish
* Dash

Para descobrir qual shell está sendo utilizado:

```bash
echo $SHELL
```

---

## 📁 5. Sistema de arquivos Linux

O Linux utiliza uma estrutura de diretórios hierárquica.

Ao contrário do Windows, não existem unidades como `C:` e `D:` organizando o sistema dessa maneira.

O sistema começa no diretório raiz:

```text
/
```

Estrutura simplificada:

```text
/
├── bin
├── boot
├── dev
├── etc
├── home
├── lib
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin
├── srv
├── tmp
├── usr
└── var
```

---

## 📂 6. Diretórios importantes

### `/`

É o diretório raiz do sistema.

### `/home`

Contém os diretórios pessoais dos usuários.

Exemplo:

```text
/home/carolina
```

### `/root`

É o diretório pessoal do usuário `root`.

Não deve ser confundido com `/`.

### `/etc`

Armazena arquivos de configuração do sistema e de diversos serviços.

### `/var`

Armazena dados que podem mudar durante a execução do sistema.

Exemplos:

* Logs.
* Cache.
* Filas.
* Dados de serviços.

### `/tmp`

Utilizado para arquivos temporários.

### `/usr`

Contém grande parte dos programas, bibliotecas e recursos utilizados pelo sistema.

### `/bin`

Contém programas essenciais para o funcionamento básico do sistema em distribuições que mantêm esse diretório separado.

### `/dev`

Contém representações de dispositivos utilizados pelo sistema.

### `/proc`

É um sistema de arquivos virtual que fornece informações sobre processos e o kernel.

---

## 🧭 7. Navegação pelo terminal

### `pwd`

Mostra o diretório atual.

```bash
pwd
```

### `ls`

Lista arquivos e diretórios.

```bash
ls
```

Para obter mais detalhes:

```bash
ls -l
```

Incluindo arquivos ocultos:

```bash
ls -la
```

### `cd`

Altera o diretório atual.

```bash
cd /home
```

Voltar um nível:

```bash
cd ..
```

Voltar para o diretório pessoal:

```bash
cd ~
```

---

## 📄 8. Criar, copiar, mover e excluir arquivos

### `touch`

Cria um arquivo vazio.

```bash
touch arquivo.txt
```

### `mkdir`

Cria um diretório.

```bash
mkdir documentos
```

### `cp`

Copia arquivos.

```bash
cp arquivo.txt backup.txt
```

Copiar um diretório:

```bash
cp -r documentos backup
```

### `mv`

Move ou renomeia arquivos.

```bash
mv arquivo.txt documentos/
```

Renomear:

```bash
mv antigo.txt novo.txt
```

### `rm`

Remove arquivos.

```bash
rm arquivo.txt
```

Remover um diretório vazio:

```bash
rmdir documentos
```

> ⚠️ Tenha muito cuidado com `rm`, especialmente quando utilizado com privilégios administrativos. A exclusão pode ser permanente.

---

## 📖 9. Visualizar arquivos

### `cat`

Exibe o conteúdo de um arquivo.

```bash
cat arquivo.txt
```

### `less`

Permite visualizar arquivos maiores página por página.

```bash
less arquivo.log
```

### `head`

Mostra o início do arquivo.

```bash
head arquivo.txt
```

### `tail`

Mostra o final do arquivo.

```bash
tail arquivo.log
```

Para acompanhar alterações em tempo real:

```bash
tail -f arquivo.log
```

Esse comando é especialmente útil para acompanhar **logs**.

---

## 🔎 10. Procurar arquivos

### `find`

Procura arquivos e diretórios.

```bash
find /home -name "arquivo.txt"
```

### `locate`

Em sistemas que possuem a ferramenta configurada:

```bash
locate arquivo.txt
```

> 💡 `find` realiza uma busca no sistema de arquivos, enquanto `locate` normalmente utiliza um banco de dados previamente indexado.

---

## 🔍 11. Procurar texto

### `grep`

Procura padrões dentro de arquivos ou da saída de comandos.

Exemplo:

```bash
grep "error" sistema.log
```

Ignorando diferenças entre maiúsculas e minúsculas:

```bash
grep -i "error" sistema.log
```

O `grep` é extremamente útil para análise de logs.

---

## 🔗 12. Pipes

O caractere `|` permite enviar a saída de um comando para outro.

Exemplo:

```bash
ps aux | grep nginx
```

Nesse caso:

1. `ps aux` lista processos.
2. `grep nginx` filtra os resultados.

Outro exemplo:

```bash
ls -l | grep ".txt"
```

---

## 🔐 13. Usuários

O Linux utiliza contas de usuário para controlar acesso aos recursos.

Um sistema pode possuir:

* Usuários comuns.
* Usuários administrativos.
* Usuários de serviços.

Para descobrir o usuário atual:

```bash
whoami
```

Para visualizar informações do usuário:

```bash
id
```

---

## 👑 14. Root

O `root` é o usuário administrativo com privilégios extremamente elevados.

O usuário root pode realizar alterações críticas no sistema.

Por isso:

> ⚠️ Evite utilizar `root` diretamente para tarefas comuns.

Em muitas distribuições, utiliza-se `sudo` para executar comandos específicos com privilégios administrativos.

---

## 🔑 15. Sudo

O `sudo` permite executar determinados comandos com privilégios elevados.

Exemplo:

```bash
sudo apt update
```

O sistema pode solicitar a senha do usuário.

O uso de `sudo` deve ser realizado com cuidado, pois comandos administrativos podem modificar componentes importantes do sistema.

---

## 👥 16. Grupos

Os usuários podem pertencer a grupos.

Os grupos facilitam o gerenciamento de permissões.

Exemplo:

```bash
groups
```

Para verificar os grupos de um usuário:

```bash
groups usuario
```

---

## 🛡️ 17. Permissões

As permissões determinam quem pode:

* Ler um arquivo.
* Escrever em um arquivo.
* Executar um arquivo.

As três permissões principais são:

| Permissão | Significado        |
| --------- | ------------------ |
| `r`       | Read — leitura     |
| `w`       | Write — escrita    |
| `x`       | Execute — execução |

As permissões são aplicadas a:

* Proprietário (`user`)
* Grupo (`group`)
* Outros (`others`)

Exemplo:

```text
-rwxr-xr--
```

Pode ser interpretado como:

```text
Owner  → rwx
Group  → r-x
Others → r--
```

---

## 🔧 18. chmod

O comando `chmod` altera permissões.

Exemplo:

```bash
chmod +x script.sh
```

Isso adiciona permissão de execução ao arquivo.

Também é possível utilizar representação numérica:

```bash
chmod 755 script.sh
```

De forma simplificada:

```text
7 → rwx
5 → r-x
5 → r-x
```

---

## 👤 19. chown

O comando `chown` altera o proprietário de um arquivo ou diretório.

Exemplo:

```bash
sudo chown usuario arquivo.txt
```

Também pode alterar proprietário e grupo:

```bash
sudo chown usuario:grupo arquivo.txt
```

---

## 💽 20. Armazenamento

O Linux possui diversos comandos para verificar armazenamento.

### `df`

Mostra espaço utilizado e disponível nos sistemas de arquivos.

```bash
df -h
```

### `du`

Mostra o espaço ocupado por arquivos e diretórios.

```bash
du -sh documentos
```

### `lsblk`

Lista dispositivos de armazenamento e partições.

```bash
lsblk
```

Esses comandos são úteis para diagnosticar problemas relacionados a **falta de espaço e discos**.

---

## 🧠 21. Processos

Um **processo** é uma instância de um programa em execução.

### `ps`

Exibe processos.

```bash
ps
```

Para uma visão mais completa:

```bash
ps aux
```

### `top`

Mostra processos e utilização de recursos em tempo real.

```bash
top
```

### `htop`

Uma alternativa mais amigável ao `top`, quando instalada:

```bash
htop
```

---

## 🛑 22. Encerrar processos

### `kill`

Envia um sinal para um processo.

```bash
kill PID
```

O `PID` é o identificador do processo.

Em situações específicas:

```bash
kill -9 PID
```

> ⚠️ O `kill -9` força a finalização do processo e deve ser utilizado somente quando necessário.

---

## ⚙️ 23. Serviços

Em muitas distribuições modernas, o **systemd** é utilizado para gerenciar serviços.

### Verificar o status

```bash
systemctl status nome-do-servico
```

### Iniciar

```bash
sudo systemctl start nome-do-servico
```

### Parar

```bash
sudo systemctl stop nome-do-servico
```

### Reiniciar

```bash
sudo systemctl restart nome-do-servico
```

### Verificar se inicia automaticamente

```bash
systemctl is-enabled nome-do-servico
```

---

## 📜 24. Logs

Logs são fundamentais para troubleshooting.

Dependendo da distribuição e configuração, podem existir arquivos em:

```text
/var/log/
```

Alguns exemplos:

```bash
ls /var/log
```

Em sistemas que utilizam `systemd`, o `journalctl` pode ser utilizado.

```bash
journalctl
```

Para visualizar mensagens recentes:

```bash
journalctl -n 50
```

Para acompanhar logs:

```bash
journalctl -f
```

> 💡 Ao investigar um problema, procure relacionar o horário do log com o momento em que o incidente ocorreu.

---

## 🌐 25. Redes

Conhecimentos básicos de rede são essenciais para suporte Linux.

### `ip`

Exibe informações das interfaces de rede.

```bash
ip addr
```

Também pode ser utilizado para consultar rotas:

```bash
ip route
```

### `ping`

Testa conectividade:

```bash
ping 8.8.8.8
```

### `curl`

Pode ser utilizado para realizar requisições HTTP e testar serviços.

```bash
curl https://example.com
```

### `ss`

Exibe conexões e portas de rede.

```bash
ss -tuln
```

---

## 🌎 26. DNS

O DNS traduz nomes de domínio em endereços IP.

Ferramentas comuns para diagnóstico incluem:

```bash
nslookup google.com
```

ou:

```bash
dig google.com
```

O `dig` pode não estar instalado por padrão em todas as distribuições.

---

## 📦 27. Gerenciadores de pacotes

Uma das principais diferenças entre distribuições Linux é o sistema de gerenciamento de pacotes.

### Debian / Ubuntu

Utilizam principalmente o **APT**.

Atualizar a lista de pacotes:

```bash
sudo apt update
```

Atualizar pacotes:

```bash
sudo apt upgrade
```

Instalar um pacote:

```bash
sudo apt install nome-do-pacote
```

Remover:

```bash
sudo apt remove nome-do-pacote
```

### Fedora

Utiliza o **DNF**.

Exemplo:

```bash
sudo dnf install nome-do-pacote
```

### Arch Linux

Utiliza principalmente o **Pacman**.

Exemplo:

```bash
sudo pacman -S nome-do-pacote
```

> 💡 Antes de executar comandos de instalação ou remoção, confirme qual distribuição e gerenciador de pacotes estão sendo utilizados.

---

## 🐚 28. Variáveis de ambiente

Variáveis de ambiente armazenam informações utilizadas por processos e programas.

Para visualizar uma variável:

```bash
echo $PATH
```

Para visualizar várias variáveis:

```bash
printenv
```

O `PATH` é especialmente importante porque define diretórios onde o shell procura executáveis.

---

## 🔗 29. Links simbólicos

Um **link simbólico** funciona como uma referência para outro arquivo ou diretório.

Criar um:

```bash
ln -s arquivo_original link
```

Verificar:

```bash
ls -l
```

Links simbólicos são bastante utilizados em sistemas Linux.

---

## 📝 30. Editor de texto

Profissionais de suporte frequentemente precisam editar arquivos de configuração.

Editores comuns:

* Nano
* Vim
* Emacs

### Nano

É uma opção amigável para iniciantes.

```bash
nano arquivo.conf
```

O `nano` é especialmente útil para quem está começando a trabalhar com administração Linux.

---

## 🗜️ 31. Compactação

### `tar`

É muito utilizado para criar e extrair arquivos compactados.

Criar um arquivo `.tar`:

```bash
tar -cvf backup.tar documentos/
```

Extrair:

```bash
tar -xvf backup.tar
```

Para arquivos `.tar.gz`:

```bash
tar -czvf backup.tar.gz documentos/
```

Extrair:

```bash
tar -xzvf backup.tar.gz
```

---

## 🔄 32. Processos em segundo plano

Um comando pode ser executado em segundo plano utilizando `&`.

Exemplo:

```bash
comando &
```

O comando `jobs` mostra trabalhos associados ao shell atual:

```bash
jobs
```

---

## 🔌 33. SSH

O **SSH (Secure Shell)** é utilizado para acessar sistemas remotamente de forma segura.

Exemplo:

```bash
ssh usuario@servidor
```

É uma ferramenta extremamente importante em:

* Administração de servidores.
* Cloud computing.
* DevOps.
* Suporte remoto.
* Infraestrutura.

> 🔐 Nunca compartilhe senhas ou chaves privadas. Em ambientes corporativos, siga as políticas de segurança para acesso remoto.

---

## 🧪 34. Troubleshooting no Linux

Ao investigar um problema, utilize uma abordagem estruturada.

### 1. Identifique o problema

Pergunte:

* O que não está funcionando?
* Quando começou?
* O problema acontece sempre?
* Houve alguma alteração recente?

### 2. Colete informações

Verifique:

* Sistema operacional.
* Hardware.
* Processos.
* Serviços.
* Logs.
* Rede.
* Armazenamento.

### 3. Formule hipóteses

Liste as possíveis causas.

### 4. Teste

Execute testes específicos para confirmar ou eliminar hipóteses.

### 5. Corrija

Aplique a solução adequada.

### 6. Valide

Confirme se o problema foi resolvido.

### 7. Documente

Registre:

* Sintoma.
* Causa.
* Procedimentos.
* Solução.

---

## 🩺 35. Exemplos de diagnóstico

### Problema: sistema sem espaço

Verifique:

```bash
df -h
```

Depois identifique diretórios que ocupam muito espaço:

```bash
du -sh /*
```

> ⚠️ O segundo comando pode exigir permissões e pode gerar mensagens de acesso negado. Em sistemas de produção, utilize-o com cuidado.

---

### Problema: serviço não está funcionando

Verifique:

```bash
systemctl status nome-do-servico
```

Depois consulte os logs:

```bash
journalctl -u nome-do-servico
```

---

### Problema: servidor não responde pela rede

Verifique:

```bash
ip addr
```

Depois:

```bash
ip route
```

Teste conectividade:

```bash
ping endereço
```

Verifique portas:

```bash
ss -tuln
```

---

## 🔐 36. Boas práticas de segurança

No suporte Linux:

* Evite utilizar `root` sem necessidade.
* Utilize `sudo` de forma consciente.
* Não execute comandos desconhecidos sem entender sua finalidade.
* Mantenha o sistema atualizado.
* Utilize senhas fortes.
* Proteja chaves SSH.
* Não compartilhe credenciais.
* Restrinja permissões ao mínimo necessário.
* Monitore logs.
* Faça backups.
* Não desabilite mecanismos de segurança sem necessidade.

---

## 🧑‍💻 37. Linux em servidores e cloud

Linux possui grande presença em ambientes de infraestrutura.

É comum encontrá-lo em:

* Servidores web.
* Bancos de dados.
* Servidores de arquivos.
* Containers.
* Máquinas virtuais.
* Ambientes AWS.
* Ambientes Azure.
* Ambientes Google Cloud.
* Sistemas de monitoramento.
* Plataformas de desenvolvimento.

Por isso, conhecimento de Linux pode complementar habilidades em **AWS, redes, segurança, DevOps e suporte técnico**.

---

## 📋 Checklist de troubleshooting

* [ ] Identificar a distribuição Linux.
* [ ] Verificar versão do sistema.
* [ ] Identificar o usuário atual.
* [ ] Verificar utilização de CPU e memória.
* [ ] Verificar armazenamento disponível.
* [ ] Verificar processos.
* [ ] Verificar serviços.
* [ ] Consultar logs.
* [ ] Verificar interfaces de rede.
* [ ] Testar conectividade.
* [ ] Verificar permissões.
* [ ] Identificar alterações recentes.
* [ ] Testar uma hipótese por vez.
* [ ] Validar a solução.
* [ ] Documentar o procedimento.

---

## 🎯 O que um profissional de suporte deve saber

Para começar a trabalhar com Linux, é importante saber:

1. Navegar pelo terminal.
2. Utilizar Bash básico.
3. Entender a estrutura de diretórios.
4. Trabalhar com arquivos e diretórios.
5. Entender permissões.
6. Gerenciar usuários e grupos.
7. Utilizar `sudo`.
8. Instalar e atualizar pacotes.
9. Gerenciar processos.
10. Gerenciar serviços.
11. Consultar logs.
12. Diagnosticar problemas de rede.
13. Utilizar SSH.
14. Monitorar armazenamento.
15. Interpretar mensagens de erro.
16. Aplicar uma metodologia de troubleshooting.

---

## 📚 Comandos essenciais

| Comando      | Função                                    |
| ------------ | ----------------------------------------- |
| `pwd`        | Mostra o diretório atual                  |
| `ls`         | Lista arquivos e diretórios               |
| `cd`         | Navega entre diretórios                   |
| `mkdir`      | Cria diretórios                           |
| `touch`      | Cria arquivos                             |
| `cp`         | Copia arquivos                            |
| `mv`         | Move ou renomeia                          |
| `rm`         | Remove arquivos                           |
| `cat`        | Exibe conteúdo                            |
| `less`       | Visualiza arquivos                        |
| `grep`       | Pesquisa texto                            |
| `find`       | Procura arquivos                          |
| `chmod`      | Altera permissões                         |
| `chown`      | Altera proprietário                       |
| `sudo`       | Executa comandos com privilégios elevados |
| `ps`         | Lista processos                           |
| `top`        | Monitora processos                        |
| `kill`       | Envia sinais para processos               |
| `systemctl`  | Gerencia serviços                         |
| `journalctl` | Consulta logs do systemd                  |
| `df`         | Verifica espaço em disco                  |
| `du`         | Verifica uso de espaço                    |
| `lsblk`      | Lista dispositivos de armazenamento       |
| `ip`         | Consulta configurações de rede            |
| `ping`       | Testa conectividade                       |
| `curl`       | Realiza requisições                       |
| `ss`         | Consulta conexões e portas                |
| `ssh`        | Acessa sistemas remotamente               |
| `apt`        | Gerencia pacotes Debian/Ubuntu            |
| `dnf`        | Gerencia pacotes Fedora                   |
| `pacman`     | Gerencia pacotes Arch                     |

---

## 🧠 Resumo rápido

```text
LINUX
│
├── Terminal
│   ├── Bash
│   ├── Comandos
│   └── Scripts
│
├── Sistema de arquivos
│   ├── /
│   ├── /home
│   ├── /etc
│   ├── /var
│   └── /tmp
│
├── Administração
│   ├── Usuários
│   ├── Grupos
│   ├── Permissões
│   └── sudo
│
├── Processos
│   ├── ps
│   ├── top
│   └── kill
│
├── Serviços
│   ├── systemctl
│   └── systemd
│
├── Logs
│   ├── /var/log
│   └── journalctl
│
├── Rede
│   ├── ip
│   ├── ping
│   ├── curl
│   ├── ss
│   └── SSH
│
└── Pacotes
    ├── APT
    ├── DNF
    └── Pacman
```

> 💡 **Para suporte técnico:** você não precisa começar dominando Linux inteiro. Priorize **terminal, arquivos, permissões, usuários, processos, serviços, logs, rede e troubleshooting**. Esses conhecimentos formam uma base sólida para trabalhar posteriormente com servidores, cloud e infraestrutura.
