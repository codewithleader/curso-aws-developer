# CIDR: Classless Inter-Domain Routing: Enrutamiento entre Dominios sin Clases

Se introdujo en 1993 por IETF y representa la última mejora en el modo de interpretar las direcciones IP.1​ Su introducción permitió una mayor flexibilidad al dividir rangos de direcciones IP en redes separadas. De esta manera permitió:

  - Un uso más eficiente de las cada vez más escasas direcciones IPv4.
  - Un mayor uso de la jerarquía de direcciones (agregación de prefijos de red), disminuyendo la sobrecarga de los enrutadores principales de Internet para realizar el encaminamiento.

- CIDR usa la técnica VLSM (variable length subnet mask: máscara de subred de longitud variable)

Decimos que una dirección IP está incluida en un bloque CIDR, y que encaja con el prefijo CIDR, si los N bits iniciales de la dirección y el prefijo son iguales. Por tanto, para entender CIDR es necesario visualizar la dirección IP en binario. Dado que la longitud de una dirección IPv4 es fija, de 32 bits, un prefijo CIDR de N-bits deja 32 32-N bits sin encajar, y hay 2^(32−N) combinaciones posibles con los bits restantes. Esto quiere decir que 2^(32−N) direcciones IPv4 encajan en un prefijo CIDR de N-bits.

Nótese que los prefijos CIDR cortos (números cercanos a 0) permiten encajar un mayor número de direcciones IP, mientras que prefijos CIDR largos (números cercanos a 32) permiten encajar menos direcciones IP.

Ejemplo:

el bloque 208.130.28.0/22, capaz de admitir 1024 direcciones IP:
32−22=10 ==>> Acá 22 es N (32-N)
2^10=1.024