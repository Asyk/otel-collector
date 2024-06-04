# otel-collector
Настроенный коллектор для open telemetry

#### Системные требования
- [docker](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04-ru)
- [docker compose](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-22-04)

#### Как все работает
- Приложение отправляет телеметрию в коллектор
  - Чтобы работал коллектор надо его установить при помощи каоманды ниже
- Коллектор собирает данные и отправляет их в signoz
  - Нужно установить [signoz](https://signoz.io/docs/install/docker/#install-signoz-using-docker-compose) на сервер 


### Телеметрия на локальном сервере
Данные записываются в zipkin который работает на маршруте http://localhost:9411/zipkin/

**Для запуска:**
```shell
docker compose -f docker-compose-local.yaml up -d
```

---

### Телеметрия на боевом сервере
Данные записываются на сервер signoz

**Для запуска:**
```shell
docker compose up -d
```


