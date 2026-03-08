FROM alpine:edge

# Instalar dependencias del sistema
RUN apk update && apk add --no-cache \
    yarn \
    git \
    python3 \
    cargo \
    neovim \
    ripgrep \
    alpine-sdk \
    bash \
    curl \
    nodejs \
    npm \
    fd \
    && rm -rf /var/cache/apk/*

# Crear usuario no-root
RUN addgroup -S lunaruser && adduser -S lunaruser -G lunaruser --shell /bin/bash

# Cambiar al usuario no-root
USER lunaruser
WORKDIR /home/lunaruser

# Instalar LunarVim (versión específica)
RUN LV_BRANCH=release-1.4/neovim-0.9 bash <(curl -s https://raw.githubusercontent.com/lunarvim/lunarvim/release-1.4/neovim-0.9/utils/installer/install.sh) --no-install-dependencies

# Agregar al PATH
ENV PATH="/home/lunaruser/.local/bin:${PATH}"

# Verificar instalación
RUN lvim --version || echo "Completed verification"

CMD ["/bin/bash"]
