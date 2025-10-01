## Avvio dei servizi con Docker Compose

Questa repository contiene un ambiente di laboratorio per testare vulnerabilità OWASP tramite Docker Compose.

### Prerequisiti
- Docker installato sul sistema
- Docker Compose installato (o `docker compose` integrato in Docker)

### Avvio dei servizi
Per avviare tutti i servizi definiti nel file `docker-compose.yaml`, esegui il seguente comando dalla root del progetto:

```bash
docker compose up -d
```

Questo comando avvierà i seguenti laboratori:
I servizi disponibili sono:

- **idor**: laboratorio OWASP IDOR, accessibile su [http://127.0.0.1:7000](http://127.0.0.1:7000) guida in [idor.md](idor.md)
- **sqli**: laboratorio OWASP SQL Injection, accessibile su [http://127.0.0.1:7001](http://127.0.0.1:7001) guida in [sqli.md](sqli.md)
- **xss**: laboratorio OWASP XSS, accessibile su [http://127.0.0.1:7002](http://127.0.0.1:7002) guida in [xss.md](xss.md)
- **ssrf**: laboratorio OWASP SSRF, accessibile su [http://127.0.0.1:7003](http://127.0.0.1:7003) guida in [ssrf.md](ssrf.md)
- **cmdi**: laboratorio OWASP Command Injection, accessibile su [http://127.0.0.1:7004](http://127.0.0.1:7004) guida in [cmdi.md](cmdi.md)

### Spegnimento dei servizi
Per fermare e rimuovere i container:

```bash
docker compose down
```

### Note
- I servizi sono esposti solo su localhost per motivi di sicurezza.
- Alcuni servizi interni non sono esposti direttamente all'host per motivi didattici (esempio per ssrf).

Per ulteriori dettagli consulta il file `docker-compose.yaml`.
