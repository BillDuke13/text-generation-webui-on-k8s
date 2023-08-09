# text-generation-webui-on-k8s
text generation webui on k8s

## Prerequisites

- Nvidia GPU

- Default StorageClass

- [Helm CLI](https://github.com/helm/helm)


## Setup

1. **Container Image Building**
   Start by cloning the [text-generation-webui](https://github.com/oobabooga/text-generation-webui) repository and navigate to the Docker folder. Build your Docker image by replacing 'YOUR_IMAGE_NAME' with the Docker image name you prefer.

   ```bash
   git clone https://github.com/oobabooga/text-generation-webui
   cd text-generation-webui/docker
   docker build -t YOUR_IMAGE_NAME .
   ```

2. **Modifying the Helm value file**

   You'll have to adjust your Helm value file, particularly the image name.

3. **Installing the Helm Chart**

   Install the chart into your desired namespace (replace 'NAMESPACE' with your desired namespace)

    ```bash
    helm install -n NAMESPACE text-generation-webui-on-k8s ./text-generation-webui-on-k8s
    ```


## References

[text-generation-webui](https://github.com/oobabooga/text-generation-webui)