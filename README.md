# tpw-data

## Meta
ownership: unknown
founded: 0000-00-00

---

### How is data scored?


#### bias_social `(-10 - 10)`

#### bias_economic `(-10 - 10)`

#### bias_ideological `(string)`
This field describes the political affiliation or bias of an organisation, supplementing the economic and social ratings to best fit particular interests within political spheres.

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
3  | Org. only publishes author name
4  | Org. only publishes author name and some editorial staff
5  | Same as a 6, but bylines never include a relevant bio.
6  | same as a 7, but bylines sometimes do not include a relevant bio.
7  | Same as an 8, but contributions are not filterable by author
8  | Same as a 10, but publication allows for use of anonymous publishing (less than 12 times per year).
9  | Same as a 10, but publication allows for infrequent use of anonymous publishing (once per year or less).
10 | Article bylines always include name, relevant bio, and social media links when applicable, contributions are filterable by author, full editorial board and directors are listed on an accesible masthead page when applicable.
-1 | Org. has never been assessed

#### subj_pseudoscience `(0 - 10)`
How often does a publication advertise, advocate for, or otherwise promote pseudoscience? Or, conversely, how often does a publication attack scientific findings in order to validate a conflicting belief? Publications that explitly cover fringe beliefs or document alternative medicine, traditional / folk remedies or similar subjects do not necessarily exist on this scale.

This rating, like other subjective categories, serves more to give an impression of a site than to affix a specific meaning by virtue of numerated values.

#### subj_conspiracy `(0 - 10)`

#### subj_message `(-1 / 0 - 10)`
This is the _balance index_, denoting how often a publication publishes stories that run contrary to their stated branding or message. A right-leaning publication running leftist authors when covering headlining stories, for instance, would place it anywhere from 1 to 4, whereas a completely _on brand_ publication that only publishes stories when they can be interpreted in a lens that is favourable to the publication's political leaning, would score a 10. Essentially, 0 is an impartial news aggregator, and 10 is a propaganda machine.

_This name was chosen deliberately to avoid the notion of "balanced coverage" of an issue, where some viewpoints are inherently less relevant at times, and may give undue weight to fringe or biased coverage. Instead, the messaging consistency of an organisation denotes how often they cover topics relative to their own stated commitment to the whole truth._

#### tags `([string])`
Tags denote the overall nature of a publication. Common tags in use now are _satire_ and _fake-news_, and are best applied when either a publication self-describes as an applicable tag _(Ex.: satire, state-owned)_ or the content of a site overwhelmingly warrants a notice _(Ex.: fake-news, single-author)_.

### Article selection
Sample a minimum of five recent articles _(recent: within six months)_. Selection need not be random, and if possible should target pieces that aim to establish a truth claim or narrative from current events. Articles that are syndications of previously published work should not be selected. If it is impossible to avoid syndicated content, their rating may be derived from the parent content's rating. Articles that summarize other content without additional analysis, are not good candidates for determining sourcing, as the facts of a situation may already be widely known _(Ex.: An article tallying election results)_.

### Fact Checking
