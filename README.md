# PRS model for hypertensive disorders in pregnancy
#### hdp-prs-finngen-r8

Jung, S. H., Kim, H., Jung, Y. M., Shivakumar, M., …, Kim, D. & Lee, S.M. (2024) Long-term cardiovascular risk according to lifestyle, metabolic health, and genetic risk of hypertensive disease during pregnancy.

### Hypertensive disorders of pregnancy - ??? variants
> [FinnGen_r8_PRSCS_auto.gz](https://github.com/dokyoonkimlab/hnc-prs-phewas/blob/main/prs-model/FinnGen_r8_PRSCS_auto.gz)

---

## Description

To generate polygenic risk score (PRS), we utilized the hypertensive disorders of pregnancy (HDP) genome-wide association study (GWAS) summary statistics from the FinnGen Consortium (Data Freeze R8v4) which is a large-scale public-private partnership combining digital health record data from Finnish health registries with genotyping data from Finnish Biobanks [1]. FinnGen Release 8 (https://www.finngen.fi/en) includes association data at 20,175,454 variants for 2,202 endpoints in 342,499 (190,879 females and 151,620 males) Finnish individuals. The HDP cases (O15_HYPTENSPREG) were identified based on ICD codes (ICD-8: 63701, 63703, 63704, 63709, 63710, 63799, and 66120; ICD-9: 642; ICD-10: O10, O11, O13, O14, O15, and O16). There were 13,071 cases and 177,808 controls following FinnGen phenotype definition. GWAS was performed by FinnGen using SAIGE with sex, age, 10 PCs, and genotyping batch as covariates [2]. In addition, we mapped FinnGen summary statistics from GRCh38 to GRCh37/hg19 using the liftOver tool to perform PRS with UK Biobank genotyped data (GRCh37/hg19) [3].

We constructed PRS for HDP by using a Bayesian polygenic prediction method, PRS-CS [4], which infers the posterior mean effect size of each variant using the linkage disequilibrium (LD) reference panel and GWAS summary. The 1000 Genome Project phase 3 EUR data was used to be the external LD reference panel. The posterior SNP effect sizes in PRS-CS were inferred from GWAS summary statistics for EUR (FinnGen r8) population. The individual PRSs were computed from beta coefficients as the weighted sum of the risk alleles by applying PLINK version 1.90 with the –score command [5].

### References
1.	Kurki, Mitja I., et al. "FinnGen provides genetic insights from a well-phenotyped isolated population." Nature 613.7944 (2023): 508-518.
2.	Zhou, Wei, et al. "Efficiently controlling for case-control imbalance and sample relatedness in large-scale genetic association studies." Nature genetics 50.9 (2018): 1335-1341.
3.	Nassar, Luis R., et al. "The UCSC genome browser database: 2023 update." Nucleic acids research 51.D1 (2023): D1188-D1195.
4.	Ge, Tian, et al. "Polygenic prediction via Bayesian regression and continuous shrinkage priors." Nature communications 10.1 (2019): 1776.
5.	Chang, Christopher C., et al. "Second-generation PLINK: rising to the challenge of larger and richer datasets." Gigascience 4.1 (2015): s13742-015.

