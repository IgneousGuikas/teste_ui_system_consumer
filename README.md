Este projeto exige uma configuração especial para aplicar o projeto provider como sub-módulo deste:

```bash
// Definir pasta como sub-módulo
git submodule add -b <branch-name> <repo_url> <path_to_submodule_folder>

// Atualizar sub-módulos com a versão mais atualizada dos repositórios remotos
git submodule update --remote

// Clonar repositório junto com os sub-módulos
git close --recurse-submodules

// Dar pull junto com os sub-módulos
git pull --recurse-submodules

// Configurar alias com esses comandos
git config --global alias.clone-all 'clone --recurse-submodules'
git config --global alias.pull-all 'pull --recurse-submodules'
```