# ZBX-GRA-ALIGERA
Teamplate_Aligera_AG562_E1_ZABBIX-5 e Grafana Dashboard

### PT-BR ###

## HOMOLOGADO PARA: ##
- Zabbix 5.0.15
- Grafana 7.3.6
- Aligera AG562 (Current running firmware is: AG562 - 5.46)
- MIB Aligera https://docs.aligera.com.br/images/b/b5/ALIGERA-MIB.mib 


## PASSOS: ##
### No Zabbix.. ###
- Importe o TEMPLATE_TELEFONIA_AG562_E1_LLD_SNMP_ZBX-5.0 para o Zabbix.
- Crie um host com o nome iniciando com "E1-" (Usei variáveis com REGEX /E1-.*/ para uma melhor experiência). Mais fique a vontade para ajustar à sua realidade.
- O Hostgroup use o nome "TELEFONIA" e vincular o modelo ao host. 
- Para a interface use o tipo SNMP, informe o IP do Aligera.
- Atribua o template importado ao host.
- Aguarde a coleta de dados ou use a função "Verificar agora" no item e no LLD para acelerar a coleta.

### No Grafana.. ###
- Certifique-se de ter o Plugin: alexanderzobnin-zabbix-app - https://grafana.com/grafana/plugins/alexanderzobnin-zabbix-app instalado e configurado. Para ao importar o Modelo para Grafana, podermos selecionar a Fonte de Dados que é o Zabbix.


![alt text](https://github.com/boldrinidouglas/ZBX-GRA-ALIGERA/raw/main/GRAFANA-E1-ZABBIX-DASH.png "Grafana")
