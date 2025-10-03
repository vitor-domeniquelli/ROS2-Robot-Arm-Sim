# ROS2-Robot-Arm-Sim

# Projeto: Simulação de Robô Manipulador Acoplado a Cadeira de Rodas

## Visão Geral

Este repositório apresenta o trabalho de desenvolvimento e simulação de um braço robótico manipulador projetado para ser acoplado a uma cadeira de rodas, visando auxiliar pacientes com dificuldades de locomoção. O projeto utiliza o Robot Operating System (ROS 2) para simulação em ambiente virtual e explora a cinemática do robô para controle via joystick.

## Motivação e Objetivos

A dificuldade de locomoção afeta uma parcela significativa da população. Tecnologias assistivas, como braços robóticos montados em cadeiras de rodas (WMRA - Wheelchair Mounted Robotic Arm), oferecem maior autonomia e acessibilidade.

Os principais objetivos deste projeto são:
*   **Simular** o funcionamento de um robô manipulador controlado via joystick e acoplado a uma cadeira de rodas.
*   **Avaliar** a usabilidade, eficácia e segurança desta tecnologia em ambiente virtual.
*   **Estabelecer** uma prova de conceito para futuras implementações físicas.

## Metodologia

O projeto foi dividido nas seguintes etapas principais:

1.  **Modelagem:** Criação dos modelos dos elos e juntas do robô utilizando o formato URDF (Unified Robot Description Format).
2.  **Cinemática:** Dedução e cálculo do modelo cinemático direto e inverso do robô.
3.  **Simulação:** Implementação e simulação do robô em ambiente virtual utilizando ROS 2 (com ferramentas como RViz e Joint_state_publisher).
4.  **Controle:** Desenvolvimento do controle do modelo virtual, com foco no controle via joystick.

## Estrutura do Repositório

*   **`README.md`**: Este arquivo, fornecendo uma visão geral do projeto.
*   **`docs/`**: Contém a proposta do projeto, apresentações e outros documentos de apoio.
*   **`src/`**: Código-fonte do projeto, incluindo a descrição URDF do robô e scripts de lançamento do ROS.
*   **`media/`**: Imagens e vídeos da simulação do robô.
*   **`references/`**: Artigos científicos, trabalhos de graduação e outras referências bibliográficas utilizadas no desenvolvimento do projeto.

## Como Usar/Reproduzir (Exemplo para ROS 2)

Para reproduzir a simulação do robô, você precisará ter o ROS 2 (preferencialmente Foxy Fitzroy ou superior) instalado em seu sistema.

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/vitor-domeniquelli/ROS2-Robot-Arm-Sim.git](https://github.com/vitor-domeniquelli/ROS2-Robot-Arm-Sim.git)
    cd seu-repositorio
    ```
2.  **Crie um workspace ROS 2 e copie o pacote do robô:**
    ```bash
    mkdir -p ~/ros2_ws/src
    cp -r src/modelo_robo ~/ros2_ws/src/
    cd ~/ros2_ws
    ```
3.  **Compile o pacote:**
    ```bash
    colcon build --packages-select modelo_robo
    ```
4.  **Fonte o ambiente:**
    ```bash
    . install/setup.bash
    ```
5.  **Lance a simulação no RViz:**
    ```bash
    ros2 launch modelo_robo display.launch.py
    ```
    Isso abrirá o RViz com o modelo do robô. Você poderá interagir com as juntas usando os sliders no Joint State Publisher.

## Principais Tecnologias

*   **Robot Operating System (ROS 2):** Framework para desenvolvimento de software robótico.
*   **URDF (Unified Robot Description Format):** Linguagem de descrição de robôs em XML.
*   **RViz:** Ferramenta de visualização 3D para ROS.
*   **Python:** Linguagem de programação principal para scripts e nós ROS.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests para melhorias, correções de bugs ou novas funcionalidades.

## Contato

Vitor Domeniquelli Chagas - vdchagas@gmail.com
