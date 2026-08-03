-**Capstone Report **

-**Author:** Harshitha Vandavasi

-**Lane:** Machine Learning

-**Repo:** https://github.com/harshithavandavasi-1401/HV-flyrank-ml-internship

-**Date:** July 2026

Copy this file to work/capstone_report.md and fill it in as you build. Sections 1–8 mirror the Pass / Needs-Work rubric axes, so nothing here is optional. Sections 0 and 9 are paper sections: your deployed research paper must carry both, and they're here so you never rebuild them from memory at ship time.

##0.Abstract**

This project investigates which web pages should be prioritized for content refresh using search performance signals. The analysis was conducted on the FlyRank ML Internship dataset containing approximately 30,000 web pages and multiple SEO-related features. A supervised machine learning model was trained and evaluated using an honest validation strategy to rank pages according to their refresh priority. The model produced better ranking performance than a simple baseline and generated interpretable recommendations for editors. The resulting ranked action list is intended to support editorial decision-making and should be reviewed by humans before implementation.

##1. Problem framing**

The objective of this project is to help content teams identify which web pages should be refreshed first to improve search performance. Each row in the dataset represents a single web page. The model produces a ranked recommendation rather than making automatic decisions. Editors can use these rankings to prioritize their content update efforts. Incorrect recommendations may cause high-value pages to be overlooked or unnecessary work to be performed, so human review remains an important part of the workflow.

##2.Data

This project uses the FlyRank ML Internship dataset containing approximately 30,000 web pages represented by 44 search-engine optimization features. Each row corresponds to one web page and includes information such as search volume, competition, CPC, content type, search intent, word count, readability measures, keyword statistics, and engagement-related metrics.

Only publicly safe features were used during modeling. Client-identifying information and other non-generalizable attributes were excluded from the final analysis. Missing values were handled before training, and duplicate records were removed where necessary.

The dataset was split using an honest validation strategy to reduce optimistic estimates and better simulate future prediction performance.
Only publicly safe features were used during modeling. Client-identifying information and other non-generalizable attributes were excluded from the final analysis. Missing values were handled before training, and duplicate records were removed where necessary.

The dataset was split using an honest validation strategy to reduce optimistic estimates and better simulate future prediction performance.

##3.Baseline

A simple baseline model was created before training the machine learning model. The baseline provides a transparent reference for comparison and demonstrates how much additional value the trained model contributes.

The machine learning model was evaluated using the same validation split as the baseline, ensuring a fair comparison between both approaches.

##4.Model / Analysis

A supervised machine learning model was trained to rank web pages according to their refresh priority. Multiple SEO-related numerical and categorical features were used as input.

Feature engineering, preprocessing, and validation were completed before model training. Leakage-sensitive columns were removed, and an honest validation strategy was used to evaluate generalization performance.

The objective of the model is not to replace editorial decisions but to provide a ranked list that helps editors identify pages likely to benefit from content refresh.

##5.Evaluation

The model was evaluated using an honest validation split instead of relying only on random train-test splitting. This reduces the risk of overly optimistic performance estimates.

Model performance was compared directly against the baseline using the same validation data. The evaluation indicates that the trained model provides improved ranking performance while maintaining more realistic estimates through leakage-aware validation.

Error analysis suggests that some pages remain difficult to classify because multiple SEO factors interact and content quality cannot always be captured by numerical features alone.

##6.Interpretation

The analysis indicates that search volume, keyword-related metrics, competition, readability, and content characteristics contribute to refresh priority decisions.

Rather than making automatic decisions, the model produces directional recommendations that help editors prioritize work. The output should be interpreted as decision support rather than a guarantee that updating a page will improve search performance.

The feature importance analysis improves transparency by showing which inputs most influence the ranking process.

##7.Recommendation

Editors should begin by reviewing the highest-ranked pages identified by the model. These pages are more likely to benefit from content updates based on the observed search performance signals.

Recommended workflow:

1. Review the highest-priority pages.
2. Verify recommendations through manual inspection.
3. Update outdated or incomplete content.
4. Monitor search performance after publication.
5. Retrain the model periodically using newly collected data.

The recommendations are intended to support editorial planning and should always be reviewed by humans before implementation.

##8.Reproducibility

The complete project is available in the GitHub repository.

The repository contains:

- Data preprocessing notebooks
- Feature engineering notebooks
- Model training notebooks
- Validation notebooks
- Action playbook notebook
- Capstone notebook
- Generated figures
- Exported metrics
- Documentation

Random seeds were fixed where applicable to improve reproducibility. The notebooks can be executed from top to bottom to regenerate the reported outputs.

##9.Acknowledgements & Data Credit

This work was completed as part of the FlyRank Machine Learning Internship.

Built on the FlyRank ML Internship dataset.

Data credit:
https://flyrank.ai

The project uses publicly safe outputs for educational and research purposes. All reported results follow honest validation practices and avoid client-identifying information.
