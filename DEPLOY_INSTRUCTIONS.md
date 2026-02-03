# Instruções para Deploy no Streamlit Community Cloud

## Passo a Passo

### 1. Preparar o Repositório GitHub

1. Crie um novo repositório no GitHub (pode ser público ou privado)
2. Clone este projeto localmente
3. Faça commit dos seguintes arquivos essenciais:
   - `app.py` (arquivo principal da aplicação)
   - `requirements.txt` (dependências Python)
   - `.streamlit/config.toml` (configurações do Streamlit)
   - `README.md` (documentação)

```bash
git init
git add app.py requirements.txt .streamlit/ README.md .gitignore
git commit -m "Initial commit - MRP System"
git remote add origin https://github.com/seu-usuario/seu-repositorio.git
git push -u origin main
```

### 2. Deploy no Streamlit Community Cloud

1. Acesse [share.streamlit.io](https://share.streamlit.io)
2. Faça login com sua conta GitHub
3. Clique em "New app"
4. Selecione:
   - **Repository**: seu repositório GitHub
   - **Branch**: main (ou master)
   - **Main file path**: app.py
5. Clique em "Deploy!"

### 3. Configurações Avançadas (Opcional)

Se você quiser usar a funcionalidade de IA, adicione secrets no Streamlit Cloud:

1. No dashboard do seu app, vá em "Settings" > "Secrets"
2. Adicione sua chave OpenAI:
```toml
OPENAI_API_KEY = "sk-sua-chave-aqui"
```

### 4. Atualizar a Aplicação

Sempre que você fizer push de novos commits para o repositório, o Streamlit Community Cloud irá automaticamente redesenhar a aplicação.

```bash
git add .
git commit -m "Atualização do sistema"
git push
```

## Limitações do Plano Gratuito

- **Recursos**: 1 GB de RAM, compartilhado
- **Upload**: Até 200 MB por arquivo (já configurado)
- **Apps**: Até 3 apps públicos ou 1 app privado
- **Tempo de inatividade**: Apps dormem após 7 dias sem uso

## Troubleshooting

### Erro de Memória
Se você tiver problemas com arquivos grandes, considere:
- Limitar o tamanho do upload
- Usar amostragem de dados
- Fazer upgrade para Streamlit Cloud Professional

### Dependências não instaladas
Certifique-se que todas as bibliotecas estão listadas no `requirements.txt`

### App não carrega
Verifique os logs do Streamlit Cloud para identificar erros de importação ou execução

## Recursos Adicionais

- [Documentação Streamlit Cloud](https://docs.streamlit.io/streamlit-community-cloud)
- [Fórum da Comunidade](https://discuss.streamlit.io)
- [Documentação API Streamlit](https://docs.streamlit.io)
