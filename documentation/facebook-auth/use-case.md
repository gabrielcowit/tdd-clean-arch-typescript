# Autenticação com Facebook

## Dados:
* Token de Acesso

> ## Fluxo primário
1. Obter dados (nome, email e FB_ID) da API do Facebook
2. Consultar se existe um usuário com o email recebido acima
3. Criar uma conta para o usuário com os dados recebidos do FB
4. Criar um token de acesos, a partir do ID do usuário, com expiração de x minutos
5. Retornar o token de acesso gerado

> ## Fluxo alternativo: Usuário já existe
3. Atualizar a conta do usuário com os dados recebidos do Facebook (FB ID e nome - só atualizar o nome caso a conta do usuário não possua nome)

> ## Fluxo de exceção: Token inválido ou expirado
1. Retornar erro de autenticação
