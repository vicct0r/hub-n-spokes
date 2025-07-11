# HUB-N-SPOKES

## 🌐 Sistema Centralizado de Distribuição

Sistema onde **CDs autônomos** realizam vendas normalmente e só acionam o **HUB** quando precisam repor estoque. O HUB orquestra transações entre CDs sem que eles precisem se comunicar diretamente.

## ⚡ Como Funciona

1. **Venda Normal**
   Cada CD vende seus produtos localmente enquanto tiver estoque

2. **Reposição Automática** 
   Quando um CD fica com estoque baixo: 
   - Solicita reposição ao HUB 
   - HUB encontra outro CD com o produto disponível 
   - Coordena a transferência entre eles 

3. **Transação Invisível**
   - CDs nunca se comunicam diretamente 
   - HUB atualiza saldos e registros de ambos 

## 🏗️ Arquitetura

- **HUB**: 1 instância central 
  *(Gatekeeper das transações)* 

- **CDs**: Múltiplas instâncias independentes 
  *(Vendem localmente + Repõem via HUB)* 

> "Os CDs fazem negócios entre si sem se conhecerem"
