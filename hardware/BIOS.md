# BIOS: O que é, para que serve e como utilizar no Suporte Técnico

## Introdução

Ao trabalhar com suporte técnico, um dos primeiros conceitos que você precisa dominar é a BIOS. Ela está presente em praticamente todos os computadores e desempenha um papel fundamental durante a inicialização do sistema.

Entender como a BIOS funciona permite diagnosticar problemas de hardware, alterar configurações importantes do computador e auxiliar usuários em situações que vão desde a instalação de um sistema operacional até a solução de falhas de inicialização.

Neste artigo, você aprenderá o que é a BIOS, suas principais funções, casos de uso e boas práticas para utilizá-la no dia a dia do suporte técnico.

---

# O que é BIOS?

BIOS significa **Basic Input/Output System** (Sistema Básico de Entrada e Saída).

Trata-se de um firmware armazenado em um chip na placa-mãe que é executado assim que o computador é ligado.

Sua principal função é verificar se os componentes de hardware estão funcionando corretamente e preparar o sistema para carregar o sistema operacional, como Windows, Linux ou macOS.

Sem a BIOS (ou sua sucessora moderna, a UEFI), o computador não conseguiria iniciar.

---

# Como a BIOS funciona?

Quando o usuário pressiona o botão de energia, ocorre a seguinte sequência:

1. O computador é ligado.
2. A BIOS inicia automaticamente.
3. É executado o POST (Power-On Self-Test).
4. Os componentes de hardware são verificados:
   - Processador (CPU)
   - Memória RAM
   - Disco rígido ou SSD
   - Placa de vídeo
   - Teclado
   - Outros dispositivos conectados
5. Caso não sejam encontrados erros críticos, a BIOS procura um dispositivo de inicialização.
6. O sistema operacional é carregado.

---

# O que é POST?

POST significa **Power-On Self-Test**.

É uma rotina de diagnóstico executada pela BIOS logo após a inicialização.

Durante o POST, a BIOS verifica se os componentes essenciais estão funcionando.

Caso algum problema seja encontrado, o computador pode:

- Exibir mensagens de erro na tela;
- Emitir sinais sonoros (beeps);
- Apresentar LEDs de diagnóstico na placa-mãe.

---

# BIOS x UEFI

Atualmente, a maioria dos computadores modernos utiliza UEFI (Unified Extensible Firmware Interface), considerada a evolução da BIOS tradicional.

| BIOS | UEFI |
|--------|--------|
| Interface simples | Interface gráfica moderna |
| Suporte limitado a discos grandes | Suporte a discos maiores que 2 TB |
| Inicialização mais lenta | Inicialização mais rápida |
| Menos recursos de segurança | Secure Boot e recursos avançados |
| Tecnologia mais antiga | Tecnologia atual |

Embora tecnicamente sejam diferentes, muitos profissionais continuam utilizando o termo "BIOS" para se referir à tela de configuração do firmware do computador.

---

# Como acessar a BIOS

O acesso ocorre durante a inicialização do computador.

As teclas mais comuns são:

| Fabricante | Tecla |
|-------------|---------|
| Dell | F2 |
| HP | F10 ou Esc |
| Lenovo | F1 ou F2 |
| ASUS | F2 ou Del |
| Acer | F2 |
| Gigabyte | Del |
| MSI | Del |

### Procedimento

1. Ligue ou reinicie o computador.
2. Pressione repetidamente a tecla correspondente.
3. Aguarde a abertura da tela de configuração.

---

# Principais configurações encontradas na BIOS

## Data e Hora

Permite configurar o relógio interno do computador.

### Sintoma comum

- Data e hora incorretas após desligar o PC.

### Possível causa

- Bateria CMOS descarregada.

---

## Ordem de Boot

Define qual dispositivo será utilizado para iniciar o sistema.

### Exemplos

- SSD
- HD
- Pendrive
- DVD

Muito utilizada durante:

- Instalação do Windows;
- Instalação de Linux;
- Recuperação de sistemas.

---

## Virtualização

Permite habilitar tecnologias como:

- Intel VT-x
- AMD-V

Necessária para:

- Máquinas virtuais;
- Docker Desktop;
- Hyper-V;
- Android Studio.

---

## Secure Boot

Recurso de segurança que impede a execução de softwares não autorizados durante a inicialização.

Comumente utilizado em:

- Windows 11;
- Ambientes corporativos.

---

## Monitoramento de Hardware

Exibe informações como:

- Temperatura da CPU;
- Velocidade dos coolers;
- Tensões da fonte;
- Estado de alguns componentes.

Muito útil para diagnóstico de superaquecimento.

---

# Casos de uso no Suporte Técnico

## 1. Instalação do Windows

### Situação

O cliente precisa formatar o computador.

### Procedimento

1. Criar um pendrive bootável.
2. Acessar a BIOS.
3. Alterar a ordem de boot.
4. Definir o pendrive como primeiro dispositivo.
5. Reiniciar o equipamento.

---

## 2. Computador não encontra o SSD

### Situação

O Windows não inicia.

### Verificação

- Acessar a BIOS.
- Confirmar se o SSD aparece na lista de dispositivos.

### Se não aparecer

- Verificar cabos;
- Verificar alimentação;
- Testar outro SSD;
- Avaliar possível defeito.

---

## 3. Ativar virtualização

### Situação

Usuário não consegue executar máquinas virtuais.

### Procedimento

1. Entrar na BIOS.
2. Localizar Intel VT-x ou AMD-V.
3. Alterar para Enabled.
4. Salvar e reiniciar.

---

## 4. Diagnóstico de superaquecimento

### Situação

Computador desliga sozinho.

### Procedimento

1. Acessar a BIOS.
2. Verificar temperatura da CPU.
3. Verificar velocidade dos coolers.
4. Inspecionar pasta térmica e sistema de refrigeração.

---

## 5. Recuperação após falha de boot

### Situação

Mensagem:

> Operating System Not Found

### Possíveis verificações

- Ordem de boot incorreta;
- SSD não reconhecido;
- Sistema operacional corrompido.

---

# Como atualizar a BIOS

A atualização da BIOS pode corrigir:

- Problemas de compatibilidade;
- Falhas de segurança;
- Erros de estabilidade;
- Compatibilidade com novos processadores.

### Procedimento geral

1. Identificar modelo da placa-mãe.
2. Acessar o site oficial do fabricante.
3. Baixar a versão correta.
4. Seguir as instruções do fabricante.

### Importante

Uma atualização interrompida pode inutilizar a placa-mãe.

Por esse motivo, atualizações devem ser realizadas apenas quando houver necessidade real.

---

# Cuidados importantes

Nunca altere configurações que você não conhece.

Antes de modificar qualquer parâmetro:

- Anote a configuração original;
- Tire fotos das telas;
- Leia a documentação do fabricante.

Alterações incorretas podem impedir a inicialização do computador.

---

# Perguntas frequentes em entrevistas de Suporte Técnico

### O que significa BIOS?

Basic Input/Output System.

### Qual é a função da BIOS?

Inicializar o hardware e carregar o sistema operacional.

### O que é POST?

Teste executado durante a inicialização para verificar os componentes do computador.

### Qual a diferença entre BIOS e UEFI?

UEFI é uma versão mais moderna, rápida e segura do firmware.

### Para que serve alterar a ordem de boot?

Permite iniciar o computador por dispositivos diferentes, como pendrives de instalação.

### Quando atualizar a BIOS?

Somente quando houver necessidade de correção, segurança ou compatibilidade.

---

# Conclusão

A BIOS é um dos componentes fundamentais para qualquer profissional de suporte técnico. Conhecer seu funcionamento permite solucionar problemas de inicialização, instalar sistemas operacionais, diagnosticar falhas de hardware e configurar recursos importantes do computador.

Dominar BIOS e UEFI é um conhecimento frequentemente exigido em entrevistas para cargos de Help Desk, Service Desk, Suporte Técnico N1 e N2, além de ser uma habilidade indispensável para quem deseja construir uma carreira sólida na área de infraestrutura e suporte.