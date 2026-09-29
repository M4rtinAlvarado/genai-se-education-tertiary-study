# Detailed Methodology

This document extends Section II of the paper. It describes the procedure as executed, with the search
string, selection criteria, extraction and coding rules, the tools used at each stage, and the deviations
from the initial protocol. The prompts are in [`prompts/`](prompts/) and the included studies in
[`included_studies/`](included_studies/).

## 1. Study design and research questions

The study combines a tertiary review, which delimits the field and serves as a sampling frame, with a
mapping of the primary studies that these reviews cite. Reviews aggregate evidence at a level that hides
the didactic technique behind each practice, so we traced their primary studies, where practices are
described in enough detail to be classified. We followed the guidelines of Kitchenham and Charters for the
search, selection and extraction, and we report the use of large language models (LLMs) following
PRISMA-trAIce ([`PRISMA-trAIce.md`](PRISMA-trAIce.md)). The process had four phases (Fig. 1): search and
selection of reviews, data extraction from the reviews, tracing of primary studies, and classification and
cross-mapping.

The research questions are:

- RQ1. In which software engineering teaching and learning activities is GenAI incorporated, and to which
  SWEBOK Knowledge Areas (KAs) do they correspond?
- RQ2. Through which didactic techniques is GenAI incorporated, and which cognitive processes do these
  techniques target?

The extraction instrument applied to the reviews was broader. It had seven questions: (1) activities,
(2) didactic strategies, (3) effects on learning, (4) assessment, (5) benefits and risks, (6) research
gaps, and (7) competencies less susceptible to automation. Questions 1 and 2 feed RQ1 and RQ2. The Results
also draw on question 7 when discussing higher-order competencies, and on questions 3, 5 and 6 as context.

## 2. Search

We searched OpenAlex, an open bibliographic index that aggregates the main publishers in the field (among
them ACM, IEEE, Springer and Elsevier) and allows the full query to be exported. The project had no access
to Scopus or Web of Science, and Google Scholar was discarded because its searches cannot be reproduced.

The string combined four blocks with AND, plus an exclusion block:

```
("software engineering" OR "software development" OR "programming education" OR "computer science
education" OR "requirements engineering" OR "coding education" OR "programming course" OR "computing
education") AND (education OR educational OR pedagogy OR pedagogical OR teaching OR student OR students
OR curriculum OR classroom OR course) AND ("generative AI" OR "generative artificial intelligence" OR
GenAI OR LLM OR LLMs OR "large language model" OR "large language models" OR ChatGPT OR "AI-assisted")
AND (SLR OR "systematic literature review" OR "systematic review") NOT (dermatology OR manufacturing OR
marketing OR "civil engineering" OR nursing OR "social network")
```

| Parameter | Value |
|---|---|
| Period | 2023–2026 (from 1 January 2023, after the public release of ChatGPT) |
| Document types | article, review, conference paper, book chapter, preprint (preprints were retrieved in order to exclude them under EC10 when no peer-reviewed version existed) |
| Fields | OpenAlex default search (title, abstract and, when available, full text) |
| Language | Not filtered in the query; controlled during screening (EC8) |
| Deduplication | Normalized title (Unicode, lower case, no punctuation) |

The first run returned 96 records, 83 after removing 13 duplicates. We also tested a broader string without
the study-type block, aimed at primary studies. It returned 2,119 unique titles, and only 19% of those
exclusive to it were rated as highly relevant in a pre-assessment of their abstracts. We therefore
reached primary studies through the reviews (Section 5) rather than by direct search. On 10 August 2026 we
re-ran the same string. It returned 7 new records, all from 2026, which were screened with the same
criteria, giving 90 records in total.

## 3. Selection of reviews

Stage 1, title and abstract. Three authors split the 83 records of the first run (28, 28 and 27), one
author per record. Each record received an exclusion criterion or, if it passed, a rating of its relevance
to the project. There was no independent double screening. We excluded 50 records and retained 40.

| Code | Excluded studies… | n |
|---|---|---:|
| EC1 | do not address the use, impact, integration or implications of GenAI, LLMs or tools based on them | 3 |
| EC2 | do not analyze GenAI in relation to teaching, learning, assessment, competency development or other educational activities | 12 |
| EC3 | have a disciplinary context outside software engineering, software development, programming or computing education | 4 |
| EC4 | focus exclusively on primary, secondary or other levels outside higher education | 2 |
| EC5 | are primary studies, opinion papers, editorials, essays, conceptual proposals or works without an explicit literature review process | 3 |
| EC6 | provide no information to answer at least one research question | 0 |
| EC7 | focus exclusively on traditional AI, machine learning, expert systems or automated assessment without GenAI or LLMs | 0 |
| EC8 | are not published in English | 6 |
| EC9 | have no accessible full text | 3 |
| EC10 | are available only as preprints, working papers or repository documents without peer review | 17 |
| | Total | 50 |

Each record was counted under the first criterion recorded. Eight records had more than one, usually EC2
together with EC3.

Stage 2, full text. Two of the 40 records had no accessible full text and were excluded under EC9. We
obtained 38 full texts.

Stage 3, relevance on the full text. Claude Sonnet 5 rated each of the 38 full texts against the focus of
the study: university teaching and assessment that integrate GenAI to develop software engineering
competencies beyond programming (requirements, design, architecture, construction, testing, maintenance,
quality, management, teamwork). The levels were high (addresses how GenAI is used in teaching software
engineering and discusses concrete effects on learning), medium (direct pedagogical relation, but one of
the two elements is missing or underdeveloped), low (general context or passing mention) and none. The
model worked from the body of the text, not the abstract, and returned a justification and a supporting
quote for each document. The prompt asked it to avoid frequent confusions (a tool with teaching, AI
performance with learning, research use with educational integration, traditional AI with GenAI) and to
assign medium in case of reasonable doubt. The result was 12 high, 22 medium, 3 low and 1 none. We kept
the high and medium reviews and excluded the other 4, plus one moderately relevant review that analyzes the capabilities and limitations of LLM coding chatbots
rather than their integration into teaching, and whose authors state that it does not cover software
engineering.
The authors confirmed these exclusions. The final corpus has 33 reviews.

## 4. Data extraction from the reviews

Claude Sonnet 5, run through Claude Code, read the full PDF of each review in blocks of up to 20 pages,
without access to earlier extractions or other project files. Each review was processed with three
independent prompts: (1) identification and quality, (2) research questions, and (3) additional findings.
Each prompt returned a table with the item, its value, a verbatim quote and its location. The three
tables were merged into an extraction matrix of 1,188 rows (33 reviews × 36 items).

| Block | Items |
|---|---|
| Identification (12) | title, authors, year, DOI, venue, country or context, review type, period covered, number of included studies, databases, educational area, educational level |
| Quality (10) | QA1–QA9 and a score from 0 to 10 |
| Research questions (7) | the seven questions of the instrument (Section 1), each with its coverage (high, medium, low or none), a synthesis and supporting quotes |
| Additional findings (7) | GenAI tools, theoretical frameworks, assessment instruments, definitions, recommendations, further quotes, other findings |

The same rules applied to the three prompts. The model had to use only the content of the article, record
"N/E" when a datum was absent, support every statement with a short verbatim quote in the original language
and its location, never invent page numbers, and declare a question as not covered rather than infer it.
It also had to distinguish whether the review asserts a finding (authors' opinion or a claim from another
work) or demonstrates it with its own results, and whether the finding is a perception (self-report) or an
objective measurement. Every quality and research-question row with content carries a quote and a
location.

Quality was assessed with nine criteria derived from the guidelines for secondary studies: (QA1) clear
objectives and questions; (QA2) reproducible search strategy with a search string; (QA3) explicit databases
and period; (QA4) explicit inclusion and exclusion criteria; (QA5) described selection process with
measures against bias; (QA6) described extraction and synthesis; (QA7) traceability between studies and
findings; (QA8) conclusions supported by the evidence; and (QA9) discussion of limitations or threats to
validity. Each criterion scored 1 (met), 0.5 (partly met) or 0 (not met), with a justification and a quote,
and the sum was rescaled to 0–10. Quality was not used to exclude reviews. It is reported descriptively.

The template and prompts were refined in a pilot. A first version used a single integrated prompt
(Claude Sonnet 5). During the pilot, the authors read a subset of reviews following a manual reading
protocol and compared their reading with the model output. The comparison was qualitative and supported
adopting the assisted procedure. The pilot output was used to select the snowballing seeds (Section 5).
All data reported in the paper come from the final three-prompt extraction.

## 5. Tracing the primary studies

Seeds. We selected as seeds the reviews that could provide primary studies for both research questions,
based on the coverage recorded in the pilot extraction: high coverage of activities (question 1), high or
medium-high coverage of didactic strategies (question 2), and at least medium coverage of competencies less
susceptible to automation (question 7). We added p29, one of only three reviews with high coverage of
question 7. p21 entered as a seed through an error in applying the criterion (its coverage of question 2
was medium) and was kept. The ten seeds are marked in [`included_studies/reviews.csv`](included_studies/reviews.csv).

Screening. We applied one iteration of backward snowballing to the reference lists of the ten seeds, in two
passes. We retained only references that were themselves studies on GenAI or LLMs applied to teaching
programming, software engineering or computing, and discarded reviews from other domains, methodological
papers and general AI work without an educational context. The first pass applied the criterion strictly.
The second revisited the same reference lists with a broader reading to recover discarded titles, and
added the reference list of p29. Claude Sonnet 5 applied the criterion, and the first author reviewed part
of the resulting list. The screening identified 113 unique candidates.

Retrieval. We downloaded automatically only legitimate open-access copies (arXiv, open-access journals and
institutional repositories), without circumventing paywalls or access protections: 72 candidates. Another 7
open-access papers were downloaded manually through a browser, and 23 were obtained through institutional
access. In total we obtained 102 of the 113 candidates (90%); the other 11 were not available. One document
(Mak et al., 2025) was excluded as the same work as a review excluded at stage 3, leaving 101 primary
studies (listed in [`included_studies/primary_studies.csv`](included_studies/primary_studies.csv)).

## 6. Classification and cross-mapping

Vocabularies. Two controlled vocabularies were used:

- Knowledge Areas (RQ1): 15 of the 18 KAs of the SWEBOK Guide V4.0, with their subtopics. We excluded the
  three foundation KAs (Computing, Mathematical and Engineering Foundations) because they describe
  background knowledge shared with other disciplines rather than software engineering practice.
- Didactic techniques (RQ2): the 100 techniques of the UnADM catalogue, coded T001–T100. The catalogue
  groups them into six cognitive levels inspired by Anderson and Krathwohl: remember (11 techniques),
  explain (19), apply (27), analyze (17), synthesize (14) and construct (12). The level of each practice is
  the one the catalogue assigns to its technique. It expresses the aim of the technique, not the level
  attained by students.

Unit of analysis. We coded each GenAI-supported educational practice described in a study, not the study
as a whole. For each practice we recorded a short description, the KA and subtopic (and a secondary KA when
the practice clearly develops a second competence), the technique, the cognitive level, the status
(implemented and evaluated, implemented without evaluation, proposed, or recommended), the type of outcome
reported (perception, objective learning measure, or tool performance), and a verbatim quote with its
location.

Coding rules. A KA or a technique was assigned only when the study addressed it explicitly, never by
thematic proximity. The KA follows the competence the practice develops: introductory programming
(writing, reading or debugging code) was coded as Construction, and "outside SWEBOK" was reserved for
practices that develop no software engineering competence. The technique represents how the activity is
organized (workshop, project, role play, case, and so on), regardless of the name the study gives it. A
clear practice without an equivalent technique was coded "no equivalent", and a practice whose format the
study does not describe, "not determinable". Research instruments of the study itself (surveys,
interviews, pre- and post-tests, the researchers' content analysis) were not treated as practices, even
when they match catalogue techniques such as questionnaire (T032), interview (T039) or case study (T066).
Benchmarks that only evaluate the tool and passing mentions in the related work were not treated as
practices either.

Procedure. NotebookLM coded the studies on 26 September 2026, in one independent query per study whose
only sources were the study's PDF and the two vocabularies. The prompt required a verbatim quote for every
practice. The 19 studies for which the first query found no practice were queried a second time with an
instruction to review the whole article, including concrete proposals and recommendations for teaching.
The responses were processed by script: every KA had to belong to the vocabulary, every subtopic to its
KA, and every code to the catalogue; the cognitive level was taken from the catalogue; and every quote was
searched for in the text of the PDF. Of 265 quotes, 245 were found literally or partially, 18 were
paraphrased and 2 were not found. The coding produced 265 GenAI practices in 87 studies. The other studies
describe no teaching practice (most only evaluate a model's performance). This coding replaced an earlier
study-level coding, which recorded which techniques and KAs each study addressed and therefore paired
techniques and KAs from different activities of the same study.

Mapping. With the practices that have both a catalogued technique and a KA, we built a matrix of 100
techniques by 15 KAs in which each cell counts practices. Grouping the techniques by cognitive level gives a
matrix of 6 levels by 15 KAs, which answers RQ1 and RQ2 jointly. The distribution by KA counts the studies
with at least one practice in that KA, as primary or secondary KA. Cells were classified as no evidence,
isolated evidence (1–2) or recurrent evidence (3 or more). These thresholds are exploratory. An empty cell
means that the search strategy retrieved no studies for that combination, not that none exist. All counts
were produced by script from the coding spreadsheet. The complete map is in [`results/`](results/).

## 7. Use of LLMs and human verification

The initial protocol did not plan the use of LLMs. We adopted them on 27 August 2026, after a feasibility
test on one review, because of the volume of material (33 reviews that together include 1,640 primary
studies, with overlap, plus 101 primary studies) and the need to apply the controlled vocabularies
consistently.

| Stage | Tool | Task | Input | Output | Human oversight |
|---|---|---|---|---|---|
| Relevance of full texts (stage 3) | Claude Sonnet 5 (Anthropic), Claude Code | Rate each review against the focus of the study | 38 full texts | Level, justification and quote per review | Exclusions confirmed by the authors |
| Extraction and quality of reviews | Claude Sonnet 5, Claude Code | Fill the three-part template | 33 full texts | 1,188-row matrix with quotes and locations | Qualitative comparison in the pilot; blind sample |
| Snowballing screening | Claude Sonnet 5, Claude Code | Apply the relevance criterion | Reference lists of 10 seeds | 113 candidates | Partial review by the first author |
| Coding of primary studies | NotebookLM (Google), 26 Sep 2026 | Identify practices and assign KA, technique, status and outcome type | 102 full texts + 2 vocabularies, one query per study | 265 practices with quotes and locations | Script validation of codes and quotes; blind sample |
| Counts and matrices | Own Python scripts | Consolidate and count | Coding spreadsheet | Matrices and tables | Script verification |

No model was fine-tuned. NotebookLM does not expose its model version or generation parameters, and Claude
was used with default settings. Both systems are non-deterministic, so reproducibility is at the level of
procedure and prompts, not of identical outputs. The full texts, including those obtained through
institutional access, were processed by these services only for text analysis and are not redistributed.
The research questions, criteria, vocabularies, seed selection and final inclusion decisions were made by
the authors.

To estimate the agreement between the models and human coding, we drew a reproducible random sample (seed
20260924) of 8 of the 33 reviews and 15 of the 101 primary studies. Two authors code it independently, with
forms equivalent to the prompts and without access to the model output or to each other's work. For the
reviews we compare the coverage of RQ1 and RQ2 and the nine quality verdicts; for the primary studies, the
KAs, the techniques and the distinction between learning activity and research instrument. Agreement is
reported as percentage agreement and Cohen's κ per dimension.

## 8. Deviations from the initial protocol

The initial protocol (v1.0, 13 July 2026, internal and unregistered) planned a mapping of primary studies.
The following amendments were made during execution.

| Element | Protocol v1.0 | As executed | Reason |
|---|---|---|---|
| Design | Mapping of primary studies, with reviews as context | Tertiary review as sampling frame + mapping of primary studies by snowballing | The broad string returned 2,119 titles with low relevance; the reviews gave traceable access to relevant primary studies |
| Sources | OpenAlex, ACM, IEEE, DBLP, Crossref, ERIC, Google Scholar | OpenAlex | Single reproducible, exportable source |
| Language | English or Spanish | English (EC8) | |
| Screening | Double screening or 20% calibration | One screener per record; blind sample to verify the LLM output | Project timeline |
| Snowballing | Backward and forward, until saturation | One backward iteration from 10 seeds | Project timeline |
| Quality | Quality assessment of primary studies | Quality assessment of the reviews only | Change to a tertiary design |
| Unit of analysis | Atomic evidence per activity | Educational practice, after a first study-level coding | Study-level coding paired techniques and KAs from different activities |
| Tools | No LLMs | LLMs in relevance rating, extraction, screening and coding | Volume and consistency (Section 7) |

## 9. Threats to validity

- Identification. A single source and a string restricted to reviews that call themselves systematic.
  Snowballing was one backward iteration from ten seeds, and at least 6 of the 11 studies not retrieved deal
  with specific software engineering areas (modelling, user stories, agile management, security,
  verification and validation), which biases the map against the less populated KAs.
- Selection. One screener per record at stage 1. The full-text relevance rating and the snowballing
  screening were performed by an LLM with partial human oversight.
- Extraction and coding. LLMs are non-deterministic, and completeness depended on how the queries were
  configured.
- Construct. The cognitive level is inherited from the technique and expresses its aim, not the level
  attained; the catalogue has no "evaluate" level; almost half of the practices have no equivalent
  technique (25%) or do not describe their format (23%), so the cognitive map rests on 139 of the 265
  practices.
- Generalization. Introductory programming dominates: 79% of the practices fall in Construction, and 25
  practices (9%) fall outside SWEBOK.
