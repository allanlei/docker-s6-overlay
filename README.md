# docker-s6-overlay

## Usage
### Usage 1 - Primary process with supporting process

- If the **primary** process exits, the container exits.
- If a **supporting** process exits, the supporting process is restarted.

```
services.d/
  support1/
    run
```

* `services.d/support1/run`

  ```
  #!/usr/bin/with-contenv sh
  SUPPORT COMMAND
  ```

`docker run -v services.d:/etc/services.d allanelei/s6-overlay PRIMARY_COMMAND`
