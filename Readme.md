# Dashboard de Vendas por Assinatura

Este projeto tem como objetivo transformar dados brutos de assinaturas em um **dashboard de vendas** claro e visual, permitindo análise de desempenho, entendimento de comportamento dos assinantes e apoio à tomada de decisão.

## 📊 Objetivos do projeto

- Organizar e visualizar dados de assinaturas.
- Analisar receita por tipo de plano.
- Entender o impacto de cupons de desconto.
- Avaliar a adesão à renovação automática.
- Calcular indicadores de receita e lucro por assinante.

## 🗂️ Dados utilizados

Os dados de entrada representam assinaturas de um serviço com os seguintes campos principais:

- **Subscriber ID**: identificador do assinante  
- **Name**: nome do assinante  
- **Plan**: tipo de plano (Core, Standard, Ultimate)  
- **Start Date**: data de início da assinatura  
- **Auto Renewal**: renovação automática (Yes/No)  
- **Subscription Price**: valor da assinatura  
- **Subscription Type**: tipo de cobrança (Monthly, Quarterly, Annual)  
- **EA Play Season Pass / Price**: adesão e valor do passe EA Play  
- **Minecraft Season Pass / Price**: adesão e valor do passe Minecraft  
- **Coupon Value**: valor de desconto aplicado  
- **Total Value**: valor final pago após desconto  
- **Custo estimado**: custo de material e mão de obra (ex.: R$ 15,00 por assinatura, quando aplicável)  
- **Lucro**: receita – custo

## 📈 Análises presentes no dashboard

O arquivo `dashboard-vendas.xlsx` contém:

1. **Volume de vendas por tipo de plano (Mensal, Trimestral, Anual)**  
   - Gráfico mostrando a quantidade de vendas por tipo de plano.

2. **Receita total gerada por assinante (plano + passes + descontos)**  
   - Gráfico de colunas empilhadas mostrando a composição da receita por plano (assinatura, passes, cupons).

3. **Distribuição de assinantes com renovação automática (Sim x Não)**  
   - Gráfico de colunas agrupadas ou barras empilhadas por tipo de plano.

4. **Impacto dos cupons de desconto no valor final da assinatura**  
   - Comparação entre valor bruto (antes do desconto), valor de cupons e valor final.

5. **Lucro estimado por assinatura**  
   - Cálculo considerando custo fixo (ex.: R$ 15,00) e receita final.

## 🧮 Como o lucro foi calculado

Para cada assinatura:

- **Valor bruto**  
  \[
  \text{Valor bruto} = \text{Subscription Price} + \text{EA Play Season Pass Price} + \text{Minecraft Season Pass Price}
  \]

- **Receita (valor recebido)**  
  \[
  \text{Receita} = \text{Total Value}
  \]

- **Lucro**  
  \[
  \text{Lucro} = \text{Receita} - \text{Custo}
  \]

Exemplo (João Silva – Ultimate):

- Valor bruto: R$ 65,00  
- Cupom: R$ 5,00  
- Receita: R$ 60,00  
- Custo: R$ 15,00  
- Lucro: R$ 45,00  

## 🛠️ Como reproduzir o dashboard

1. **Baixar o arquivo**
   - Faça o download do arquivo `dashboard-vendas.xlsx` deste repositório.

2. **Abrir no Excel**
   - Abra o arquivo no Microsoft Excel (versão com suporte a Tabelas Dinâmicas e Gráficos).

3. **Explorar as abas**
   - `Base de Dados`: contém os dados brutos.
   - `Tabelas Dinâmicas`: contém as tabelas de análise.
   - `Dashboard`: consolida os gráficos e indicadores.

4. **Atualizar dados (opcional)**
   - Substitua ou acrescente linhas na base de dados.
   - Atualize as Tabelas Dinâmicas (clique com o botão direito → Atualizar).
   - Os gráficos do dashboard serão atualizados automaticamente.
