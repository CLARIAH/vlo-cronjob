# cronjob to harvest endpoints

Run the mail script to harvest nde and oai endpoints
```shell
./main.sh
```

This is the main repo to run the pipeline of CLARIAH. The pipeline consists of the following steps:
1. Harvesting endpoints both NDE and OAI
2. Ingesting the harvested datasets (Needs [VLO](https://vlo.datasets.dev.clariah.nl/?0) and it's repo is [here](https://github.com/CLARIAH/datasets-vlo/))
3. Labeling and RAIR-assess the datasets (Need [INEO Labeling](https://github.com/CLARIAH/vlo-cronjob-labeling) and [pyFAT](https://github.com/CLARIAH/pyFAT/tree/develop), they are built into one docker image)
   1. Labeling datasets as INEO records (`true` or `false`) in [VLO](https://vlo.datasets.dev.clariah.nl/?0)
   2. RAIR-assess the datasets and show the resuilt in [VLO](https://vlo.datasets.dev.clariah.nl/?0)
   3. The assessment reports are store in ttl folder on [VLO](https://vlo.datasets.dev.clariah.nl/?0)
4. Sync the datasets to INEO (Needs [INEO Sync](https://github.com/CLARIAH/ineo-collaboration/tree/main))
5. 

