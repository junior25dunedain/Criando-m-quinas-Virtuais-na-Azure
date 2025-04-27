
# Guia Completo: Máquinas Virtuais na Azure 🚀

## 📌 Visão Geral
Este repositório tem como objetivo centralizar informações, resumos, anotações e dicas sobre o uso da Azure, com foco na **criação, gerenciamento e otimização de máquinas virtuais (VMs)**. Ele servirá como **material de apoio para estudos e futuras implementações**, abrangendo desde conceitos básicos até práticas avançadas.

---


## 📖 Resumo

### 🔹 Introdução à Azure
A **Microsoft Azure** é uma plataforma de serviços em nuvem que permite a criação e gerenciamento de infraestrutura e aplicativos de maneira escalável. Algumas vantagens:
- **Escalabilidade**: ajuste fácil de recursos conforme demanda.
- **Segurança**: modelos robustos de autenticação e proteção de dados.
- **Integração**: compatível com diversas tecnologias e linguagens.
- **Automação**: suporte para scripts e gerenciadores como Azure DevOps.

### 🔹 Criando uma Máquina Virtual (VM)
#### Métodos de criação:
1. **Azure Portal**: Interface gráfica para configuração manual.
2. **Azure CLI**: Linha de comando para operações rápidas.
3. **PowerShell**: Automação de processos de criação e gerenciamento.
4. **Terraform**: Infraestrutura como código.

Exemplo de criação via Azure CLI:
```bash
az vm create \
  --resource-group MeuGrupoDeRecursos \
  --name MinhaVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys
```

### 🔹 Gerenciamento de VMs
Após a criação, é essencial saber monitorar e administrar suas instâncias para garantir um funcionamento adequado. Alguns pontos:
- Escalabilidade: Alteração dinâmica de capacidade conforme necessidade.
- Snapshots: Backup rápido para restauração de estados anteriores.
- Políticas de segurança: Controle de acessos e permissões refinadas.

Comandos úteis para gerenciamento:

az vm stop --name MinhaVM --resource-group MeuGrupoDeRecursos
az vm start --name MinhaVM --resource-group MeuGrupoDeRecursos
az vm delete --name MinhaVM --resource-group MeuGrupoDeRecursos

## 📝 Anotações

### 🔹 Comandos Azure CLI
Principais comandos para criação e gerenciamento:

az vm list --output table

az vm show --name NomeVM --resource-group MeuGrupoDeRecursos

### 🔹 Troubleshooting
- Problemas de conexão SSH:
az network nic list --resource-group MeuGrupoDeRecursos


- Erros de inicialização:
az vm get-instance-view --name MinhaVM --resource-group MeuGrupoDeRecursos


## 💡 Dicas e Boas Práticas
### 🔹 Custos e Otimização Financeira
- Escolha a VM ideal com base na carga de trabalho (evite superdimensionamento!).
- Utilize reservas de instância para descontos em contratos longos.
- Configure auto shutdown para desligar VMs fora do horário de uso.

Exemplo de configuração de desligamento automático:
```bash
az vm auto-shutdown \
  --resource-group MeuGrupoDeRecursos \
  --name MinhaVM \
  --time 20:00
```

### 🔹 Backup e Recuperação
- Snapshots periódicos garantem pontos de restauração.
- Configure Azure Backup para proteção de dados.
- Implemente disaster recovery para ambientes críticos.

### 🔹 Monitoramento e Alertas
- Use Azure Monitor para coletar métricas da VM.
- Configure Log Analytics para análise aprofundada.
- Crie alertas automatizados com base em consumo de recursos.


🛠 Recursos Adicionais

🔗 [Documentação Oficial da Azure](https://learn.microsoft.com/en-us/azure/?product=popular)

🔗 [Tutoriais sobre Azure Virtual Machines](https://learn.microsoft.com/en-us/azure/virtual-machines/)

🔗 [Guia Azure CLI](https://learn.microsoft.com/en-us/cli/azure/)

