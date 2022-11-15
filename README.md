# HASOC2022-task3
========================

Marathi Offensive Language Identification Dataset (MOLD)


========================

1) DESCRIPTION

This is the README file for MOLD described in: https://doi.org/10.1007/s13278-022-00906-8

MOLD contains 3103 annotated tweets.

The files included in this phase are:

- MOLD_train.tsv contains 3103 annotated tweets.


The dataset was annotated using crowdsourcing. The gold labels were assigned taking the agreement of three annotators into consideration. No correction has been carried out on the crowdsourcing annotations.

Twitter user mentions were substituted by @USER and URLs have been substitute by URL.

MOLD is annotated using a hierarchical annotation. Each instance contains up to 3 labels each corresponding to one of the following levels:

- Level (or sub-task) A: Offensive language identification;

- Level (or sub-task) B: Automatic categorization of offense types;

- Level (or sub-task) C: Offense target identification.

2) FORMAT

Instances are included in CSV format as follows:
The column names in the file are the following:

id	tweet	subtask_a	subtask_b	subtask_c
Whenever a label is not given, a value NULL is inserted (e.g. INSTANCE	NOT	NULL	NULL)


The labels used in the annotation are listed below.

3) TASKS AND LABELS

(A) Level A: Offensive language identification

- (NOT) Not Offensive - This post does not contain offense or profanity.
- (OFF) Offensive - This post contains offensive language or a targeted (veiled or direct) offense

In our annotation, we label a post as offensive (OFF) if it contains any form of non-acceptable language (profanity) or a targeted offense, which can be veiled or direct.

(B) Level B: Automatic categorization of offense types

- (TIN) Targeted Insult and Threats - A post containing an insult or threat to an individual, a group, or others (see categories in sub-task C).
- (UNT) Untargeted - A post containing non-targeted profanity and swearing.

Posts containing general profanity are not targeted, but they contain non-acceptable language.

(C) Level C: Offense target identification

- (IND) Individual - The target of the offensive post is an individual: a famous person, a named individual or an unnamed person interacting in the conversation.
- (GRP) Group - The target of the offensive post is a group of people considered as a unity due to the same ethnicity, gender or sexual orientation, political affiliation, religious belief, or something else.
- (OTH) Other – The target of the offensive post does not belong to any of the previous two categories (e.g., an organization, a situation, an event, or an issue)

Label Combinations

Here are the possible label combinations in the MOLD annotation.

-	NOT NULL NULL
-	OFF UNT NULL
-	OFF TIN (IND|GRP|OTH)
