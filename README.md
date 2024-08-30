#!/bin/bash

# Defina variáveis
GITHUB_TOKEN="YOUR_GITHUB_TOKEN"
USERNAME="Eduardo"
REPO_NAME="GdakRepositorio"
REPO_DESCRIPTION="Apenas um repositorio"
IS_PRIVATE=false # 

# Crie o repositório
curl -H "Authorization: token $GITHUB_TOKEN" \
     -d "{\"name\": \"$REPO_NAME\", \"description\": \"$REPO_DESCRIPTION\", \"private\": $IS_PRIVATE}" \
     https://api.github.com/user/repos

echo "Repositório '$REPO_NAME' criado com sucesso!"
