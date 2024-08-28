FROM python:3.12.5-slim AS builder

RUN set -eux; \
    \
    pip install -u pdm

ENV PDM_CHECK_UPDATE false

COPY pyproject.toml pdm.lock /project/
COPY src/ /project/src

WORKDIR /project

RUN set -eux; \
    \   
    pdm install --check --prod --no-editable

FROM python:3.12.5-slim

COPY --from=builder /project/.venv/ /project/.venv
ENV PATH="/project/.venv/bin:$PATH"

COPY src /project/src