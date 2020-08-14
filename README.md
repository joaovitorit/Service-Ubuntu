# Service-Ubuntu

#### CRIAR SERVIÇO NO UBUNTU

1 - CRIE UM ARQUIVO NO CAMINHO /etc/systemd/system/nomedoserviço.service

#### Exemplo do conteúdo

[Unit]

Description=Node Exporter

After=network.target

[Service]

User=node_exporter

Group=node_exporter

Type=simple

ExecStart=/usr/local/bin/node_exporter

[Install]

WantedBy=multi-user.target

2 - DIGITE:
OBS. ESSE COMANDODÁ UM RELOAD NOS SERVIÇOS DA PASTA MENCIONADA NO ITEM 1

systemctl daemon-reload  

3 - AGORA VAMOS INICIAR O SERVIÇO DIGITANDO

systemctl start node_exporter.service

4 - AGORA VAMOS CERTIFICAR QUE O SERVIÇO FOI INICIADO COM SUCESSO

systemctl status node_exporter.service


