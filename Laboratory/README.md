# 💻 Construindo o Ambiente de Desenvolvimento

## Índice
1. [Informações sobre o Ambiente](#informacoes-sobre-o-ambiente)
2. [Opção 01: Distros (ISO - VirtualBox)](#distros-iso-virtualbox)
3. [Opção 02: Distros (Vagrant - VirtualBox)](#distros-vagrant-virtualbox)
4. [Orquestramento](#orquestramento)
5. [Suporte/Contato](#suporte-contato)

## <a id="informacoes-sobre-o-ambiente"></a> Informações sobre o Ambiente

Existem duas opções para configurar o ambiente de desenvolvimento, dependendo das suas preferências e necessidades. Utilizamos RockyLinux para melhor simulação ao RHEL e openSUSE Leap para o SLE. Ambas as distribuições são conhecidas pela estabilidade e compatibilidade com ambientes corporativos.

## <a id="distros-iso-virtualbox"></a> Opção 01: Distros (ISO - VirtualBox)

### Distribuições Disponíveis

1. [openSUSE Leap 15.6](https://get.opensuse.org/leap/15.6/)
2. [RockyLinux v9.4](https://rockylinux.org/download)

### Passos para Configuração

1. Baixe a ISO da distribuição desejada.
2. Instale a distribuição usando o VirtualBox.
3. Para desativar a interface gráfica, utilize os seguintes comandos como usuário **root**:

```bash
su root
systemctl set-default multi-user.target
shutdown -r now
```

### Requisitos do Sistema

- **Memória RAM:** 4GB mínimo, 8GB recomendável
- **CPU:** 2 núcleos mínimo, 4 núcleos recomendável
- **Armazenamento:** 20GB mínimo, 40GB reconmendável

## <a id="distros-vagrant-virtualbox"></a> Opção 02: Distros (Vagrant - VirtualBox)

### Distribuições Disponíveis

1. [opensuse/Leap-15.4.x86_64](https://app.vagrantup.com/opensuse/boxes/Leap-15.4.x86_64)
2. [RockyLinux/9](https://app.vagrantup.com/rockylinux/boxes/9)

### Passos para Configuração

1. Instale o [Vagrant](https://developer.hashicorp.com/vagrant/install?product_intent=vagrant).
2. No diretório onde se encontra o `Vagrantfile`, execute:

```bash
vagrant up
```

### Configuração dos Servidores

Ao executar o comando `vagrant up`, serão criados dois servidores:

- **Servidor codelinx01:** Distribuição RockyLinux 9, IP: 192.168.1.201
- **Servidor codelinx02:** Distribuição openSUSE Leap 15.4, IP: 192.168.1.202

### Acesso via SSH

Para acessar os servidores via SSH, utilize:

```bash
vagrant ssh codelinx01
vagrant ssh codelinx02
```

## <a id="orquestramento"></a> Orquestramento

### Comandos Principais

- **Inicialização de Novo Projeto Vagrant:**
  ```bash
  vagrant init
  ```
- **Início da Máquina Virtual:**
  ```bash
  vagrant up
  vagrant up "nome_da_vm"
  ```
- **Verificação do Estado das Máquinas Virtuais:**
  ```bash
  vagrant status
  ```
- **Desligamento da Máquina Virtual:**
  ```bash
  vagrant halt "nome_da_vm"
  ```
- **Destruição da Máquina Virtual:**
  ```bash
  vagrant destroy "nome_da_vm" -f
  ```
- **Listagem de Boxes Vagrant Instaladas:**
  ```bash
  vagrant box list
  ```
- **Remoção de uma Box Vagrant:**
  ```bash
  vagrant box remove "nome_da_box"
  ```
- **Status Global das VMs:**
  ```bash
  vagrant global-status
  ```

Resumo dos Termos Importantes `LICENSE.md`:
Permissões: A licença MIT permite a qualquer pessoa que obtenha uma cópia do software e dos arquivos de documentação associados (o "Software"), usar, copiar, modificar, mesclar, publicar, distribuir, sublicenciar e/ou vender cópias do Software, e permitir que pessoas a quem o Software seja fornecido façam o mesmo, sem restrições.

Condições: A única condição é que o aviso de direitos autorais (copyright) acima e este aviso de permissão sejam incluídos em todas as cópias ou partes substanciais do Software.

Isenção de Garantias: O software é fornecido "como está", sem garantia de qualquer tipo, expressa ou implícita, incluindo, mas não se limitando a, garantias de comercialização, adequação a um propósito específico e não violação. Em nenhum caso os autores ou detentores de direitos autorais serão responsáveis por qualquer reivindicação, danos ou outras responsabilidades, seja em uma ação de contrato, delito ou de outra forma, decorrente de, fora de ou em conexão com o software ou o uso ou outras negociações no software.

## <a id="suporte-contato"></a> 🤝 Suporte/Contato

### Contato Profissional

Para suporte ou questões relacionadas ao projeto, entre em contato através dos seguintes canais:

[![LinkedIn Badge](https://img.shields.io/static/v1?style=for-the-badge&message=LinkedIn&color=0A66C2&logo=LinkedIn&logoColor=FFFFFF&label=)](https://www.linkedin.com/in/ihanmessias/)
[![Instagram Badge](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/ihan.py/)

✉ Email: codelinx.academy@gmail.com

<p align="center">© CodeLinx Academy</p>