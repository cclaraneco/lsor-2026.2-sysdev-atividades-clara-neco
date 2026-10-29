Aula 01 — Introdução à Virtualização e Instalação do Ubuntu Server
1. Identificação
Aluno: MARIA CLARA NECO DA SILVA
Matrícula: 2024333731
Curso: Técnico Integrado em Desenvolvimento de Sistemas
Instituição: IFAL — Campus Maceió
Disciplina: Laboratório de Sistemas Operacionais e Redes (LSOR)
Semestre: 2026.02
Data da prática: 26 de out.
2. Objetivo

Compreender os conceitos básicos de virtualização, criar uma máquina virtual no VirtualBox e instalar o Ubuntu Server 26.04 LTS com configurações de hardware e armazenamento definidas no roteiro da aula.

3. Ambiente
Sistema hospedeiro: Windows
Hipervisor: VirtualBox
Sistema convidado: Ubuntu Server 26.04 LTS
Memória RAM configurada: PREENCHA O VALOR UTILIZADO
Processadores virtuais: PREENCHA A QUANTIDADE
Disco virtual: PREENCHA O TAMANHO
Nome da máquina virtual: ubuntu_server
4. Procedimento

Descreva as etapas que você executou durante a prática:

Organização dos diretórios de trabalho no Windows.
Criação da máquina virtual no VirtualBox.
Configuração da memória, processador e disco virtual.
Seleção da imagem ISO do Ubuntu Server.
Instalação do sistema operacional.
Configuração das partições e do usuário administrador.
Reinicialização e primeiro acesso ao sistema.
Atualização dos pacotes com o comando:
bash
sudo apt-get update

5. Testes e Evidências
5.1. Verificação do sistema instalado

Comando executado:

bash
hostnamectl


Resultado obtido:
Registre aqui a saída real do comando.

5.2. Atualização dos pacotes

Comando executado:

bash
sudo apt-get update


Resultado obtido:
Descreva o resultado observado durante a atualização.

5.3. Captura de tela da instalação

Adicione abaixo uma captura de tela real da sua prática, caso tenha sido solicitada ou registrada.

<!-- Exemplo após adicionar a imagem à pasta imagens:
![Instalação do Ubuntu Server](imagens/aula1_instalacao.png)
-->

6. Problemas e Soluções

Registre um problema que você realmente encontrou durante a instalação ou configuração da máquina virtual e explique como resolveu.

Se não encontrou problemas, informe isso honestamente e descreva os cuidados que tomou para concluir a instalação.

7. Conclusão

Escreva o que aprendeu sobre virtualização, configuração de máquinas virtuais e instalação do Ubuntu Server. Comente também a importância de configurar corretamente os recursos de hardware e o armazenamento.
