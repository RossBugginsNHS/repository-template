# Publishing

To publish, create classic and docker login before `make publish`

Docker login:

```bash
export CR_PAT=YOUR_TOKEN
echo $CR_PAT | docker login ghcr.io -u USERNAME --password-stdin
```
