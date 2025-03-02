# Sistema de Proteção de Dados Baseado em Técnicas de Criptografia e Anonimização (Back-end)

A API SysPAD consiste em um sistema RESTful para proteção de bancos de dados através de criptografia e anonimização, seguindo os princípios das legislações LGPD e GDPR. Este componente é responsável pelo processamento seguro de dados e integração com o agent monitor e front-end.

# Estrutura do readme.md

Este documento está organizado nas seguintes seções principais:

1. **Funcionalidades-Chave**  
   Principais capacidades técnicas do sistema

2. **Documentação Técnica**  
   Detalhes de endpoints e especificação OpenAPI

3. **Tecnologias Utilizadas**  
   Stack tecnológico completo do back-end

4. **Instalação**  
   Guia completo para implantação (Docker e manual)

5. **Configuração de Ambiente**  
   Variáveis necessárias e pré-requisitos

6. **Usuários de Teste**  
   Credenciais pré-configuradas para validação

7. **Estrutura do Repositório**  
   Organização de diretórios e arquivos-chave

8. **Contribuição**  
   Diretrizes para colaboração no projeto

9. **Licença**  
   Direitos de uso e informações legais

# DependÊncias 
Tecnologias Utilizadas
Componente	Versão	Finalidade
Python	3.10+	Lógica principal do sistema
Flask	2.3.x	Framework web para APIs
SQLAlchemy	2.0.23	ORM para operações de banco
Cryptography	41.0.3	Implementação de criptografia
Flask-SQLAlchemy	3.0.3	Integração com bancos de dados
Swagger UI	4.19.0	Documentação interativa de APIs

# Instalação

Método 1: Instalação Manual
```bash
Copy
git clone https://github.com/FRIDA-LACNIC-UECE/back-end.git
cd back-end

python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Configurar variáveis de ambiente
export FLASK_APP=application.py
export DATABASE_URL="mysql://user:password@localhost/db_name"
export SECRET_KEY="chave_secreta_aleatoria"

# Inicializar banco de dados
flask create_db

# Iniciar serviço
flask run --port=5000
Método 2: Via Docker
bash
Copy
docker compose up --build
```

# Variáveis necessárias no .env
## Usuários de Teste

| Perfil        | Email                   | Senha         | Acessos               |
|---------------|-------------------------|---------------|-----------------------|
| Administrador | admin@example.com       | Admin@123     | Controle completo     |
| Convidado      | convidado@example.com   | Convidado@123 | Operações limitadas   |

# Licença
Este projeto não possui licença específica, podendo ser utilizado livremente para fins acadêmicos e de pesquisa. Para uso comercial, entre em contato com LARCES/UECE.
