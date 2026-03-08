# DevContainer Templates

Colección de plantillas de devcontainer para diferentes tecnologías.

## 📚 Templates disponibles

| Template | Descripción | Tecnologías |
|----------|-------------|-------------|
| [lunarvim](./templates/lunarvim) | Entorno con LunarVim | Alpine, Rust, Python, Node |

## 🔧 Cómo usar

```bash
# Clonar el repo
git clone https://github.com/joanmat117/devcontainer-templates.git

# Copiar el template que necesites a tu proyecto
cp -r devcontainer-templates/templates/lunarvim/.devcontainer/ tu-proyecto/

# Abrir en VS Code / Codespaces
code tu-proyecto
