Aula 04 — Acesso Remoto Seguro com OpenSSH e Redirecionamento de Portas
1. Identificação
Aluno: MARIA CLARA NECO DA SILVA
Matrícula: 2024333731
Curso: Técnico Integrado em Desenvolvimento de Sistemas
Instituição: IFAL — Campus Maceió
Disciplina: Laboratório de Sistemas Operacionais e Redes (LSOR)
Semestre: 2026.02
Data da prática: 26 de out.
2. Objetivo

Verificar interfaces e rotas de rede, auditar portas TCP no Windows e configurar o acesso remoto ao Ubuntu Server por SSH, utilizando o redirecionamento de portas do VirtualBox em modo NAT.

3. Ambiente
Sistema hospedeiro: Windows
Sistema convidado: Ubuntu Server 26.04 LTS
Hipervisor: VirtualBox
Modo de rede: NAT
IP esperado da VM: 10.0.2.15
Gateway esperado: 10.0.2.2
Porta do hospedeiro: 5222
Porta do convidado: 22
Usuário de acesso: administrador
4. Procedimento
4.1. Verificação do OpenSSH

Comandos executados:

bash
dpkg -l | grep openssh-server
systemctl status ssh


Resultado obtido:
Registre a saída real dos comandos e informe se o serviço SSH estava ativo.

4.2. Diagnóstico da rede

Comandos executados:

bash
ifconfig
route -n
traceroute 8.8.8.8
w


Resultado obtido:
Registre o endereço IP, a máscara, o MAC, o gateway e os resultados do rastreamento e da verificação de sessões.

4.3. Verificação no Windows

Comandos executados no PowerShell:

powershell
ipconfig /all
netstat -an | findstr 5222


Resultado obtido:
Registre as informações de rede do Windows e o resultado da consulta à porta antes de configurar o redirecionamento.

4.4. Configuração do redirecionamento

No VirtualBox, a regra de rede deve encaminhar a porta TCP 5222 do hospedeiro para a porta TCP 22 do convidado, utilizando os endereços definidos no roteiro.

Registre a configuração efetivamente utilizada.

5. Testes e Evidências
5.1. Interfaces da VM

Comando:

bash
ifconfig


!Interfaces de rede

Descreva o IP, a máscara e o MAC observados.

5.2. Tabela de rotas

Comando:
