# exercicio_1
Repositório para exercitar git e pre-processamento de imagens
## Tarefas do Exercício
1. Leitura e Padronização:
- Leia a imagem original do disco.
- Redimensione a imagem para um tamanho padrão (por exemplo, 800x600) para facilitar o processamento.
2. Correção de Perspectiva (Envelopamento):
- Defina os 4 pontos de origem (os cantos distorcidos da bandeja na foto) e os 4 pontos de destino (os cantos de um retângulo perfeito).
- Utilize as funções matemáticas do OpenCV para realizar o warp perspective (envelopamento), gerando uma nova imagem onde a bandeja aparece perfeitamente vista de cima.
3. Pré-processamento e Mudança de Cor:
- Converta a imagem "envelopada" de BGR para Tons de Cinza.
- Aplique um desfoque (Blur) e um limiar (Threshold) ou Canny para criar uma máscara binária (fundo preto e objetos brancos).
Operações Morfológicas:
- A máscara gerada provavelmente terá ruídos (pontos brancos isolados) e falhas dentro das peças (buracos pretos).
- Utilize operações de Abertura (Opening) para remover os ruídos externos.
- Utilize operações de Fechamento (Closing) para preencher os buracos dentro dos componentes.
4. Separação de Objetos e Gravação:
- Encontre os contornos das peças na máscara morfológica.
- Para cada peça encontrada, desenhe um retângulo delimitador (Bounding Box) na imagem cinza original (para visualização).
- Recorte (crop) a região de cada peça usando as coordenadas do retângulo.
- Salve cada recorte como um arquivo de imagem individual (ex: peca_1.jpg, peca_2.jpg) em uma pasta específica.
