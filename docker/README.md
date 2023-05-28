# invoke-ai

InvokeAI

---

## Podman

```bash

podman build \
    -f docker/Dockerfile.podman \
    -t gabr1elt/invoke-ai

podman run \
    --rm \
    -it \
    # use gpu (CDI)
    --device nvidia.com/gpu=all \
    # forward ports for 'openvscode-server'
    # -p 127.0.0.1:3000:3000 \
    # -v "${HOME}/Development/diffusers:/root/Development:cached" \
    -h "invoke-ai" \
    gabr1elt/invoke-ai
    # gabr1elt/invoke-ai /bin/bash

```
