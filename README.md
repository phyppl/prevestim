# True prevalence estimator using probabilistic programming

Copyright: Viktor Senderov and Savina Stoitsova, 2020
Email: vsenderov@gmail.com 
Licence: Apache Licence v2.0, 2020

This WebPPL script estimates true prevalence of something (e.g. a
disease) based on a survey using a testing procedure whose specificity
and sensitivity are known.

## Web interface

Use [directly in the web](https://phyppl.github.io/prevestim/).

## Manual usage

1. Open [source code](basic.wppl).
2. Paste source code in https://webppl.org.
3. Set sensitivity and specifity, as well as survey results by editting
the INPUT section.
4. Run the script in your browser by clicking run.

## Validation

The script has been validated against four epidemiological studies on
Covid-19. Our performance is comparabale to the performance in the
studies.

| Study       | Sensitivity (θ+) | Specificity (θ-) | Crude seropr.  | Adj. seropr.(study)  | Adj. seropr. (prevestim) | Ref |
|-------------|------------------|------------------|---------|------------------|------------------|-----|
| Santa Clara | 0.828            | 0.995            | 1.5%    | 1.2%             | 1.18%            | [1] |
| LA unweighted         | 0.827            | 0.995            | 4.06%   | 4.34%            | 4.27%            | [2] |
| LA weighted         | 0.827            | 0.995            | 4.31%   | 4.65%            | 4.56%            | [2] |
| Denmark     | 0.830            | 0.9954           | 1.8%    | 1.7%             | 1.631%           | [3] |
| Gangelt IgA    | 1                | 0.912            | 18.5%   | 10.63%           | 11.86%           | [4] |
| Gangelt IgG    | 0.909            | 0.991            | 13.6%   | 14.11%           | 14.03%           | [4] |

## Motivation

See Stringhi et al. [5, supplementary information] for a generalization of this model.

## References

1. Bendavid et al. (2020) COVID-19 Antibody Seroprevalence in Santa Clara County, California. https://doi.org/10.1101/2020.04.14.20062463.this

2. Sood et al. (2020) Seroprevalence of SARS-CoV-2–Specific Antibodies Among Adults in Los Angeles County, California, on April 10-11, 2020 https://jamanetwork.com/journals/jama/fullarticle/2766367?utm_campaign=articlePDF&utm_medium=articlePDFlink&utm_source=articlePDF&utm_content=jama.2020.8279

3. Erikstrup et al. (2020) Estimation of SARS-CoV-2 infection fatality rate by real-time antibody
screening of blood donors. preprint doi: https://doi.org/10.1101/2020.04.24.20075291

4. Streeck et al. (2020) Infection fatality rate of SARS-CoV-2 infection in a German community with a super-spreading event. https://doi.org/10.1101/2020.05.04.20090076

5. Stringhini et al. (2020). The Lancet. Seroprevalence of anti-SARS-CoV-2 IgG antibodies in Geneva, Switzerland (SEROCoV-POP): a population-based study. https://www.thelancet.com/pdfs/journals/lancet/PIIS0140-6736(20)31304-0.pdf
