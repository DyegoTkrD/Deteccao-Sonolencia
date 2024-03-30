# Detecção de Sonolência com Visão Computacional
 Este projeto Python utiliza as bibliotecas numpy, cv2 (OpenCV), e mediapipe para detectar sonolência em pessoas. Vamos explorar os conceitos de EAR (Eye Aspect Ratio) e MAR (Mouth Aspect Ratio) para mapear a abertura e fechamento dos olhos e da boca, além de calcular a contagem de piscadas por minuto. Sendo assim possível detectar a sonolência das pessoas por meio do olho fechado por mais de 3 segundos ou se os olhos piscarem menos de 15 vezes por minuto. As métricas foram criadas utilizando pesquisas sobre sonolência.

# Conceitos-Chave
1. EAR (Eye Aspect Ratio)
O EAR é uma métrica que avalia a abertura dos olhos. Ele é calculado com base nos pontos de referência dos olhos detectados na face. Quando os olhos estão fechados, o valor do EAR diminui, indicando sonolência.

2. MAR (Mouth Aspect Ratio)
O MAR é outra técnica para detectar sinais de sonolência. Ele utiliza os pontos de referência na região da boca para calcular a relação de abertura da boca. Valores maiores de MAR indicam que o indivíduo está bocejando e, portanto, apresentando sinais de sonolência.

# Implementação
1. Instale as bibliotecas necessárias:
pip install -r requirements.txt
2. Selecione a camera que será utilizada no arquivo projeto.ipynb.
3. Insira os valores de ear_limear e mar_limear, estes valores são responsáveis por definir se a boca está fechado ou aberta. (Consistem entre a média entre fechado e aberto)

# Artigos Utilizados
"Drowsiness Detection According to the Number of Blinking Eyes Specified from Eye Aspect Ratio Value Modification", escrito por Novie Pasaribu, Agus Prijono, Ratnadewi, Roy Adhie e Joseph Felix.
"Real-Time Eye Blink Detection using Facial Landmarks" de Tereza Soukupová e Jan Cech
