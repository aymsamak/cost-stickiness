Cost Stickiness Measure (1970–2025)

This repository provides firm-level quarterly and annual cost stickiness measures for U.S. listed firms from 1970 to 2025. The data are constructed following the methodology of Anderson, Banker, and Janakiraman (2003) and subsequent studies on asymmetric cost behavior.

Overview
Cost stickiness refers to the asymmetric adjustment of operating costs with respect to changes in sales (Anderson et al., 2003). Firms with higher cost stickiness exhibit limited operational flexibility—often due to rigid resource commitments such as labor contracts, asset specificity, or internal frictions (Banker et al., 2013; Chen et al., 2012). These constraints heighten firms’ vulnerability to external shocks and may amplify strategic responses.

Following the literature, we construct a firm-quarter measure of cost stickiness and aggregate it to the firm-year level. The final dataset includes two files:

Quarterly.dta — firm-quarter level stickiness (available upon request due to file size limits)
annual.dta — firm-year level stickiness (annualized version of quarterly values)

Methodology
The construction follows the approach of Anderson et al. (2003), Kama and Weiss (2013), and Subramaniam and Watson (2016).

For each firm i and time period t:

Stickiness(i,t) = ln((ΔCost(i,t)^down / ΔSales(i,t)^down)) – ln((ΔCost(i,t)^up / ΔSales(i,t)^up))

Where:
ΔSales(i,t) = Sales(i,t) – Sales(i,t–1)
ΔCost(i,t) = (Sales(i,t) – Income Before Extraordinary Items(i,t)) – (Sales(i,t–1) – Income Before Extraordinary Items(i,t–1))

We identify quarters where sales increased (up) and decreased (down) separately. The difference between log-cost changes in down and up quarters defines Stickiness.

Data Files
Quarterly.dta
Variables:

gvkey: firm identifier (Compustat)
datadate: quarter end date
fyearq: fiscal year (quarterly version)
fqtr: fiscal quarter (1–4)
quarter: Stata quarterly time variable
stickiness: Difference between cost decrease and increase responses

Note: Due to GitHub file size limitations, the full quarterly dataset is not included in this repository. Researchers may request access by contacting the author.

annual.dta
Variables:

gvkey: firm identifier
fyear: fiscal year
stickiness: firm-year cost stickiness


Brief Construction Method:

Load and clean quarterly Compustat data.
Compute changes in sales and operating costs.
Calculate log(ΔCost/ΔSales) for quarters with sales up vs. down.
Derive the STICKY variable and aggregate to annual level.

Citation
If you use this dataset, please cite both the underlying literature and this repository:

Base methodology:

Anderson, M. C., Banker, R. D., & Janakiraman, S. N. (2003). Are selling, general, and administrative costs “sticky”? Journal of Accounting Research, 41(1), 47–63.
Banker, R. D., Byzalov, D., & Chen, L. T. (2013). Employment protection legislation, adjustment costs, and cross-country differences in cost behavior. Journal of Accounting and Economics, 55(1), 111–127.
Chen, C. X., Lu, H., & Sougiannis, T. (2012). The agency problem, corporate governance, and the asymmetrical behavior of selling, general, and administrative costs. Contemporary Accounting Research, 29(1), 252–282.
Kama, I., & Weiss, D. (2013). Do earnings targets and managerial incentives affect sticky costs? Journal of Accounting Research, 51(1), 201–224.
Subramaniam, C., & Watson, M. (2016). Additional evidence on the sticky behavior of costs. Management Accounting Research, 31, 40–58.

Repository citation (example):
Samak, Ayman (2025). Cost Stickiness Measure (1970–2025): Quarterly and Annual Datasets. GitHub repository, https://github.com/aymsamak/cost-stickiness

License

Code: Released under the MIT License.

Data: Released under the Creative Commons Attribution 4.0 International (CC BY 4.0) license.
You are free to use, share, and adapt the data and code with appropriate attribution.

Contact
For questions, data requests (including access to the quarterly dataset), or collaboration inquiries:
Ayman Samak
Texas A&M International University
Email: aymansamak@dusty.tamiu.edu
