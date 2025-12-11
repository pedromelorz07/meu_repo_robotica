# Base image com ROS 2 Humble (versão LTS recomendada)
FROM osrf/ros:humble-desktop-full

# Configura o shell para usar bash
SHELL ["/bin/bash", "-c"]

# Atualiza e instala ferramentas essenciais
RUN apt-get update && apt-get install -y \
    git \
    python3-colcon-common-extensions \
    python3-argcomplete \
    && rm -rf /var/lib/apt/lists/*

# Cria o workspace
WORKDIR /ros2_ws/src

# Instalação dos pacotes do TurtleBot4 Simulator
# Nota: Dependendo da versão, pode ser necessário clonar o repo oficial
# Mas muitas vezes os pacotes binários já resolvem para simulação básica
RUN apt-get update && apt-get install -y \
    ros-humble-turtlebot4-simulator \
    ros-humble-irobot-create-nodes \
    && rm -rf /var/lib/apt/lists/*

# Configuração do ambiente (source automático)
RUN echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc

# Define o diretório de trabalho padrão
WORKDIR /ros2_ws

# Comando padrão ao iniciar o container
CMD ["bash"]