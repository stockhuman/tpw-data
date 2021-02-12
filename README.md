# tpw-data

## Meta
**ownership**: `string`, parent company, proprietor(s) or other

**founded**: `0000-00-00`, date of founding, using domain purchase date if uncertain

**lang**: `[string]`, languages publication is translated in, or produces separate content for

---

### How is data scored?


#### bias_social `(-10 - 10)`
This rating places a publication's average political leaning on the commonly understood social left/right spectrum. As with other attempts at reducing political complexity to so few axes of values, this axis primarily represents the publication's embrace or regection of social values evident in coverage, describing the _desired sociopolitical outcome_ aspect of ideological positions on issues such as healthcare type and availability, religious freedom, moral values, identitarian interests, and the nature of violence. Combined with the ideological descriptor, it can inform bias towards socioeconomic classes or identities.

The frequency of support for political positions (or attack of competing positions) by any means (see bias types factored for analysis) places `-10` as support for extreme-left social causes and `10` as support for its far-right equivalent. A zero indicates either a perfect balance of biases or a lack of content that meaningfully engages with arguments that push this bias in either direction.

A data entry must always contain this rating, there is no unrated value.

#### bias_governmental `(-10 - 10)`
This rating places a publication's average political leaning on the commonly understood authoritarian/libertarian spectrum. As with other attempts at reducing political complexity to so few axes of values, this axis primarily represents the publication's embrace or regection of legislation at any level, describing the _governmental size and scope_ aspect of ideological positions on issues such as military spending, taxation policy, power projection, policing, free trade, governmental structure, and support for authorities. Combined with the ideological descriptor, it can inform a bias towards individualism or collectivism in opinion pieces.

The frequency of support for political positions (or attack of competing positions) by any means (see bias types factored for analysis) places `-10` as support for anarchy and `10` as support for totalitarianism. A zero indicates either a perfect balance of biases or a lack of content that meaningfully engages with arguments that push this bias in either direction.

A data entry must always contain this rating, there is no unrated value.

#### bias_ideological `(string)`
This field describes the political affiliation or bias of an organisation, supplementing the economic and social ratings to best fit particular interests within political spheres. This tag should be informed by self-description on the part of the organisation when applicable, and by the conventional bias analysis otherwise.

#### fact_sourcing `(-1 / 0 - 10)`
This rating denotes both the quality and quantity of individual inline citations within any given article. Whilst contextually dependant (opinion pieces need not necessarily cite sources, not all claims within an article support its thesis and thus warrant sourcing), most articles that attempt to draw conclusions from exterior facts should cite them.

This rating should be be revised with major editorial staff or ownership changes, or in response to failed fact checks.
When rating, assume an initial score of 10 and count downwards. See Fact Checking section.

1. Subtract at least a point for any known failed fact check in the history of the publication. A minor fact check fail leaves the score at 9. A since-retracted claim is treated as a minor fail.
2. With each article studied, subtract fact checks as appropriate against the major thesis of each piece to a maximum subtraction of 7, leaving at least a rating of 2.
3. Subtract a point for citation quality as necessary
4. Subtract the final point for any misleading citations of data, or out of context quotes

Rating | Meaning
-- | ------------
0  | Org. does not meaningfully care about sourcing claims / does not cite
1  | Org. does not cite sources, or does so with misleading or wrong sources
2  | Org. may cite sources, but routinely publishes misleading or false claims
3  | Org. may routinely publish misleading or false claims amidst regular reporting
4  | Org. is unreliable with regards to sourcing and factual accuracy
5  | Org. may be unreliable with regards to sourcing and factual accuracy
6  | Org. generally reports with some verifiable sources, with exceptions
7  | Org. mostly reports with verifiable sources, with few, minor exceptions
8  | Org. reliably reports with verifiable sources, with few, minor exceptions
9  | Org. reliably reports with verifiable sources, has failed at most a single fact check
10 | Org. always reports with verifiable sources, has never failed a fact check or misused data
-1 | Org. has never been assessed

#### fact_editorial `(-1 / 0 - 10)`
This rating reflects how easily one can obtain information regarding the individuals writing for a news organisation. Self-published sources with sole authorship _(a personal blog)_ shall be rated as `-1`, as this scale does not apply.

Rating | Meaning
-- | ------------
0  | Org. deliberately conceals the authorship of idividual articles and the editorial board
1  | Org. normally conceals author names (at least one named byline in past 6 months)
2  | Org. sometimes publishes author name (>50% named bylines)
3  | Org. only publishes author name or publishes other details but author may use a pseudonym
4  | Org. only publishes author name and some editorial staff
5  | Same as a 6, but bylines never include a relevant bio.
6  | same as a 7, but bylines sometimes do not include a relevant bio.
7  | Same as an 8, but contributions are not filterable by author
8  | Same as a 10, but publication allows for use of anonymous publishing (less than 12 times per year) _or_ editorial situation reflects a 10 rating with an exception from ratings 4 through 7 (ex.: Names posted without relevant bio).
9  | Same as a 10, but publication allows for infrequent use of anonymous publishing (once per year or less).
10 | Article bylines always include name, relevant bio, and social media links when applicable, contributions are filterable by author, full editorial board and directors are listed on an accesible masthead page when applicable.
-1 | Org. has never been assessed

#### subj_pseudoscience `(0 - 10)`
How often does a publication advertise, advocate for, or otherwise promote pseudoscience? Or, conversely, how often does a publication attack scientific findings in order to validate a conflicting belief? Publications that explitly cover fringe beliefs or document alternative medicine, traditional / folk remedies or similar subjects do not necessarily exist on this scale.

This rating, like other subjective categories, serves more to give an impression of a site than to affix a specific meaning by virtue of numerated values.

#### subj_conspiracy `(0 - 10)`
How often does a publication suggest, promote, invent  or otherwise endorse conspiracy theories? Like the pseudoscience rating, publications that explitly cover the aesthetics or meaning of conspiracy theories in an academic or journalistic meta-context do not necessarily exist on this scale.

This rating serves as an indicator of the severity and frequency of any conspiracy theories promoted by the organisation. Theories that advocate for genocide and either promote or act as plausible deniability for human rights abuses are rated more harshly. _Maintaining any of the following theories or patterns as fact constitutes an automatic 8 or above:_ Genocide or war crimes denial (apply `state-owned` tag when applicable), genetic inferiority or supremacy of any peoples, and the Great Replacement Theory (and similar racialized conflict meta-theories).

This rating, like other subjective categories, serves more to give an impression of a site than to affix a specific meaning by virtue of numerated values.

#### subj_message `(-1 / 0 - 10)`
This is the _balance index_, denoting how often a publication publishes stories that run contrary to their stated branding or message. A right-leaning publication running leftist authors when covering headlining stories, for instance, would place it anywhere from 1 to 4, whereas a completely _on brand_ publication that only publishes stories when they can be interpreted in a lens that is favourable to the publication's political leaning, would score a 10. Essentially, 0 is an impartial news aggregator, and 10 is a propaganda machine.

_This name was chosen deliberately to avoid the notion of "balanced coverage" of an issue, where some viewpoints are inherently less relevant at times, and may give undue weight to fringe or biased coverage. Instead, the messaging consistency of an organisation denotes how often they cover topics relative to their own stated commitment to the whole truth._

#### tags `([string])`
Tags denote the overall nature of a publication. Common tags in use now are `satire` and `fake-news`, and are best applied when either a publication self-describes as an applicable tag _(Ex.: `satire`, `state-owned`)_ or the content of a site overwhelmingly warrants a notice _(Ex.: `fake-news`, `single-author`)_.

---

### Article selection
Sample a minimum of five recent articles _(recent: within six months)_. Selection need not be random, and if possible should target pieces that aim to establish a truth claim or narrative from current events. Articles that are syndications of previously published work should not be selected. If it is impossible to avoid syndicated content, their rating may be derived from the parent content's rating. Articles that summarize other content without additional analysis, are not good candidates for determining sourcing, as the facts of a situation may already be widely known _(Ex.: An article tallying election results)_.

### Fact Checking
When checking articles for false or misleading claims, recognized fact-checking resources may be used, as well as common sense and, with ample evidence, original research. This project shall organically determine which fact checking organisations may be deemed reliable in their respective fields of expertise, and likewise what standards of original research are permissable on a case by case basis. _Common sense_ fact checking generally applies only to blatanty false information that makes great, extraordinary claims for the purposes of clickbaiting.

Failed fact checks are rated on a severity scale as follows:

Severity | Meaning
-------- | -------
Minor    | The failed check does not affect the substance of the article. If retracted or corrected during the article's relevance, it does not count. The window of relevancy relies greatly on publishing frequency and the prominence of the article within the broader media landscape and the publication itself (ex.: cover stories). Incorrect dates, figures and names may be counted within reason as minor fact checking failures assuming they do not impact the substance of the article.
Moderate | These failed fact checks _plausibly_ reject the thesis, headline or conclusion of an article. Major _supporting_ claims without evidence may be counted as moderate or minor depending on the overall claims within a story.
Severe   | A severe fact check fail impacts the validity of the article as a whole. The central thesis, headline or conclusion must be logically negated to be counted as severe. Examples include claiming events that did not happen, distorting timelines to fit a narrative, falsifying statements or evidence, presenting false or anachronous statistics (when more recent ones are available) or otherwise directly manipulating reporting to create a false narrative.

### Bias Analysis

*Support*

*Bias by omission*

*Denouncement*

---
A note on stances: this project aims for an international weighting on issues, whilst recognizing local contexts.

As an example, the United States' lack of universal health care places it in the [global minority](https://en.wikipedia.org/wiki/List_of_countries_with_universal_health_care), where public health care is generally regarded as a minor left-leaning issue or politically neutral (without further context). A non-American source commenting negatively on this issue need not be labelled left-leaning by virtue of the American position being comparatively right-wing.
