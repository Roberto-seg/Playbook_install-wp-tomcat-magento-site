# Instalação simples das plataformas Wordpress, Magento, Tomcat no centos7

  instalação do Magento2,TomCat,Wordpress e um site estático, Nginx, centos 7

## Código 
Essas instruções fornecerão uma cópia do projeto instalado e funcionando em sua máquina local para fins de desenvolvimento e teste. Consulte implantação para obter notas sobre como implantar o projeto em um sistema ativo.

### Pré-requisitos

Centos 7 , PHP 7.2 , Ansible 2.9.9

```
$ ansible 2.9.9
  config file = /etc/ansible/ansible.cfg
  configured module search path = ['/usr/share/my_modules']
  ansible python module location = /usr/lib/python3/dist-packages/ansible
  executable location = /usr/bin/ansible
```
## Mão na massa 

No caso dessa Playbook, a parte da infra foi toda feita na aws, utilzando Ec2, Route53

## Built With

* [EC2](https://aws.amazon.com/pt/ec2/?ec2-whats-new.sort-by=item.additionalFields.postDateTime&ec2-whats-new.sort-order=desc) - Vms 
* [Route53](https://aws.amazon.com/pt/route53/) - Apontamento de Dns 
* [Freenom](https://www.freenom.com/pt/index.html?lang=pt) - Dominio

### Como rodar

Crie um arquivo Yml com o nome de hosts, e sete o ip de seu servidor.

### Iniciando o site,yml

```
ansible-playbook -i hosts site.yml 
```
Esta playbook fei desenvolvida como base de estudo, na ferramenta Ansible.

# Atualização futuras.
- [ ] Dividir o site.yml para melhor orgalização, e testes
- [ ] Implementar variáveis para senhas
