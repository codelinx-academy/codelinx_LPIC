# 💻 Construindo o Ambiente de Desenvolvimento

## Índice
1. [Informações sobre o Ambiente](#informacoes-sobre-o-ambiente)
2. [VirtualBox](#download-virtualbox)
  - 2.1 [Opção 01: Baixar e instalar Distros no VirtualBox (Método Manual)](#opcao-01)
    - [Criando e configurando o ROCKYLINUX9](#rockylinux)
    - [Criando e configurando o LEAP](#leap)
  - 2.2 [Opção 02: Baixar e instalar Distros no VirtualBox (Método Vagrant)](#opcao-02)
    - [Vagrant](#download-vagrant)
    - [Criando e configurando o ROCKYLINUX9 e LEAP](#rocky-leap)
    - [Orquestramento](#orquestramento)
3. [Contato Profissional](#contato-profissional)

## <a id="informacoes-sobre-o-ambiente"></a>1. Informações sobre o Ambiente

Existem duas opções para configurar o ambiente de desenvolvimento, dependendo das suas preferências e necessidades. Utilizamos RockyLinux para melhor simulação ao RHEL e openSUSE Leap para o SLE. Ambas as distribuições são conhecidas pela estabilidade e compatibilidade com ambientes corporativos.

## <a id="download-virtualbox"></a>2. VirtualBox
O VirtualBox da Oracle é um software de virtualização poderoso que permite executar múltiplos sistemas operacionais em um único computador físico. É uma ferramenta ideal para quem precisa testar aplicações em diferentes ambientes sem a necessidade de múltiplas máquinas.

Link para Download: [virtualbox-download](https://www.virtualbox.org/wiki/Downloads).

### <a id="opcao-01"></a>2.1 Opção 01: Baixar e instalar Distros no VirtualBox (Metodo Manual)

<p align="center">
<img src="https://github.com/codelinx-academy/codelinx_LPIC/assets/72288211/cff444fe-8a79-4adb-9374-4fed9119a9f9" alt="VirtualBox-SSH">
</p>

Distribuições Disponíveis:
1. [openSUSE Leap 15.6](https://get.opensuse.org/leap/15.6/)
2. [RockyLinux v9.4](https://rockylinux.org/download)

Requisitos do Sistema:
- **Memória RAM:** 2GB mínimo, 4GB recomendável
- **CPU:** 2 núcleos mínimo, 4 núcleos recomendável
- **Armazenamento:** 10GB mínimo, 20GB reconmendável

#### <a id="rockylinux"></a> Criando e configurando o ROCKYLINUX9:

inserir passos aqui

_Para desativar a interface gráfica, utilize o seguinte comando como usuário **root** e reinicie o sistema: `systemctl set-default multi-user.target`_

#### <a id="leap"></a> Criando e configurando o LEAP:

inserir passos aqui

### <a id="opcao-02"></a>2.2 Opção 02: Baixar e instalar Distros no VirtualBox (Metodo Vagrant)

<p align="center">
<img src="https://github.com/codelinx-academy/codelinx_LPIC/assets/72288211/7f8a80a2-3290-4b61-9c8b-54fa52e793fc" alt="Vagrant-SSH">
</p>

Distribuições Disponíveis:
1. [opensuse/Leap-15.4.x86_64](https://app.vagrantup.com/opensuse/boxes/Leap-15.4.x86_64)
2. [RockyLinux/9](https://app.vagrantup.com/rockylinux/boxes/9)

#### <a id="vagrant"></a> Vagrant
O Vagrant é uma ferramenta para construir e distribuir ambientes de desenvolvimento. Com ele, você pode criar e configurar ambientes de desenvolvimento leves, reprodutíveis e portáteis.

Link para Download: [vagrant-download](https://developer.hashicorp.com/vagrant/install?product_intent=vagrant).

2. No diretório onde se encontra o `Vagrantfile`, execute:

```bash
vagrant up
```

#### <a id="rocky-leap"></a> Criando e configurando o ROCKYLINUX9 e LEAP

Ao executar o comando `vagrant up`, serão criados dois servidores:

- **Servidor codelinx01:** Distribuição RockyLinux 9, IP: 192.168.1.201
- **Servidor codelinx02:** Distribuição openSUSE Leap 15.4, IP: 192.168.1.202

#### Acesso via SSH

Para acessar os servidores via SSH, utilize:

```bash
vagrant ssh codelinx01
vagrant ssh codelinx02
```

#### <a id="orquestramento"></a> Orquestramento

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
  vagrant destroy -f "nome_da_vm" 
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

## <a id="contato-profissional"></a> 🤝 Contato Profissional

Para suporte ou questões relacionadas ao projeto, entre em contato através dos seguintes canais:

[![LinkedIn Badge](https://img.shields.io/static/v1?style=for-the-badge&message=LinkedIn&color=0A66C2&logo=LinkedIn&logoColor=FFFFFF&label=)](https://www.linkedin.com/in/ihanmessias/)
[![Instagram Badge](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/ihan.codelinx/)

✉ Email: codelinx.academy@gmail.com

<p align="center">© CodelinxAcademy</p>