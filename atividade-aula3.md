Aula 03 — Interfaces e Endereçamento de Rede
1. Identificação
Aluno: MARIA CLARA NECO DA SILVA
Matrícula: 2024333731
Curso: Técnico Integrado em Desenvolvimento de Sistemas
Instituição: IFAL — Campus Maceió
Disciplina: Laboratório de Sistemas Operacionais e Redes (LSOR)
Semestre: 2026.02
Data da prática: PREENCHA A DATA
2. Objetivo

Identificar interfaces de rede, endereços IP, máscaras de sub-rede, endereços MAC e gateway padrão no Ubuntu Server. Realizar testes de conectividade e comparar os modos NAT e Placa em Ponte (Bridge) no VirtualBox.

3. Ambiente
Sistema hospedeiro: Windows
Sistema convidado: Ubuntu Server 26.04 LTS
Hipervisor: VirtualBox
Interface de rede esperada no modo NAT: enp0s3
IP esperado no modo NAT: 10.0.2.15
Gateway esperado no modo NAT: 10.0.2.2
4. Procedimento
4.1. Inspeção das interfaces de rede

Comandos executados:

bash
ip addr show
ip link
ip route
netplan status


Resultado obtido:

Registre os dados reais da interface, incluindo nome, endereço IP, prefixo, MAC e gateway padrão.

4.2. Testes de conectividade

Comandos executados:

bash
ping -c 4 127.0.0.1
ping -c 4 IP_DA_SUA_VM
ping -c 4 10.0.2.2
ping -c 4 8.8.8.8
ping -c 4 google.com


Substitua IP_DA_SUA_VM pelo endereço IP real da sua máquina virtual.

Resultado obtido:

Descreva quais testes funcionaram e quais apresentaram falhas. Explique o que os resultados indicam sobre a conectividade e a resolução de nomes.

4.3. Rastreamento de rotas

Comando executado:

bash
traceroute 8.8.8.8


Resultado obtido:

Registre os saltos exibidos pelo comando e identifique o gateway, se aparecer na saída.

4.4. Comparação entre NAT e Bridge

Registre os dados observados em cada modo:

Informação	NAT	Bridge
Endereço IP da VM	PREENCHER	PREENCHER
Gateway padrão	PREENCHER	PREENCHER
Conectividade com a internet	PREENCHER	PREENCHER
Acesso do host à VM	PREENCHER	PREENCHER
5. Testes e Evidências
5.1. Interfaces de rede

!Interfaces de rede

Adicione a captura real de ip addr show e explique o endereço IP, o prefixo e o MAC identificados.

5.2. Tabela de rotas

!Tabela de rotas

Adicione a captura real de ip route e identifique a rota padrão.

5.3. Testes de conectividade

!Testes de conectividade

Adicione a captura dos testes de ping e descreva os resultados observados.

6. Problemas e Soluções

Descreva um problema realmente encontrado durante os testes de rede, sua causa provável e a solução aplicada.

Se não houve problemas, informe isso e explique como verificou a conectividade.

7. Conclusão

Explique o que aprendeu sobre interfaces de rede, endereçamento IP, gateway, testes de conectividade e diferenças entre NAT e Bridge. Comente a importância desses conceitos no diagnóstico de problemas de rede.
