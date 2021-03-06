# crm_service

## Development

Build the image:

```bash
docker-compose build
```

Run the web server:

```bash
docker-compose up
```

Open your browser with URL `http://localhost:8002`.
For the admin panel `http://localhost:8002/admin`
(user: `admin`, password: `admin`).

Run the tests only once:

```bash
docker-compose run --rm --entrypoint 'bash scripts/run-tests.sh' crm_service
```

Run the tests and leave bash open inside the container, so it's possible to
re-run the tests faster again using `bash scripts/run-tests.sh [--keepdb]`:

```bash
docker-compose run --rm --entrypoint 'bash scripts/run-tests.sh --bash-on-finish' crm_service
```

To run bash:

```bash
docker-compose run --rm --entrypoint 'bash' crm_service
```
