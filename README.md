# Projeto Integrado - Especialização em Aprendizado de Máquina e Inteligência Artificial 

***Este projeto mostra todo o processo de treino, validação e teste em um projeto de machine learning.***</br>
***O processo de colocar em produção será também mostrado a seguir.***

O estudo trata dos efeitos de degradação de imagens em redes CNN com grandes melhorias em redes em cápsula.

***O repositório oficial do projeto está em [Effects of Degradations on Deep Neural Network Architectures](https://arxiv.org/abs/1807.10108).***
## Citação
```
@article{roy2018effects,
  title={Effects of Degradations on Deep Neural Network Architectures},
  author={Roy, Prasun and Ghosh, Subhankar and Bhattacharya, Saumik and Pal, Umapada},
  journal={arXiv preprint arXiv:1807.10108},
  year={2018}
}
```

## Instalação

O Código roda no Python 3.6

#### Instalando dependências:
```
pip install numpy scipy pandas matplotlib opencv-python tensorflow keras
```
```
pip install git+https://github.com/prasunroy/mlutils.git
```
##### OBS: é necessário instalar o tensorflow 2.0

## Dataset
O estudo utiliza dois grupos de dataset: Syntetic Digits e Natural Images

### Synthetic Digits
Foi gerado um dataset sintético com dígitos de 0 a 9 com fundo aleatório. Foram utilizadas uma variação de fontes, escalas e rotação. O total de imagens são 12000. O dataset está disponível em [*Kaggle*](https://www.kaggle.com/prasunroy/synthetic-digits).

A forma mais prática de baixar é utilizando a [*Kaggle API*](https://github.com/Kaggle/kaggle-api) `kaggle datasets download -d prasunroy/synthetic-digits`

Abaixo temos um exemplo das imagens sintéticas geradas:

![image](https://github.com/prasunroy/cnn-on-degraded-images/blob/master/assets/image_01.png)

### Natural Images
São 8 classes de diversas fontes: aviões, carros, gatos, cachorros, flores, frutas, motocicletas e pessoas. Representam um total de 6899 imagens. A base de dados também está disponível no [*Kaggle*](https://www.kaggle.com/prasunroy/natural-images).

A forma mais prática de baixar é utilizando a [*Kaggle API*](https://github.com/Kaggle/kaggle-api) `kaggle datasets download -d prasunroy/natural-images`

Abaixo temos um exemplo das imagens naturais geradas:

![image](https://github.com/prasunroy/cnn-on-degraded-images/blob/master/assets/image_02.png)

## Etapa de treinamento
>Dentro dos arquivos há a seção *`configurations`* a qual define vários parâmetros de treio os quais podem ser alterados diretamente antes do treinamento.

#### Treinando a deep convolutional neural network
```
python train_deepcnn.py
```

#### Treinando a capsule network
```
python train_capsnet.py
```

## Testando os modelos
>Dentro do arquivo há a seção *`configurations`* a qual também define vários parâmetros de teste. Estes parâmetros também podem ser alterados antes de se executar o script de teste.
```
python test.py
```


