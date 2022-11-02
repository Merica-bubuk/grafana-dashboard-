version: '2'
services:
  grafana:
    image: grafana/grafana:8.4.5-ubuntu
    ports:
      - "3000:3000"
    environment:
      - GF_INSTALL_PLUGINS=grafana-clock-panel,grafana-simple-json-datasource
    volumes:
      - grafana-new:/var/lib/grafana

volumes:
  grafana-new: 
