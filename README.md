# Simulação de Rede Corporativa: VLANs, STP e Roteamento InterVLAN

Este repositório contém os arquivos e a documentação referentes ao projeto prático de Redes de Computadores, focado na construção e expansão de uma topologia corporativa utilizando o simulador **Cisco Packet Tracer**.

## 📋 Descrição do Projeto

O cenário simula a rede de uma empresa dividida por departamentos e andares. O objetivo principal é segmentar a rede através de **VLANs**, realizar o roteamento entre elas utilizando **subinterfaces (Router-on-a-Stick)**, configurar links **Trunk** entre os switches e garantir alta disponibilidade e prevenção de loops através do **STP (Spanning Tree Protocol)**.

### A Expansão (O Novo Cenário)
A partir da topologia base documentada no arquivo `image_eb97ca.jpg`, a empresa construiu um novo andar. Para atender a essa demanda, a nova topologia inclui:
* **Um 3º Switch** dedicado ao novo andar.
* **4 Novos Computadores:**
  * 3 alocados no departamento **Financeiro (Finance)**.
  * 1 alocado no departamento de **Vendas (Sales)**.
* **Caminho Redundante:** Interligação dos switches formando um caminho redundante, com o protocolo **STP** ativado e validado para evitar loops de camada 2.

## 🏗️ Topologia e Endereçamento Base

A rede foi segmentada conforme a estrutura departamental abaixo:

| VLAN | Departamento | Endereçamento IPv4 | Portas Alocadas |
| :--- | :--- | :--- | :--- |
| **VLAN 2** | Sales (Vendas) | `172.16.2.0/24` | 1 a 5 |
| **VLAN 3** | HR (Recursos Humanos) | `172.16.3.0/24` | 6 a 10 |
| **VLAN 4** | Purchasing (Compras) | `172.16.4.0/24` | 11 a 15 |
| **VLAN 5** | Finance (Financeiro) | `172.16.5.0/24` | 16 a 20 |



## 🛠️ Tecnologias e Protocolos Utilizados

* **VLAN (Virtual Local Area Network):** Segmentação lógica de domínios de broadcast.
* **(Trunking):** Passagem de múltiplas VLANs entre os switches e o roteador.
* **Subinterfaces:** Configuração no roteador principal para assumir o papel de *Default Gateway* de cada VLAN (Roteamento InterVLAN).
* **STP (Spanning Tree Protocol):** Prevenção de loops na topologia redundante dos 3 switches.

## 📦 Entregáveis do Projeto

- [ ] **Arquivo do Packet Tracer (`.pkt`):** Simulação completa e funcional com uso de *labels* para identificar cada elemento.
- [ ] **Vídeo de Demonstração:** Time-lapse de no máximo 3 minutos apresentando a configuração, testes de conectividade (ping entre departamentos) e validação do STP.
  - 🔗 **Link do Vídeo (YouTube):** `[INSERIR LINK PÚBLICO AQUI]`
- [ ] **Relatório Técnico (PDF):**
  - Introdução teórica sobre VLANs, STP, Trunk e Roteamento InterVLAN.
  - Imagem detalhada da nova topologia gerada pelo Packet Tracer.
  - Referências normativas (RFCs e Padrões IEEE) formatadas em ABNT.