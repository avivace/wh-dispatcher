# wh-dispatcher

Install the dependencies locally:

```bash
poetry install
poetry run uvicorn src.main:app --reload --env-file secrets.txt
```
Or run it with docker:

```bash
docker build -t wh-dispatcher .
docker run -it wh-dispatcher
```

### Tests

Run tests:

```bash
poetry run pytest
```

### Playing around

To mimick an arriving payload:

```bash
curl -X 'POST' \
  'http://http://0.0.0.0:8000/webhook/1' \
  -d '{"42": "your_json_data_should_go_here"}'
```
