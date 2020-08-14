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
