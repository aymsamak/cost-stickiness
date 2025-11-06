Title & Description:

Cost Stickiness Measure (1970–2025)
Quarterly and annual firm-level cost stickiness measures following Anderson et al. (2003), Kama & Weiss (2013), and Subramaniam & Watson (2016).

Citation:

Anderson, M., Banker, R., & Janakiraman, S. (2003). Are selling, general, and administrative costs "sticky"? Journal of Accounting Research, 41(1), 47–63.
Banker, R., Byzalov, D., & Chen, L. (2013). Employment protection legislation, adjustment costs, and cross-country differences in cost behavior. Journal of Accounting and Economics, 55(1), 111–127.
Chen, C. X., Lu, H., & Sougiannis, T. (2012). The agency problem, corporate governance, and the asymmetrical behavior of selling, general, and administrative costs. Contemporary Accounting Research, 29(1), 252–282.
Kama, I., & Weiss, D. (2013). Do earnings targets and managerial incentives affect sticky costs? Journal of Accounting Research, 51(1), 201–224.
Subramaniam, C., & Watson, M. (2016). Additional evidence on the sticky behavior of costs. Management Accounting Research, 31, 40–58.

Variable Description:

gvkey: firm identifier
quarter: Stata quarterly time variable
fyear, fqtr: fiscal year and quarter
stickiness difference between cost decrease and increase responses

Brief Construction Method:

Compute quarterly changes in sales and costs.
Calculate log(ΔCostΔSales) for sales up and down quarters.
Subtract the two to obtain stickiness.
Aggregate to the annual level.