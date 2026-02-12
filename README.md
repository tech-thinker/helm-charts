# Services
Installation guide of service.

## Helm:
1. Add Helm Repository:
    ```sh
    helm repo add <repository-name> <repository-url>
    # or private git repository
    # helm repo add tech-thinker https://tech-thinker.github.io/helm-charts
    
    helm repo update
    ```

2. Inspect the values of chart.
    ```sh
    helm show values <chart-name>
    # If you want to save the values to yaml file, use:
    helm show values <chart-name> > values.yaml
    ```

3. App Installation:
    ```sh
    helm install <release-name>  <chart-name>  -n <namespace> -f values.yaml
    ```

4. List of Installed App:
    ```sh
    helm list -n <namespace>
    ```

5. Uninstall App:
    ```sh
    helm uninstall <release-name> -n <namespace>
    ```

6. Upgrade App:
    ```sh
    helm upgrade <release-name> <chart-name> -n <namespace> -f values.yaml
    ```

7. Rollback App:
    ```sh
    helm rollback <release-name> <revision> -n <namespace>
    ```

8. Create Helm Chart:
    ```sh
    helm create <chart-name>
    ```

9. Package Helm Chart:
    ```sh
    helm package <chart-name>
    ```

10. Publish Helm Chart:
    ```sh
    helm push <chart-name>-<version>.tgz <repository>
    ```
