# 💰 Gestor Financeiro Pessoal

> Sistema completo de controle financeiro pessoal com interface moderna, armazenamento em arquivos XLSX locais e visualizações gráficas avançadas.

![Versão](https://img.shields.io/badge/vers%C3%A3o-1.0.0-blue.svg)
![Licença](https://img.shields.io/badge/licen%C3%A7a-MIT-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?logo=bootstrap&logoColor=white)

---

## 📋 Índice

- [Sobre o Projeto](#-sobre-o-projeto)
- [Características Principais](#-características-principais)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Pré-requisitos](#-pré-requisitos)
- [Como Usar](#-como-usar)
- [Funcionalidades Detalhadas](#-funcionalidades-detalhadas)
- [Estrutura de Dados](#-estrutura-de-dados)
- [Sistema de Armazenamento](#-sistema-de-armazenamento)
- [Exportação de Dados](#-exportação-de-dados)
- [Categorias Disponíveis](#-categorias-disponíveis)
- [FAQ - Perguntas Frequentes](#-faq---perguntas-frequentes)
- [Resolução de Problemas](#-resolução-de-problemas)
- [Contribuindo](#-contribuindo)
- [Licença](#-licença)

---

## 🎯 Sobre o Projeto

O **Gestor Financeiro Pessoal** é uma aplicação web standalone (sem backend) para controle completo de receitas e despesas pessoais. Desenvolvido com tecnologias modernas, oferece uma experiência profissional de gestão financeira totalmente **offline** e **gratuita**.

### 🌟 Destaques

- ✅ **100% Local** - Seus dados nunca saem do seu computador
- ✅ **Sem Servidor** - Não precisa de banco de dados ou servidor
- ✅ **Arquivos XLSX** - Compatível com Excel/Google Sheets
- ✅ **Interface Moderna** - Design dark profissional e responsivo
- ✅ **Gráficos Interativos** - Visualizações ricas com Chart.js
- ✅ **Multi-visualização** - Mensal, anual ou histórico completo

---

## ⚡ Características Principais

### 📊 Controle Financeiro Completo

| Funcionalidade | Descrição |
|----------------|-----------|
| 💵 **Lançamentos** | Adicione entradas e saídas com data, descrição e categoria |
| 📅 **Gestão Mensal** | Organize por mês/ano com navegação intuitiva |
| 📈 **Saldo Acumulado** | Acompanhe seu saldo em tempo real |
| 🏷️ **Categorização** | 11 categorias pré-definidas para organização |
| 🔍 **Busca e Filtro** | DataTables com busca e ordenação avançada |
| 🗑️ **Exclusão Segura** | Confirmação antes de excluir lançamentos |

### 📈 Visualizações e Relatórios

- **Tabela de Lançamentos** - Todos os movimentos com saldo progressivo
- **Resumo por Categoria** - Agregação de entradas/saídas por tipo
- **Tabela Pivot** - Análise cruzada de dados
- **Gráficos Dinâmicos**:
  - 📉 Linha: Evolução do saldo acumulado
  - 🍩 Pizza: Distribuição de gastos por categoria
  - 📊 Barras: Comparativo entradas vs saídas

### 💾 Armazenamento Inteligente

```
Pasta "salvar" (escolhida pelo usuário)
├── 01-2026.xlsx  ← Janeiro/2026
├── 02-2026.xlsx  ← Fevereiro/2026
├── 03-2026.xlsx  ← Março/2026
└── ...
```

- **File System Access API** - Acesso direto aos arquivos no disco
- **IndexedDB** - Lembra a pasta escolhida entre sessões
- **localStorage** - Fallback quando API não disponível

### 📤 Exportação Profissional

- ✅ **Exportar Ano Completo** - Todos os 12 meses em uma única tabela
- ✅ **Exportar Ano Separado** - Uma aba por mês
- ✅ **Exportar Histórico** - Todos os anos consolidados
- ✅ **Formatação Excel** - Cores, bordas, totais e formato R$

---

## 🛠️ Tecnologias Utilizadas

### Frontend

| Tecnologia | Versão | Uso |
|------------|--------|-----|
| **HTML5** | - | Estrutura da página |
| **CSS3** | - | Estilização customizada |
| **JavaScript ES6+** | - | Lógica da aplicação |
| **jQuery** | 3.7.1 | Manipulação DOM |
| **Bootstrap** | 5.3.2 | Framework UI responsivo |
| **Bootstrap Icons** | 1.11.3 | Ícones SVG |

### Bibliotecas de Dados

| Biblioteca | Versão | Uso |
|------------|--------|-----|
| **DataTables** | 1.13.7 | Tabelas interativas |
| **Chart.js** | 4.4.1 | Gráficos dinâmicos |
| **SheetJS (XLSX)** | 0.18.5 | Leitura/escrita XLSX |
| **ExcelJS** | 4.4.0 | Formatação avançada Excel |
| **SweetAlert2** | 11.14.1 | Alertas bonitos |

### APIs Web

- **File System Access API** - Salvar/ler arquivos localmente
- **IndexedDB API** - Persistência de configurações
- **localStorage API** - Fallback de armazenamento

---

## 💻 Pré-requisitos

### Navegador Compatível

Para funcionalidade completa, use um dos navegadores:

| Navegador | Versão Mínima | Suporte File System API |
|-----------|---------------|-------------------------|
| ✅ **Google Chrome** | 86+ | ✅ Sim |
| ✅ **Microsoft Edge** | 86+ | ✅ Sim |
| ✅ **Opera** | 72+ | ✅ Sim |
| ⚠️ Firefox | Qualquer | ❌ Não (usa localStorage) |
| ⚠️ Safari | Qualquer | ❌ Não (usa localStorage) |

> **Nota**: Em navegadores sem File System API, os dados são salvos em localStorage (limitação de ~5MB).

### Sistema Operacional

- ✅ Windows 10/11
- ✅ macOS 10.15+
- ✅ Linux (Ubuntu, Fedora, etc.)

### Permissões Necessárias

- Acesso de leitura/escrita na pasta "salvar" escolhida

---

## 🚀 Como Usar

### 1️⃣ Instalação

```bash
# Clone o repositório
git clone https://github.com/Otavio1661/gestor-financeiro.git

# Entre na pasta
cd gestor-financeiro

# Abra o arquivo no navegador
# Windows
start app.html

# macOS
open app.html

# Linux
xdg-open app.html
```

Ou simplesmente:
- Baixe o arquivo `app.html`
- Dê duplo clique para abrir no navegador

### 2️⃣ Primeira Configuração

#### Passo 1: Escolher Pasta de Armazenamento

1. Clique no botão **"📁 salvar"** (laranja)
2. Crie uma pasta chamada `salvar` no seu computador
3. Selecione essa pasta
4. Confirme as permissões quando solicitado

> ✅ O status mudará para **"Pasta pronta"**

#### Passo 2: Selecionar Mês/Ano

1. No topo da página, escolha o **Mês** (ex: Janeiro)
2. Escolha o **Ano** (ex: 2026)
3. O sistema criará automaticamente o arquivo `01-2026.xlsx`

### 3️⃣ Adicionar Lançamentos

#### Entrada (Receita)

```
Data: 05/01/2026
Descrição: Salário Janeiro
Categoria: Salário
Entrada: 5000.00
Saída: (deixe vazio)
```

#### Saída (Despesa)

```
Data: 10/01/2026
Descrição: Aluguel
Categoria: Moradia
Entrada: (deixe vazio)
Saída: 1200.00
```

> 🔒 **Importante**: A data é automaticamente travada no mês/ano selecionado!

### 4️⃣ Visualizar Dados

Use as **6 abas** disponíveis:

1. **📊 Lançamentos** - Tabela completa com busca
2. **📋 Resumo por categoria** - Totais agregados
3. **🏷️ Categorias** - Lista de categorias
4. **🔢 Pivot** - Análise cruzada
5. **📈 Gráficos** - Visualizações gráficas
6. **📅 Ano / Geral** - Análise anual e histórica

---

## 🎨 Funcionalidades Detalhadas

### 📊 Aba: Lançamentos

**Características:**
- ✅ Tabela paginada (15 itens por página)
- ✅ Busca em tempo real
- ✅ Ordenação por qualquer coluna
- ✅ Saldo acumulado progressivo
- ✅ Cores diferenciadas:
  - 🟢 Verde claro = Entradas
  - 🔴 Vermelho claro = Saídas
  - 🟢/🔴 Saldo positivo/negativo
- ✅ Botão de exclusão por linha
- ✅ Totais no rodapé

**Layout:**
```
┌─────────────────────────────────────────────────────────┐
│ Data     │ Descrição │ Categoria │ Entrada │ Saída │ ... │
├─────────────────────────────────────────────────────────┤
│ 01/01/26 │ Salário   │ Salário   │ R$ 5.000│   -   │ ... │
│ 05/01/26 │ Aluguel   │ Moradia   │    -    │ R$ 1.200 │...│
├─────────────────────────────────────────────────────────┤
│ TOTAIS                           │ R$ 5.000│ R$ 1.200 │...│
└─────────────────────────────────────────────────────────┘
```

### 📋 Aba: Resumo por Categoria

Agrega todos os lançamentos do período por categoria:

```
Categoria         │ Entradas  │ Saídas    │ Diferença
──────────────────┼───────────┼───────────┼───────────
Salário          │ R$ 5.000  │ R$ 0      │ +R$ 5.000
Moradia          │ R$ 0      │ R$ 1.200  │ -R$ 1.200
Alimentação      │ R$ 0      │ R$ 800    │ -R$ 800
```

### 📈 Aba: Gráficos

#### 1. Gráfico de Linha - Saldo Acumulado
Mostra a evolução do seu saldo ao longo do tempo.

#### 2. Gráfico de Pizza - Distribuição de Gastos
Visualiza percentualmente onde você gasta mais.

#### 3. Gráfico de Barras - Comparativo
Compara entradas vs saídas por categoria.

### 📅 Aba: Ano / Geral

#### Modo 1: Ver Ano
Clique em **"Carregar Ano"** para:
- 📊 Tabela de resumo anual por categoria
- 📈 Gráfico de barras dos 12 meses

#### Modo 2: Ver Todos os Anos
Clique em **"Carregar Todos"** para:
- 📊 Tabela comparativa entre anos
- 💰 Totais históricos

#### Controles de Visualização
Use os **switches** para escolher:
- ☑️ Dados do Ano
- ☑️ Todos os Anos
- ☑️ Ambos
- ☐ Nenhum

---

## 📁 Estrutura de Dados

### Formato de Lançamento

Cada lançamento possui:

```javascript
{
  id: 1704412800000,           // Timestamp único
  data: "2026-01-05",           // Data ISO (YYYY-MM-DD)
  descricao: "Salário Janeiro", // Texto livre
  categoria: "Salário",         // Uma das 11 categorias
  entrada: 5000.00,             // Valor numérico (0 se vazio)
  saida: 0.00,                  // Valor numérico (0 se vazio)
  saldo: 5000.00                // Calculado automaticamente
}
```

### Arquivo XLSX

Estrutura das colunas no Excel:

| Coluna | Tipo | Descrição |
|--------|------|-----------|
| **Data** | String | Formato: DD/MM/YYYY (na exportação) |
| **Descrição** | String | Texto descritivo |
| **Categoria** | String | Nome da categoria |
| **Entrada (+)** | Número | Formato: R$ #.##0,00 |
| **Saída (-)** | Número | Formato: R$ #.##0,00 |
| **Saldo Acumulado** | Número | Calculado progressivamente |

---

## 💾 Sistema de Armazenamento

### File System Access API (Recomendado)

**Vantagens:**
- ✅ Arquivos .xlsx reais no seu computador
- ✅ Abrir diretamente no Excel
- ✅ Backup fácil (copiar pasta)
- ✅ Sem limite de tamanho
- ✅ Compatibilidade total

**Como funciona:**
```
1. Usuário escolhe pasta "salvar"
2. Sistema guarda referência no IndexedDB
3. Toda alteração salva automaticamente em XLSX
4. Na próxima visita, reabre a mesma pasta
```

### localStorage (Fallback)

**Quando usar:**
- Firefox ou Safari
- Navegador sem suporte ao File System API

**Limitações:**
- ⚠️ Máximo ~5MB de dados
- ⚠️ Dados em JSON (não XLSX)
- ⚠️ Apenas no navegador

---

## 📤 Exportação de Dados

### 1. Exportar Ano Completo

**Botão:** "📥 Exportar XLSX"

**Arquivo gerado:** `ANO-COMPLETO-2026_05_01_2026.xlsx`

**Conteúdo:**
- ✅ **UMA única aba** com todos os 12 meses consolidados
- ✅ Dados ordenados cronologicamente
- ✅ Saldo acumulado do ano inteiro
- ✅ Formatação profissional com cores e bordas

**Ideal para:**
- Análise completa do ano
- Declaração de imposto de renda
- Relatórios financeiros

### 2. Exportar Ano Separado

**Botão:** "📥 Exportar Ano XLSX" (na aba Ano/Geral)

**Arquivo gerado:** `ANO-2026.xlsx`

**Conteúdo:**
- ✅ **12 abas** (Janeiro, Fevereiro, ..., Dezembro)
- ✅ Uma aba por mês com lançamentos
- ✅ Meses sem dados são ignorados

**Ideal para:**
- Análise mensal separada
- Compartilhar mês específico

### 3. Exportar Todos os Anos

**Botão:** "📥 Exportar Todos XLSX"

**Arquivo gerado:** `TODOS-ANOS.xlsx`

**Conteúdo:**
- ✅ **Todas as abas** de todos os anos
- ✅ Formato: `01-2024`, `02-2024`, etc.
- ✅ Histórico completo

**Ideal para:**
- Backup geral
- Migração de dados
- Análise histórica

### Formatação Excel

Todas as exportações incluem:

```
✅ Cabeçalhos azuis (#2C5F8D) com texto branco
✅ Bordas em todas as células
✅ Alinhamento apropriado (números à direita)
✅ Formato monetário brasileiro (R$ #.##0,00)
✅ Linha de totais com fundo cinza
✅ Largura de colunas otimizada
✅ Altura de linhas ajustada
```

---

## 🏷️ Categorias Disponíveis

O sistema possui **11 categorias** pré-configuradas:

### Receitas (Entradas)

| Categoria | Ícone | Uso Típico |
|-----------|-------|------------|
| **Salário** | 💼 | Salário mensal, 13º, bônus |
| **Receita Extra** | 💰 | Freelance, vendas, investimentos |

### Despesas (Saídas)

| Categoria | Ícone | Uso Típico |
|-----------|-------|------------|
| **Moradia** | 🏠 | Aluguel, condomínio, IPTU |
| **Alimentação** | 🍔 | Mercado, restaurantes, delivery |
| **Transporte** | 🚗 | Gasolina, ônibus, Uber, manutenção |
| **Saúde** | 🏥 | Plano de saúde, remédios, consultas |
| **Lazer** | 🎮 | Cinema, jogos, streaming, viagens |
| **Educação** | 📚 | Cursos, livros, faculdade |
| **Cartão de Crédito** | 💳 | Faturas de cartão de crédito |
| **Cartão de Débito** | 💳 | Compras no débito |
| **Outros** | 📦 | Despesas diversas |

> **Dica**: Use "Cartão de Crédito" para a fatura total do mês e categorize compras individuais em outras categorias.

---

## ❓ FAQ - Perguntas Frequentes

### 1. Meus dados estão seguros?

✅ **Sim!** Tudo fica no seu computador. Não há servidor externo, não enviamos nada pela internet. Você tem controle total dos seus arquivos.

### 2. Posso usar em qualquer navegador?

⚠️ **Parcialmente**. Funciona em todos, mas:
- **Chrome/Edge/Opera**: Experiência completa com arquivos .xlsx
- **Firefox/Safari**: Funciona, mas usa localStorage (limite de 5MB)

### 3. Como faço backup dos meus dados?

📁 Simples! Copie a pasta `salvar` inteira para um HD externo, nuvem, pendrive, etc.

```bash
# Backup manual
cp -r /caminho/para/salvar /backup/financeiro-2026
```

### 4. Posso editar os arquivos .xlsx direto no Excel?

✅ **Sim**, mas com cuidado:
- Não altere os nomes das colunas
- Não mude a ordem das colunas
- Mantenha o formato de data (YYYY-MM-DD)
- Salve como .xlsx (não .xls)

### 5. O que acontece se eu trocar de computador?

Copie a pasta `salvar` para o novo PC e selecione-a novamente no sistema.

### 6. Posso ter várias "pastas salvar" diferentes?

✅ **Sim!** Crie pastas diferentes:
- `salvar-pessoal/`
- `salvar-empresa/`
- `salvar-2025/`

E alterne entre elas clicando no botão "📁 salvar".

### 7. Como adiciono uma nova categoria?

Atualmente as categorias são fixas no código. Para adicionar:
1. Abra `app.html` em um editor de código
2. Procure por `const CATEGORIAS = [`
3. Adicione sua categoria na lista
4. Adicione também no `<select id="categoria">`

### 8. Posso importar dados de outro sistema?

✅ **Sim!** Crie um arquivo .xlsx com as colunas:
- `id`, `data`, `descricao`, `categoria`, `entrada`, `saida`

E use o botão "📤 Importar XLSX".

### 9. Qual o limite de lançamentos?

Não há limite fixo! Mas para melhor performance:
- ✅ Até 1.000 lançamentos/mês: Ótimo
- ⚠️ 1.000 - 5.000: Bom
- 🐢 Mais de 5.000: Pode ficar lento

### 10. Posso usar no celular?

⚠️ **Parcialmente**. O layout é responsivo, mas:
- File System API não funciona no mobile
- Use apenas em tablets/desktop para melhor experiência

---

## 🔧 Resolução de Problemas

### Problema: "Sem suporte ao acesso ao sistema de arquivos"

**Solução:**
- Use Chrome, Edge ou Opera (versão atualizada)
- Ou aceite trabalhar com localStorage

### Problema: "Permissão pendente"

**Solução:**
1. Clique novamente no botão "📁 salvar"
2. Selecione a mesma pasta
3. Clique em "Permitir" quando solicitado

### Problema: Dados sumiram após fechar o navegador

**Causa:** Você está em modo anônimo/privado

**Solução:** Use o navegador em modo normal

### Problema: Gráficos não aparecem

**Solução:**
1. Verifique sua conexão com internet (CDNs)
2. Desative bloqueadores de conteúdo
3. Recarregue a página (F5)

### Problema: Erro ao exportar "ExcelJS não carregada"

**Solução:**
- Verifique conexão com internet
- O sistema usará fallback automático (SheetJS)

### Problema: Tabela não carrega

**Solução:**
1. Abra o Console do navegador (F12)
2. Verifique erros JavaScript
3. Recarregue a página
4. Verifique se o arquivo .xlsx não está corrompido

---

## 📄 Licença

Este projeto está sob a licença **MIT**. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

```
MIT License

Copyright (c) 2026 Otavio Silva

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 📞 Contato

Encontrou um bug? Tem uma sugestão? Entre em contato:

- 📧 **Email:** otavio.silva1661@gmail.com
- 📱 **WhatsApp:** (44) 99734-1687
- 🐛 **GitHub:** [Abra uma Issue](https://github.com/Otavio1661/gestor-financeiro/issues)

> 💡 Feedbacks e sugestões são sempre bem-vindos!

---

## 🎉 Agradecimentos

Agradecimentos especiais às bibliotecas open source:

- [Bootstrap](https://getbootstrap.com/) - Framework CSS
- [Chart.js](https://www.chartjs.org/) - Gráficos
- [DataTables](https://datatables.net/) - Tabelas interativas
- [SheetJS](https://sheetjs.com/) - Manipulação XLSX
- [ExcelJS](https://github.com/exceljs/exceljs) - Excel avançado
- [SweetAlert2](https://sweetalert2.github.io/) - Alertas bonitos

---

<div align="center">

**Feito com ❤️ e ☕**

⭐ Se este projeto foi útil, dê uma estrela no GitHub!

[⬆ Voltar ao topo](#-gestor-financeiro-pessoal)

</div>
