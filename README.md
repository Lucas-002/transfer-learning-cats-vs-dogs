# Classificação de Gatos e Cachorros com Transfer Learning

Este projeto utiliza transfer learning com o modelo pré-treinado VGG16 para realizar a classificação de imagens de gatos e cachorros. O dataset utilizado é o **Cats and Dogs Filtered**, fornecido pelo TensorFlow.

## Configuração do Ambiente

Certifique-se de ter o Python instalado junto com as bibliotecas abaixo:

- TensorFlow
- NumPy
- Matplotlib
- wget

### Instalação das Dependências

```bash
pip install tensorflow numpy matplotlib wget
```

## Dataset

O dataset é baixado automaticamente a partir do link: [Cats and Dogs Filtered Dataset](https://storage.googleapis.com/mledu-datasets/cats_and_dogs_filtered.zip). Ele contém imagens de gatos e cachorros divididas em pastas de treino e validação.

## Arquitetura do Modelo

O modelo utiliza a rede VGG16 pré-treinada com os pesos do ImageNet. A parte superior do modelo é substituída por camadas personalizadas:

- Camada `Flatten`
- Camada totalmente conectada com 256 neurônios e ativação ReLU
- Dropout de 50%
- Camada de saída com 1 neurônio e ativação sigmoid

## Métricas de Desempenho

O modelo foi treinado por 10 épocas com os seguintes resultados na validação:

- **Loss**: 0.1897
- **Accuracy**: 92.70%

## Gráficos de Métricas

Abaixo estão os gráficos de perda e acurácia durante o treinamento:

![Gráficos]("C:\Users\Ghost\Pictures\Screenshots\Captura de tela 2024-12-13 103234.png")

## Como Executar o Código

1. Clone este repositório:

```bash
git clone <url-do-repositório>
cd <nome-do-repositório>
```

2. Execute o script principal:

```bash
python main.py
```

3. Os resultados e os gráficos serão exibidos ao final do treinamento.

## Melhorias Futuras

- Adicionar data augmentation mais avançado.
- Testar diferentes arquiteturas de redes neurais.
- Implementar uma interface gráfica para carregamento e predição de imagens personalizadas.

---

Este projeto foi desenvolvido com o objetivo de explorar conceitos de aprendizado de máquina e visão computacional utilizando transfer learning.

