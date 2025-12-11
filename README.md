# Capacitação em Robótica - Task Git & Docker

Este repositório contém as soluções para as tasks de ambiente de desenvolvimento e versionamento.

## Estrutura
- `/task-anterior`: Ambiente ROS básico (Task 01).
- `/turtlebot4-sim`: Ambiente para simulação do TurtleBot4 (Task 02).

## Pré-requisitos
- Docker instalado
- Git instalado

## Como usar

### 1. Build da Imagem TurtleBot4
Entre na pasta e execute:
`docker build -t turtlebot4-sim ./turtlebot4-sim`

### 2. Rodar o Container
Execute o comando abaixo para acessar o terminal do robô:
`docker run -it --rm turtlebot4-sim`