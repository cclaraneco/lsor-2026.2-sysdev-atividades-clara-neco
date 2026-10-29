Aula 02 — Administração de Usuários, Grupos e Permissões no Linux
1. Identificação
Aluno: MARIA CLARA NECO DA SILVA
Matrícula: 2024333731
Curso: Técnico Integrado em Desenvolvimento de Sistemas
Instituição: IFAL — Campus Maceió
Disciplina: Laboratório de Sistemas Operacionais e Redes (LSOR)
Semestre: 2026.02
Data da prática: 26 de out.
2. Objetivo

Praticar a administração de usuários e grupos no Ubuntu Server, configurar permissões de arquivos e diretórios e verificar como o Linux controla o acesso aos recursos do sistema.

3. Ambiente
Sistema operacional: Ubuntu Server 26.04 LTS
Hipervisor: VirtualBox
Usuário administrativo: administrador
Grupo de desenvolvimento: devs
Diretório compartilhado: /srv/projeto
4. Procedimento
4.1. Criação dos usuários

Comandos executados:

bash
sudo adduser fulano
sudo adduser cicrano
sudo adduser beltrano
sudo adduser novato


Descreva o resultado observado ao criar as contas.

4.2. Criação do grupo de desenvolvimento

Comandos executados:

bash
sudo groupadd devs
sudo usermod -aG devs fulano
sudo usermod -aG devs cicrano
sudo usermod -aG devs beltrano
grep "devs" /etc/group


Registre a saída real do último comando.

4.3. Criação e configuração do diretório

Comandos executados:

bash
sudo mkdir -p /srv/projeto
sudo chown administrador /srv/projeto
sudo chgrp devs /srv/projeto
sudo chmod 770 /srv/projeto
ls -ld /srv/projeto


Explique o significado das permissões rwxrwx---.

4.4. Configuração do arquivo compartilhado

Comandos executados:

bash
echo "Especificacao tecnica do roteador de borda" > /srv/projeto/config_redes.txt
chmod 660 /srv/projeto/config_redes.txt
ls -l /srv/projeto/config_redes.txt


Descreva as permissões aplicadas ao arquivo e quem pode modificá-lo.

5. Testes e Evidências
5.1. Teste com usuário do grupo devs

Utilize o usuário fulano para testar o acesso ao diretório e ao arquivo.

bash
su - fulano
cd /srv/projeto
ls -l
cat config_redes.txt
exit


Resultado obtido:
Registre o resultado real e explique se o acesso foi permitido.

<!-- Após adicionar a imagem:
![Teste do usuário do grupo devs](imagens/aula2_usuarios.png)
-->

5.2. Teste com usuário externo

Utilize o usuário novato para testar o acesso ao diretório protegido.

bash
su - novato
cd /srv/projeto
ls -l /srv/projeto
exit


Resultado obtido:
Registre se o sistema permitiu ou negou o acesso.

5.3. Evidências de grupos e permissões

<!-- Após adicionar as capturas:
![Grupos de trabalho](imagens/aula2_grupos.png)
-->

Adicione capturas de tela reais dos comandos e dos testes de acesso.

6. Problemas e Soluções

Descreva um problema realmente encontrado durante a criação de usuários, configuração de grupos ou definição de permissões, explicando como foi resolvido.

Se não houve problemas, registre essa informação e explique como verificou que as configurações estavam corretas.

7. Conclusão

Explique o que aprendeu sobre usuários, grupos, propriedade de arquivos e permissões no Linux. Comente a importância de restringir o acesso a diretórios compartilhados para proteger os dados.
