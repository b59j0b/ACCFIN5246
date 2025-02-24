java c
Data   Science    Machine   Learning   in   Finance   (ACCFIN5246)
Course Project – Spring 2025


1         Instruction
(I)    Deadline:   4 March, noon.
(II)    This   course   project   counts   towards   (i) 35%   (via   quiz   format)   +   (ii) 50%   via   the   reflective report,   to the   overall course   grade.    This is   an individual   assessment.    Answer   all   ques-   tions. Both   submissions (i)-(ii)   to   be   made   electronically   via   the   course   Moodle   page. Each   part specifies further instructions.
(III)    Results should be reported in a clear   format.   Avoid   reporting   numbers   in   the   ‘scientific   format’   e.g.         7   .2031e-06.      All   reported   numbers   should   be   rounded   to   two   decimal   points. For   example, report   0.00 in   place   of   7   .2031e-06.
(IV)    The   grading   in   (i)   is   carried   out   strictly   based   on   the   precision   of   results   (with   minor   variational   tolerance).    The   reflective   component   (ii)   is   graded   according   to   the   clarity   of arguments, connectedness of the interpretations to the underlying quantitative frame-   work,   clarity   of   the   visualisations,   and   financial   implications.    The   final   part   is   graded   based on the relevance of finance analysis supported   by the methodologies and empirical   results.
2         Data: Acquisition and DescriptionAll   data series are to be   researched   thoroughly   to   ensure   consistency with   other   variables,   in   terms   economic   interpretations,   units,   frequency,   and   other   characteristics.    The   study   focus   time-span   is   2000-2023.      The   cleaned   dataset   should   be   arranged   in   both   daily   and   weekly frequencies   in   preparation   for   various   results   requested   in   Section   (3.2).
2.1         Dataset 1   (DS1)The   first   dataset   (DS1) is   provided   in   the   course   project, including   63 variables   and   summaris-   ingMSFT public stock transactions and market information. The data is acquired from WRDS-   CRSP universe.   DS1 only includes data entries —   with   the   data   description   and   data   dictio-   nary provided separately via   WRDS: Data Description Guide.   All computations and analyses   should explicitly take into account the instructions provided in the data description guide.The   dataset   provides   part   of   the   variables   needed   to   gather   descriptive   and   inferential   statis-   tics.   The   data   covers   2000-01-03 to   2023-12-29, on a daily basis.   The project set-up below refers to several variable (not all) included in the DS1,for example:
•   Calendar Date: Trading day (date)
•   Microsoft   stock   price   (PRC)


•   SP500 composite market index return (sprtrn)
•   Outstanding shares (Shrout)
•   Ask, Bid   Quotes   (ASK, BID)
•   Market   index   returns   data   on   a   value-weighted   market   portfolio   including   dividends   reinvested (variables   vwretd)   and   excluding   dividends (variable: vwretx). This   is   based   on   the   US   Total   Market   Index   produced by   the   CRSP   that   comprises   nearly   4,000   con-   stituents   across   mega, large, small   and   micro   capitalizations, representing   nearly   100% of the   U.S. investable   equity   market.
The dataset includes   additional variables. The course project will not require using those vari-   ables   where   there   are   no   entries   across   an   entire   column.
2.2         Risk-free Rate (DS2)
Interest   rates, associated   with   US   1-, 2-, and   10-year   maturity   treasuries.
2.3         US   CPI   (DS3)
The US consumer price index maybe used to transform. nominal data to real terms.
3         Data Preparation
3.1         Data   Cleaning   and   Arrangement
•   Construction of the financial dataset should takes into account the possibility of sporadic   observations.    When   multiple   series   of   disparate   frequencies   are   used   within   the   same   model, variable timestamps must be aligned.
•   The combined dataset including all variables alongside a common timeline may amount   to encountering missing values and   other irregularities.
•   The definition of (daily) log-return provides a measurement for value changes between   consecutive   observation   points   which   may   not   necessarily   be   adjacent   points   in   time   (days,   weeks,   etc.)    as   a   result   of   discarding   missing values   or   synchronising   an   unbal-   anced   set   of   observations.
•   Assume the following when required:
–   a ‘calendar   year’ comprises   exactly   52 weeks, this   may   amount   to   minor   discrepan-   cies   since, year   ≈ 52.17 weeks   – disregard   this   discrepancy.
–   a   trading   year   comprises   250 days, thus   disregard   any   variations   such   as   leap   years or public holidays affecting the number of trading days.


–   a   trading   month   is   25 days and a   trading   week   is   5 days, disregard   variations   beyond   these settings.
•   Weekly   log-returns   are   defined   as   the   percentage   value   change   between   a   week’s   first   trading day to next week’s first   trading day.
3.2         Main   Variables
Based   on   the   datasets   and   instructions   in   Sections   (2)-(3.1), construct   the   following   variables:
•   Construct   the   daily   MSFT   log-returns   (rt) using   the   price   (PRC) as   the   basis   variable.
•   Denote   the   simple   market   net   return   using   the   (sprtrn) as   (m,t).
•   Construct   log-returns   using   (m,t). Denote   the   market   log-return   as   (rm,t). You   may   need to   use   the   SP   index   value   at   2000-01-03 which   was   equal   to   1455.22.
•   Construct   the   net   risk-free   rate, using   DS2 (variable: DGS2) denoted   as   (rf,t)
•   Construct   daily   excess   MSFT   log-returns   儿rt   = rt   − rf
•   Construct   daily   excess   market   log-returns   儿rm,t   = rm,t   − rf.
•   Construct   the   net   inflation   rate,   using   DS3   (variable:      CPILFESL), by   applying   the   log-   return   method, and   denoted   by   πt.
At   this   stage, the   dataset   is   arranged   to   have   daily   observations:   {rt   ,   m,t,   rm,t,   rf,t,xrt,xrm,t,πt}also   extended   to   include   other   variables   provided   is   DS1 and   DS2. If   there   are   occasional   miss-   ing   values,   investigate   whether   these   are   due   to   coding   issues   (for   example,   πt    must   always   be   populated   at   all   days   in   the   dataset   above)   or   whether   there   has been   unreported   values   between   the   asset, market   and   the   riskfree   returns.
4         Objective Component (35%)Each question carries an equal代 写ACCFIN5246 Data Science & Machine Learning in Finance Spring 2025Python
代做程序编程语言   weight and according to the   University Objective Grading   Scale.   Provide   the   answers   to   the   following   questions   via   the   Objective   Component   Section   on   the   Course Moodle page.Note       For   all   of   the   questions   (Q1.-Q20.),   any   numerical   answer   must   be   rounded   to   the   closest two decimal points.    The computation is carried   out based   on   daily   frequency   and   for   whole sample timespan.
Q1   .   Average   stock   price   (as   recorded   by   the   PRC   variable).
Q2   .   Average   outstanding   shares   (as   recorded   by   the   SHROUT   variable).   Q3 .   Final   stock   price   on   2023-12-29 (as   recorded   by   the   PRC   variable).
Q4 .   Final   outstanding   shares   balance   on   2023-12-29 (as   recorded   by   the   SHROUT   variable).   Q5   .   Average   ask-bid   spread   (as   recorded   by   the   ASK−BID   variables).
Q6   .   Final   ask-bid   spread   (as   recorded   by   the   ASK−BID   variables) on   2023-12-29.
Q7   .   Construct   the   log-returns   based   on   the   PRC   variable, and   similarly,   percentage   changes   in the outstanding shares   (constructed following a similar   method   as   the   log-returns   of the prices).   Run a simple linear regression using OLS   where   the   outcome   variable   is the log-returns on the prices, on an intercept and an independent variable which is   the   percentage   change   of   the   outstanding   shares. Report   the   slope   coefficient.


Q8   .   Select   the   units   of   the   coefficient   reported   in   the   previous   part.   Q9   .   The   lowest   stock   price   value   in   the   whole   sample
Q10   .   The   highest   stock   price   value   in   the   whole   sample, occurred   in   which   year?   Enter   the year   value   only   (4 digits, e.g. 2000 without   any   month   or   day).
Q11   .   Construct   the   log-returns based   on   the   PRC   variable   on   the   original   frequency,   and   similarly, include the percentage changes in the SP market index (sprtrn, noting the   value under   this variable is   already in   percentage   changes).    Run   a   simple   linear   re-   gression   using   OLS   where   the   outcome   variable   is   the   log-returns   on   the   prices,   on   an   intercept   and   an   independent   variable   which   is   the   percentage   changes   in   the   SP   market index. Report the slope coefficient.
Q12   .   Construct   the   log-returns based   on   the   PRC   variable   on   the   original   frequency,   and   similarly, include the percentage changes in the SP market index (sprtrn, noting the   value under   this variable is   already in   percentage   changes).    Run   a   simple   linear   re-   gression   using   OLS   where   the   outcome   variable   is   the   log-returns   on   the   prices,   on   an intercept and two independent variables which are   the   percentage   changes   in   the   SP   market   index. Report   the   slope   coefficient, on   the   percentage   changes   in   the   SP   market index.
Q13   .   Construct   the   dividend-yield   (DP   ratio). Report   the   sum   of   DP   ratios.Compute the following financial returns. Assume an investment value of $1, invested in at the   start   of   2000-01-03 and   liquidated   on   2023-12-29. For   net   returns, this   should   be   computed   with two   decimals, for   example   20.75% is   0.2075   and   rounded   and   entered   as   0.21.
Q14   .   Total   nominal   net   return   associated   with   the   SP   market   index.
Q15   .   The   average   (annual) nominal   net   return   associated   with   the   SP   market   index   (ac-   count for compounding).
Q16   .   Nominal   net   return   associated   with   the   MSFT   stock.
Q17   .   Real   net   return   associated   with   the   SP   market   index.   Q18   .   Real   net   return   associated   with   the   MSFT   stock.
Q19   .   The   average   (annual) real   net   return   associated   with   with   theMSFT   stock   (account   for compounding).
Q20 .   Total   real   excess   net   return   for   the   MSFT   stock.
5         Reflective Component (50%)
1.   Investigate the ASK-BID variable   and comment   if   the behaviour   of   the   data   series   over   the full sample is reasonable. Do you observe any irregularities? Explain.
2.   Consider the model characterised by the following specification:xrt               =       αw   +   βwxrm,t   +   ut                                                                                                                                                                                                (1)
note   that   the   object   of   interest   is   the   time-varying   feature   of   the   coefficients   α-w   and   β-w. In particular, β-w   summarizes the conditional relationship, given a   rolling window incorpo-rating a consecutive but limited span of data, between the market   excess   log-return   and   an individual investment excess log-return.   The diagram below provides an illustration   to describe overlapping windows (w), including a calendar year of data:
Figure 1:   The timeline illustrates a rolling window set-up, where each iteration includes a consecutive 52 weekly   datapoints, where W1, W2, ...   refer to week numbers throughout the entire sample and wi   refer to   a rolling window   identifier.Focus on the abnormal returns^(α)w    as the outcome variable,   and   the   remaining variables   included in DS1-DS3. Provide a shrinkage and regularisation methodology to explain the   variations of the abnormal returns on the weekly frequency.
•   The   proposed   methodology   and   estimation   should   not   introduce   new data,   however   the existing variable maybe combined or transform. (lagged data is acceptable).
•   Provide a financial rationale why the variables are selected.
•   Provide a quantitative evaluation on how much the model set-up to predict the ab-   normal   returns   may   amount   to   increasing   the   financial   performance.    Benchmark   this   output   versus   the   value   in   Q.20 established   under   Section   (4).
6         Background Reading
•   Lecture slides
•   WRDS: Data Description Guide
•   SP   U.S. Indices   Methodology
•   Microsoft   Annual   Report   (2023)
•   Frank   A   Wolak.    An   exact   test   for   multiple   inequality   and   equality   constraints   in   the   linear   regression   model.      Journal   of   the   American   Statistical   Association,   82(399):   782–793,   1987
•   Chong Kiew Liew.   Inequality Constrained Least-Squares   Estimation.      Journal of the   American   Statistical Association,   71(355):746–751,   1976.    ISSN   01621459.    URL http:   //www.jstor.org/stable/2285614







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
