# IMP006A Zj-58
Driver Linux da Impressora Bluetooth IMP006A Zj-58 POS

Se você quer usar esta impressora apenas conectada a interface USB, somente instale o driver usando:
~~~
sudo chmod +x install58
~~~
E então:
~~~
sudo ./install58
~~~
## Abaixo está como configurar a IMP006A ou a Impressora Bluetooth Zj-58 no linux pela conexão Bluetooth.

_Nota: estas configurações também se aplicam aos modelos GO HIT XPJ-58* (testado)_
### 1
Autorize o sistema a executar o script de instalação do driver. Abra um terminal na pasta onde se encontram os drivers e digite:
~~~
sudo chmod +x install58
~~~
e depois execute o script com:
~~~
sudo ./install58
~~~
### 2
Instale o CUPS com:
~~~
sudo apt install cups
~~~
### 3
Instale o bluez-cups com:
~~~
sudo apt install bluez-cups
~~~
_Isso permite ao CUPS usar o protocolo bluetooth_
### 4
Sincronize a impressora bluetooth com teu computador. Use as senhas 1234 ou 0000. Ou use as senhas padronizadas de acordo com o teu fabricante.
### 5
Tome uma nota com o endereço bluetooth da impressora. Exemplo: 0f:08:09:07:0b:08
### 6
Abra no navegador o server do CUPS em http://localhost:631/admin e vá até 'add printer'
### 7
Insira tuas credenciais de acesso root(superuser)
### 8
Selecione 'LPD/LPR Host or Printer'
### 9
No campo URI preencha com:
~~~
bluetooth://0f0809070b08
~~~
onde "_0f0809070b08_" é o endereço da impressora em questão sem os pontos entre os números.
### 10
Selecione o arquivo POS58.ppd se necessário e clique 'ADD Printer'
### 11
Vá para o arquivo que você deseja imprimir ou abra o software onde a impressão será realizada...
### 12
Cheque as predefinições do papel e mande isto para a fila de impressão.

#### CUPS link:
https://github.com/apple/cups/releases
#### BLUEZ-CUPS links:
https://packages.debian.org/sid/admin/bluez-cups

https://www.archlinux.org/packages/extra/x86_64/bluez-cups/
