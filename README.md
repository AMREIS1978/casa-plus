# MyGGas Radar + EcoDrive

## Novas opções
### MyGGas Radar
- ativar/desativar;
- confirmação de preços;
- pontos;
- distância e limites de alertas.

### MyGGas EcoDrive
- ativar/desativar independentemente;
- alerta de excesso de velocidade;
- tolerância configurável;
- opção de sugestões de condução eficiente;
- frequência de alertas configurável;
- leitura da velocidade por GPS;
- consulta do `maxspeed` OpenStreetMap quando existe;
- sem alerta de excesso quando o limite não é conhecido;
- aviso claro de que a sinalização rodoviária prevalece.

## Otimização de consumo
O EcoDrive desta versão não mede consumo real do veículo. As sugestões usam velocidade GPS e variação de velocidade:
- aceleração progressiva;
- evitar acelerações/desacelerações fortes;
- manter velocidade estável;
- aviso de que velocidades elevadas aumentam o consumo.

Para consumo real (L/100 km, carga do motor, rpm, etc.) a evolução correta é integração OBD/Bluetooth.

## Segurança
A funcionalidade é opcional. Não deve ser usada como substituto da sinalização rodoviária ou do velocímetro do veículo.
