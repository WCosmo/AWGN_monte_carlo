# AWGN com Monte Carlo
Autor: Wilson Cosmo
Data: 2026-05-01

Simulação física do canal LoRa P2P usando o método Monte Carlo:

1. Modulação CSS (Chirp Spread Spectrum) - geração de up-chirps
2. Canal AWGN com potência de ruído controlada pela variável IR (SNR em dB)
3. Demodulação via de-chirping (multiplicação por down-chirp) + FFT
4. Decodificação de símbolos para bits
5. Estimativa estatística de BER e PDR sobre N realizações independentes

Parâmetros configuráveis:
- N  : Número de pacotes (realizações Monte Carlo)
- T  : Tamanho do pacote em bytes
- IT : Intervalo entre pacotes em ms
- IR : Intensidade do Ruído (SNR em dB)
- SF : Spreading Factor (6-12)
- Freq: Frequência de operação (Hz)
- BW : Bandwidth (Hz)

Métricas de saída:
- BER : Bit Error Rate
- PER : Packet Error Rate
- PDR : Packet Delivery Rate (pacotes inteiros)
