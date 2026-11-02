# Detecção de sonolência com visão computacional

Detecta sinais de sonolência em tempo real pela câmera, usando os pontos do rosto mapeados pelo MediaPipe. O projeto mede a abertura dos olhos e da boca e conta as piscadas por minuto.

![Detecção em tempo real: EAR, MAR, piscadas por minuto e alerta de olhos fechados](imagens/deteccao.jpg)

## Como funciona

1. O MediaPipe Face Mesh localiza os pontos de referência dos olhos e da boca em cada quadro capturado com OpenCV.
2. Com esses pontos, o código calcula duas métricas:
   - **EAR (Eye Aspect Ratio):** relação de abertura dos olhos. Cai quando o olho fecha.
   - **MAR (Mouth Aspect Ratio):** relação de abertura da boca. Sobe quando a pessoa boceja.
3. O sistema aponta sonolência quando:
   - os olhos ficam fechados por **mais de 3 segundos**; ou
   - a pessoa pisca **menos de 15 vezes por minuto**.

Os limites vêm dos artigos citados abaixo.

## Como rodar

```bash
git clone https://github.com/DyegoTkrD/Deteccao-Sonolencia
cd Deteccao-Sonolencia
python -m venv .venv
source .venv/bin/activate   # no Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook projeto.ipynb
```

No notebook:
1. Escolha a câmera que será usada.
2. Ajuste `ear_limiar` e `mar_limiar`, os limites que separam olho e boca abertos de fechados. Um bom ponto de partida é a média entre o valor medido com olho (ou boca) aberto e fechado.

## Stack

Python · OpenCV · MediaPipe · NumPy

## Referências

- Pasaribu, N.; Prijono, A.; Ratnadewi; Adhie, R.; Felix, J. *Drowsiness Detection According to the Number of Blinking Eyes Specified from Eye Aspect Ratio Value Modification.*
- Soukupová, T.; Čech, J. *Real-Time Eye Blink Detection using Facial Landmarks.*

---

Feito por [Dyego Seabra](https://dyegoseabra.com.br) · [LinkedIn](https://www.linkedin.com/in/dyegoseabradata)
