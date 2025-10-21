# Laboratorio XSS

Questo laboratorio permette di testare vulnerabilità di tipo Cross-Site Scripting (XSS) tramite esempi pratici.

## Come usare il laboratorio

1. Avvia il servizio XSS tramite Docker Compose come indicato nel README principale.
2. Prova gli esempi nei campi di input dell'applicazione XSS.
3. Osserva il comportamento dell'applicazione per capire se è vulnerabile.

### 1. Navigazione iniziale
Accedi all'applicazione all'indirizzo [http://localhost:7002](http://localhost:7002).


### 2. Test di escaping
Utilizza questa stringa per verificare se i caratteri speciali vengono correttamente gestiti dall'applicazione:

```
ciao >< "pippo" :// 'pippo' &=
```

### 3. Payload XSS 1
Un esempio di payload che può essere usato per testare la vulnerabilità XSS:

```
XSS!<script>alert('XSS')</script>
```

### 4. Payload XSS 2
Un esempio di link che può essere utilizzato per indurre l'utente a cliccare e sfruttare una vulnerabilità XSS:

```
<a href="http://localhost:7000/">Clicca qui e ottieni 50% di sconto</a>
```