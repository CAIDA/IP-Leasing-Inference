# Infer Leased IP Prefixes

This repo contains the analysis code for the IMC 2024 paper Sublet Your Subnet: Inferring IP Leasing in the Wild.

## Results from paper

The 5 files named `leases_[RIR]_20240401.json.gz` contain the 47,318 inferred leased prefixes described in the paper. The prefixes were also annotated with RIR metadata and necesarry information to infer their lease (e.g. BGP origins as depicted in Figure 2 in the paper).

## Curated reference datasets

- The leased prefixes reference dataset (positive labels) needs to be generated using the most up-to-date datasets. The registered brokers are listed in `recognized_brokers_[RIR].txt`
- The non-leased prefixes reference dataset is included in the files named `non_lease_[ISP]_pfx.csv`. They are relatively stable compared to leased prefixes.

## Data Requirement

To run the code, you need to download the following CAIDA datasets:

- [CAIDA AS Relationship dataset](https://www.caida.org/catalog/datasets/as-relationships/)
- [CAIDA AS Organizations dataset](https://www.caida.org/catalog/datasets/as-organizations/)
- [CAIDA Routeviews Prefix2AS dataset](https://www.caida.org/catalog/datasets/routeviews-prefix2as/)

and RIR WHOIS database:

- [RIPE](https://ftp.ripe.net/ripe/dbase/) (public)
- [AFRINIC](https://ftp.afrinic.net/dbase/) (public)

- [ARIN](https://www.arin.net/reference/research/bulkwhois/) (need to sign AUP)
- [APNIC](https://www.apnic.net/manage-ip/using-whois/bulk-access/) (need to sign AUP)
- [LACNIC](https://www.lacnic.net/2472/2/lacnic/accessing-bulk-whois) (need to sign AUP)