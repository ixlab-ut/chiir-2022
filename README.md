# COVID-19 claims dataset for CHIIR 2022 Paper


This repository contains the data for the paper **The Effects of Interactive AI Design on User Behavior: An Eye-tracking Study of Fact-checking COVID-19 Claims** published at the [ACM CHIIR 2022](https://ai.ur.de/chiir2022/program/papers) conference.

- DOI: https://doi.org/10.1145/3498366.3505786
- arXiv: https://arxiv.org/pdf/2202.08901.pdf


## Demo
The mock AI fact-checking system used in the study can be accessed by clicking the link below.
- [Link to mock AI fact-checking system](https://volt.ischool.utexas.edu/viz/fcweb_ui_demo.php)



## Teaser Video for CHIIR 2022

[![YouTube Video: CHIIR'22 Poster Boaster Video](https://img.youtube.com/vi/aic030YwiLA/0.jpg)](https://www.youtube.com/watch?v=aic030YwiLA)




## Structure of the Repository

### `claims.csv`
Contains 24 claims related to the COVID-19 pandemic used in the eye-tracking user study.
- **claim_id**: unique ID for a claim
- **claim_correctness**: whether the claim is `TRUE`, `FALSE`, or `UNSURE`; as determined using the methodology described in the paper in Section 2.2
- **claim_txt**: the text of the claim

### `news.csv`
Contains metadata about 120 news articles, with 5 news articles per claim.
- **claim_id**: coming from `claims.csv`, the claim to which this news article corresponds to
- **news_source**: source of the news outlet (domain name of the website)
- **news_source_reputation**: reputation of the news outlet, ranging between -1 (low) to +1 (high); as determined using the methodology described in the paper in Section 2.2
- **news_headline**: title of the news article 
- **news_stance**: stance of the news article towards the claim, ranging from -1 (deny), to 0 (neutral), to +1 (support); as determined using the methodology described in the paper in Section 2.2
- **news_url**: URL of the news article, as collected during April-May 2021



### `screenshots` folder
Contains 48 screenshots of the 24 claims presented via two user interfaces (UIs). The filename structure for each file is
`<UI>_<claim_id>.png`, 
with `claim_id` coming from `claims.csv`.
UI A is interactive, with sliders to tweak model parameters, while UI B is non-interactive.






## Citation
If you use any part of our work, please cite us as
```
@inproceedings{shi2022effects,
  title={The Effects of Interactive AI Design on User Behavior: An Eye-tracking Study of Fact-checking COVID-19 Claims},
  author={Shi, Li and Bhattacharya, Nilavra and Das, Anubrata and Lease, Matthew and Gwizdka, Jacek},
  booktitle={Proceedings of the ACM SIGIR Conference on Human Information Interaction and Retrieval},
  year={2022},
  doi={10.1145/3498366.3505786},
  series={CHIIR '22}
}
```

## Acknowledgement
We thank the reviewers for their valuable feedback, and the research participants for their time. This research was completed under UT Austin IRB study 2017070049 and supported in part by Wipro, the Micron Foundation, the Knight Foundation, and by Good Systems (http://goodsystems.utexas.edu), a UT Austin Grand Challenge to develop responsible AI technologies. The statements made herein are solely the opinions of the authors and do not reflect the views of the sponsoring agencies.
