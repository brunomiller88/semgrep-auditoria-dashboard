📄 README.md 
# 🔍 Auditoria de Código com Semgrep (SAST) + Dashboard HTML

Este repositório demonstra um fluxo completo de **análise estática de código (SAST)** utilizando **Semgrep**, ferramenta amplamente usada por equipes de **DevSecOps**, **AppSec**, **Segurança da Informação** e **Pentest Interno**.

O objetivo deste projeto é mostrar, na prática, como:

- Instalar e configurar o Semgrep em um ambiente seguro  
- Realizar auditoria completa de um código-fonte  
- Gerar relatórios JSON  
- Criar um **dashboard HTML elegante** exibindo vulnerabilidades  
- Organizar tudo em um repositório profissional no GitHub  

---

# 🛡 O que é o Semgrep?

O **Semgrep** é uma ferramenta de **análise estática de código (SAST)** que identifica vulnerabilidades, más práticas e violações de segurança *antes* que o código seja executado ou enviado para produção.

Utilizada por times de:

- 🔵 DevSecOps  
- 🟣 AppSec  
- 🔴 Segurança interna  
- 🟠 Pentest de aplicações  
- 🟢 Auditorias de conformidade  

O Semgrep atua no conceito **shift-left**, onde a segurança acontece cedo no pipeline, evitando riscos antes do deploy.

Ele detecta problemas como:

- SQL Injection  
- Command Injection  
- Unsafe eval()  
- CORS misconfiguration  
- XSS  
- Hardcoded secrets  
- Unsafe function calls  
- Erros comuns em PHP, JS, Python, Go, Java, etc.  

E usa regras da comunidade ou personalizadas.

---

# ⚠️ Importante antes de começar

Recomenda-se utilizar o Semgrep dentro de uma **máquina virtual (VM)** e em um **ambiente virtual Python (venv)**.

Isso evita quebrar dependências do Kali Linux e garante isolamento seguro.

---

# 📦 1. Instalar dependências

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install python3 python3-pip git -y

🧩 2. Criar ambiente virtual (venv)
mkdir ~/semgrep-env
cd ~/semgrep-env
python3 -m venv venv


Ativar:

source venv/bin/activate

🛠️ 3. Instalar o Semgrep
pip install semgrep


Verificar:

semgrep --version

🔎 4. Rodar uma análise de código

Entre na pasta do seu código:

cd /caminho/do/projeto


Execute:

semgrep scan --config auto . --json --output semgrep-resultados.json


Isso gera um arquivo JSON com todas as vulnerabilidades detectadas.

🎨 5. Gerar Dashboard HTML Profissional

Crie o script abaixo dentro do seu ambiente (gera_html_semgrep.py):

Execute:

python3 gera_html_semgrep.py


Será criado:

semgrep-relatorio.html


Abra no navegador:

xdg-open semgrep-relatorio.html

📊 6. Exemplo do dashboard gerado

O relatório exibe:

Severidade

Regra violada

Descrição da vulnerabilidade

Caminho do arquivo

Linha e coluna do problema

Inclui:

Fundo gradiente moderno

Layout escuro

Cards de contagem

Tabela organizada

Ideal para:

auditorias internas

envio para gestão

evidências de DevSecOps

documentação de segurança

Conclusão

Este repositório demonstra de forma clara e profissional como aplicar auditoria de código com Semgrep, gerando evidências visuais e organizadas das vulnerabilidades detectadas.

É um fluxo real utilizado em pipelines de DevSecOps e auditorias corporativas.
