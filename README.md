Who Feels Threatened by AI?
GDP per capita, internet use, and how developers in 65 countries view AI

This BA780 Team B04 project examines how developers use and trust AI, and whether they see it as a threat to their jobs. It focuses on country-level GDP and internet use, while also comparing views across developer groups.
Main question
What shapes how developers see AI?

We look at two related but different ideas: how developers use and trust AI, and how secure they feel about their jobs as AI becomes more common.
Data
We started with the 2025 Stack Overflow Developer Survey, which had 49,191 responses. After keeping professional developers with complete answers, the project had 23,605 records. For country comparisons, we kept countries with at least 30 respondents, leaving 22,753 developers across 65 countries.
Source	Data used
Stack Overflow Developer Survey 2025	Developer role, AI use, trust in AI accuracy, job-threat responses, age, and coding experience
World Bank: GDP per capita	2025 GDP per capita
World Bank: Individuals using the internet	2024 internet-use rate, as a share of the population


The World Bank internet-use data is from 2024 because 2025 data was missing for most countries. We matched country names to World Bank country codes before joining the data.
Analysis process
1. Selected the survey fields needed for the project and kept professional developers.
2. Cleaned the data and matched countries across the survey and World Bank files.
3. Calculated percentages for AI use, AI trust, and job-threat responses.
4. Compared countries by GDP and internet-use groups, and compared developers by age and job role.
5. Used Pearson correlations to examine country-level relationships. We also used chi-square tests and Cramér’s V for categorical comparisons.
6. Used an OpenAI API model to assign an exploratory job-concern score from 1 to 10 based on five AI-related survey answers. We compared these scores with respondents’ answers to the direct job-threat question.
Valid response counts differ by question because not every developer answered every survey item. For Yes/No job-threat percentages, “I’m not sure” was excluded. The LLM score kept uncertain responses near the middle of its scale.
Main findings
- Developers in lower-income countries reported more AI use, trust, and job concern. Daily AI use was 70.6% in the lowest GDP quarter and 47.5% in the highest. The share saying AI threatens their job was 17.0% in the lowest quarter and 11.4% in the highest. Trust in AI accuracy was 77.2% in the poorest fifth of countries and 33.7% in the richest fifth.
- Trust and job concern can occur together. Among developers who highly trusted AI accuracy, 36.0% said AI was a threat to their job. The share was 12.2% among those who highly distrusted AI accuracy.
- Age patterns differ for trust and job concern. The average AI trust score rose from 3.93 among developers aged 18–24 to 4.70 among those aged 65 or older. Job-threat perception was highest at 19.5% among developers aged 45–54 and lowest at 10.9% among those aged 65 or older.
- Internet use alone does not explain job-threat views. Across 65 countries, internet use and job-threat perception had a weak negative correlation (r = -0.32). The relationship was not consistent within GDP groups. In the upper-middle GDP group, the correlation changed from r = 0.39 to r = -0.14 when South Korea was excluded.
- Concern also varied by job role. Mobile and front-end developers reported the highest job-threat shares in the role comparison, at 25.8% and 24.1%.

Why this matters
Employers can use these results to start conversations about AI training and career support, especially in roles or groups where concern was higher. They should ask employees what support they need instead of assuming that everyone of a certain age or role feels the same way.

AI companies can explain how accurate their tools are, where they have limits, and how they may change work. Trust in AI and concern about job security should be addressed as separate issues.

Policymakers and educators can consider local job markets, developer roles, and AI adoption when planning workforce programs. Internet access by itself is not a reliable guide to developers’ concerns.

Limitations
- The results show associations, not cause and effect.
- Stack Overflow respondents may not represent all developers.
- Country averages cannot describe every developer in a country.
- Countries had different sample sizes, and some results were sensitive to one country.
- The survey and internet-use data come from different years.
- The LLM score is exploratory. It is not an independently validated measure or ground truth.

Reproducing the analysis
The notebooks use Python and packages such as pandas, NumPy, Matplotlib, and Seaborn. Download the source data from the links above, confirm that you have access to the files used by the notebooks, and run the notebook cells from top to bottom. Update file paths if your data files are stored elsewhere.

Team B04
- Steven Nguyen
- Ilya Barymov
- Yi-Chen Hsu (YC)
- Muhammad Rafi
