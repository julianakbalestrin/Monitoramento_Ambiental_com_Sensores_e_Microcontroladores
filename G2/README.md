# G2 · Experimento C: dispersão de sal com condutivímetros

Condutivímetro de baixo custo (Wemos D1 mini / ESP8266, sensor TDS, termômetro DS18B20, RTC DS3231 e cartão microSD) testado em canal de laboratório de inclinação variável, com pulsos de NaCl, para estimar velocidade e coeficiente de dispersão longitudinal.

Entrega: 28/11/2026 (relatório em PDF, apresentação e todos os códigos, num único zip). Apresentação: 30/11/2026. Ver `referencias/enunciado_G2.pdf`.

## Conteúdo

| Caminho | O que é |
|---|---|
| `firmware/datalogger_sd/` | datalogger com gravação no microSD, copiado do roteiro da Aula 07 (`platformio.ini` + `src/main.cpp`) |
| `dados/brutos/sensor_data_canal_2026-11-09.csv` | ensaio no canal (09/11/2026): 5 placas, enviado por Wi-Fi |
| `dados/brutos/aula07_sensorA_2026-09-28.txt`, `aula07_sensorC_2026-09-28.txt` | cartão microSD dos sensores A e C: teste da Aula 07 (28/09), calibração (05/10) e ensaio no canal de 26/10/2026 (gravado com a data errada, 05/10, entre 16:24 e 16:54) |
| `dados/brutos/aula07_sensorE_2026-10-05.txt` | cartão microSD do sensor E no ensaio de 26/10/2026 (relógio cerca de 2 h 19 min atrasado) |
| `dados/calibracao/calibracao.txt` | calibração da sonda A em concentração (05/10/2026) |
| `dados/coeficiente_dispersao_sal.xlsx` | planilha dos experimentos 1 a 5 |
| `notebooks/processamento_dispersao.ipynb` | processamento principal: calibração, momentos, dispersão, figuras e tabelas |
| `notebooks/validacao_independente.ipynb` | validação independente da propagação A → E |
| `notebooks/experimento_2610.ipynb` | ensaio de 26/10/2026 (sensores A, C e E): sincronização dos relógios, momentos, U e D_L, figuras F12 a F14; baixa os três arquivos do Drive |
| `figuras/foto_prototipo.jpg` | foto do protótipo |
| `figuras/quadro_esquema_canal_2026-10-07.jpeg` | esquema do canal e das posições das sondas, no quadro |
| `relatorio/relatorio.tex` | fonte LaTeX do relatório (em andamento) |
| `relatorio/Relatorio_G2_PLANT_HARRISON.pdf` | versão em PDF do relatório |
| `referencias/` | enunciado do G2 e roteiro da Aula 07 |

## Como reproduzir

Abra os notebooks no Google Colab e execute tudo. Eles baixam `sensor_data.csv` e `calibracao.txt` do Google Drive; se o download falhar, faça o upload dos arquivos de `dados/`. As figuras e tabelas são gravadas em pastas `figuras/` e `tabelas/` no ambiente do Colab.

## Pendências

- Firmware com envio por Wi-Fi/MQTT usado no ensaio de 09/11 (o relatório cita essa versão).
- Figuras referenciadas pelo `relatorio.tex` (`figuras/F*.pdf` do ensaio de 09/11; as F12 a F14, de 26/10, já estão na pasta; `esquema_ligacoes.pdf`, `esquema_canal.png`, `fundo`): gerar com os notebooks e copiar para `figuras/`.
- Arquivo da apresentação.
