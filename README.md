# Projeto CI/CD com GitHub Actions

Pipeline de Integração Contínua (CI) e Deploy Contínuo (CD) usando GitHub Actions.

**Criador:** Alberto Oliveira

## 📁 Estrutura

- `site/` - Arquivos HTML estáticos
- `.github/workflows/` - Configurações dos workflows

## 🔍 Validações Realizadas

### CI - Integração Contínua (ci.yml)

1. **Estrutura do Projeto** - Verifica se as pastas e arquivos necessários existem
2. **Sintaxe HTML** - Valida tags obrigatórias: `<html>`, `<head>`, `<body>`
3. **Workflows YAML** - Verifica se os arquivos de configuração são válidos
4. **Testes Automatizados**:
   - Verifica se contém o título "Meu Primeiro Deploy Automatizado"
   - Confirma que o arquivo HTML não está vazio
   - Valida presença das tags `<title>`
   - Confirma que o charset está definido
5. **Relatório de CI** - Gera arquivo com resumo das validações
6. **Upload de Artefatos** - Armazena relatório por 30 dias

### CD - Deploy Contínuo (cd.yml)

1. **Preparação de Artefatos** - Copia arquivos para o diretório `build/`
2. **Setup GitHub Pages** - Configura o ambiente de deploy
3. **Upload** - Envia arquivos para o GitHub Pages
4. **Deploy** - Publica o site
5. **Verificação de Saúde** - Valida se o site foi publicado corretamente
6. **Relatório de Deploy** - Gera arquivo com informações do deploy

## ⚙️ Gatilhos

- **CI**: Ativado por push ou pull request nas branches `main` e `develop`
- **CD**: Ativado por push na branch `main` após sucesso do CI

## 🌐 Site Publicado

Após deploy bem-sucedido, o site fica disponível em:
