# Manual Judgment Reader
> Custom job stage for spinnaker

Run a pipeline and read the manual judgment to cancel the pipeline if a rollout occurs.

### How install

- Add the manual judgment reader dic to patchesStrategicMerge in your kustomization.yaml
- In the manual-judgment-reader.yaml change:
  - application: application-name # Application name (Change this)
  - namespace: namespace-name # Configure the namespace (Change this)
  - image: dwdraju/alpine-curl-jq # Image with CURL and JQ (OPTIONAL)
- Apply changes in kustomization and restart the UI

Important use ignore the failure if the stage fails in the pipeline step configuration.

---

## Authors
* **Carlos Catalán** - [Github](https://github.com/carloscatalanl)  - [Gitlab](https://gitlab.com/carloscatalanl) 