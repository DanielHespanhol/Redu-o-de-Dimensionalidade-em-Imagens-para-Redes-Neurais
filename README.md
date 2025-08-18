# Processamento de Imagens: Redução de Dimensionalidade
Este projeto demonstra técnicas fundamentais de processamento de imagens para redução de dimensionalidade, implementado em Python com OpenCV e NumPy. O código foi otimizado para execução no Google Colab.

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

# 📌 Visão Geral
O objetivo deste projeto é mostrar o pipeline completo de redução de dimensionalidade em imagens, incluindo:

- Redimensionamento inteligente
- Conversão para escala de cinza
- Binarização com threshold ajustável
- Método de Otsu para threshold automático
- Análise estatística dos resultados

# 🛠️ Funcionalidades Principais
redimensionar_imagem(): Reduz dimensões mantendo proporções

converter_para_cinza(): Transforma RGB em escala de cinza (fórmula: 0.299R + 0.587G + 0.114B)

binarizar_imagem(): Converte para preto e branco com threshold configurável

encontrar_melhor_threshold(): Usa método de Otsu para threshold automático

Visualização comparativa: Exibe original, cinza e binária lado a lado

Análise estatística: Calcula distribuição de pixels e valores médios

# 🚀 Como Executar

No Google Colab: 

    # Substitua pelo caminho da sua imagem
    caminho_imagem = "/content/sua_imagem.jpg"

    # Processamento completo
    original, cinza, binaria = processar_imagem(caminho_imagem)

    # Threshold automático com Otsu
    melhor_threshold = encontrar_melhor_threshold(cinza)
    print(f"Threshold ótimo: {melhor_threshold}")
    
Testar múltiplos thresholds:

    testar_multiplos_thresholds(caminho_imagem, thresholds=[64, 128, 192])
    
# 📊 Saída Esperada
Visualização em 3 estágios:
- Imagem original (RGB)
- Versão em escala de cinza
- Versão binarizada

Estatísticas:
- Dimensões da imagem
- Valores mínimo/máximo/médio de intensidade
- Distribuição de pixels pretos/brancos

# 📚 Métodos Implementados
1. Conversão para cinza: Fórmula de luminosidade padrão
2. Binarização:
  - Threshold fixo (default=128)
  - Threshold automático (método de Otsu)

Redimensionamento: Mantém aspect ratio sem aumentar imagens

# 💻 Requisitos
- Python 3.x
- OpenCV
- NumPy
- Matplotlib

# 📌 Exemplo de Uso

    # Processamento completo com salvamento
    processar_imagem("foto.jpg", threshold=150, salvar_resultados=True)

    # Saída:
    # Imagens salvas: foto_cinza.jpg e foto_binaria.jpg
    
# 📈 Aplicações
- Pré-processamento para visão computacional
- Redução de dimensionalidade para ML
- Análise de padrões em imagens
- Sistemas de OCR (pré-processamento)

# 🛠️ Estrutura do Código
- Processamento principal: processar_imagem()
- Conversões:
    - converter_para_cinza()
    - binarizar_imagem()
- Otimização:
    - redimensionar_imagem()
    - encontrar_melhor_threshold()
- Visualização:
    - Comparação lado a lado
    - Teste de múltiplos thresholds
