# (dm)charts

This repository stores in its **gh-pages** branch  collection of publicly available Helm charts.

To use the charts from this repository you first need to add this to the list of your helm repositories. This is done by executing:

```bash
helm repo add dmcharts https://dmadunic.github.io/charts/
```

You can now use charts from this repository, for example to install *geodata demo app* execute the following command:

```bash
helm install geodata dmcharts/geodata
```

## Adding new chart to this repo

To add a new chart, for example `mychart-0.0.1.tgz`  perform the following steps (inside this repository folder):

```bash
git checkout gh-pages
cp {path_to_file}/mychart-0.0.1.tgz .
helm repo index helm-example/ --url https://dmadunic.github.io/charts/
git commit -a -m "Updated index with new chart: mychart-0.0.1.tgz"
$ git push origin
```

New chart should now be availabel for download.

---
(c) Domagoj Madunić 2022.
