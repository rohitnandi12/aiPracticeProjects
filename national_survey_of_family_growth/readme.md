This repo is initiated from the book **ThinkStats** written by AllenDowney.
Learn more about the book at https://greenteapress.com/wp/think-stats-2e/

The book use the below dataset

### Dataset Description

The National Survey of Family Growth (NSFG), conducted by the U.S. Centers for Disease Control and Prevention (CDC) to gather information on family life, marriage and divorce, pregnancy, infertility, use of contraception, and men’s and women’s health." (See
http://cdc.gov/nchs/nsfg.htm.)


The National Survey of Family Growth
Since 1973 the U.S. Centers for Disease Control and Prevention (CDC)
have conducted the National Survey of Family Growth (NSFG), which is
intended to gather \information on family life, marriage and divorce, pregnancy, infertility, use of contraception, and men’s and women’s health. The
survey results are used . . . to plan health services and health education programs, and to do statistical studies of families, fertility, and health." See
http://cdc.gov/nchs/nsfg.htm.


We will use data collected by this survey to investigate whether first babies
tend to come late, and other questions. In order to use this data effectively,
we have to understand the design of the study.

The NSFG is a **cross-sectional study**, which means that it captures a snapshot of a group at a point in time. The most common alternative is a **longitudinal study**,
which observes a group repeatedly over a period of time.
The NSFG has been conducted seven times; each deployment is called a
**cycle**. We will use data from **Cycle 6**, which was **conducted from January
2002 to March 2003.**
The goal of the survey is to draw conclusions about a population; the
target population of the NSFG is people in the United States aged 15-44.
Ideally surveys would collect data from every member of the population,
but that’s seldom possible. Instead we collect data from a subset of thepopulation called a sample. The people who participate in a survey are
called respondents.

In general, cross-sectional studies are meant to be representative, which
means that every member of the target population has an equal chance of
participating. That ideal is hard to achieve in practice, but people who
conduct surveys come as close as they can.

The NSFG is not representative; instead it is deliberately oversampled. The
designers of the study recruited three groups|Hispanics, African-Americans
and teenagers|at rates higher than their representation in the U.S. population, in order to make sure that the number of respondents in each of these
groups is large enough to draw valid statistical inferences.
Of course, the drawback of oversampling is that it is not as easy to draw
conclusions about the general population based on statistics from the survey.
We will come back to this point later.

When working with this kind of data, it is important to be familiar with
the codebook, which documents the design of the study, the survey questions, and the encoding of the responses. The codebook and user’s guide for
the NSFG data are available from http://www.cdc.gov/nchs/nsfg/nsfg_
cycle6.htm


There are 244 variables in total but only the following variables are used: 

- **caseid** is the integer ID of the respondent
- **prglngth** is the integer duration of the pregnancy in weeks.
- **outcome** is an integer code for the outcome of the pregnancy. The code 1 indicates a live birth.
- **pregordr** is a pregnancy serial number; for example, the code for a respondent’s first pregnancy is 1, for the second pregnancy is 2, and so on.
- **birthord** is a serial number for live births; the code for a respondent’s first child is 1, and so on. For outcomes other than live birth, this field is blank.
- **birthwgt_lb** and **birthwgt_oz** contain the pounds and ounces parts of the birth weight of the baby.
- **agepreg** is the mother’s age at the end of the pregnancy.
- **finalwgt** is the statistical weight associated with the respondent. It is a floating-point value that indicates the number of people in the U.S. population this respondent represents.

In addition it uses several special codes:
- 97 NOT ASCERTAINED
- 98 REFUSED
- 99 DON'T KNOW

