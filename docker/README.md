# invoke-ai

InvokeAI

---

## Podman

```bash

podman build \
    . \
    -f docker/Dockerfile.podman \
    -t gabr1elt/invoke-ai

podman run \
    --rm \
    -it \
    # use gpu (CDI)
    --device nvidia.com/gpu=all \
    -p 127.0.0.1:9090:9090 \
    # -v "${HOME}/Development/diffusers:/root/Development:cached" \
    -h "invoke-ai" \
    gabr1elt/invoke-ai
    # gabr1elt/invoke-ai /bin/bash

podman run \
    --rm \
    -it \
    --device nvidia.com/gpu=all \
    -p 127.0.0.1:9090:9090 \
    -h "invoke-ai" \
    gabr1elt/invoke-ai

```
