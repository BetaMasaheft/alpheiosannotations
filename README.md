# alpheiosannotations
Here you can store json annotations exported from https://alignment.alpheios.net/. 
Please, watch the video on the landing page to see how it works. This is very important to make sure that the exported result is then usable.

Ideally you will use this to 
- align gez to transliterated gez
- annotate morphologically the aligned transliteration.

This is an alternative simplified workflow for adding morphological annotations. It does not have all the features of the GETA tool, but is included in the workflow, so that you can immediately see your annotations exploited. It is suggested for smaller pieces of alignment work or larger efforts done bit by bit.
The transliteration is not computed, you can try this tool if you do not have others https://betamasaheft.github.io/transliteration/ to obtain an initial one.

When doing this sort of annotations, you can additionally watch the following screencast.https://www.awesomescreenshot.com/video/5079573?key=e8ade0fa6c5a08ad4afa2ff4e24140ee

The steps are the following:
- copy paste or import from DTS your text
- copy paste or keydown the tranliteration
- follow details to enter metadata (IMPORTANT!!!) 
- follow alpheios guidance to prepare text (video above)
- edit the text to split tokens in the transliteration (conjunctoins, pronouns, etc.)
- do the alignment, carefully clicking until the alignment group is saved
- deactivate annotation mode if on
- double-click on one word of the gez text to pull up the information from the morphological parser + Dillmann
- copy-paste the link to the source in Dillmann
- add an annotation to the word in the transliteration: 
    - lemmaid will contain only the link to Dillmann in the form "https://betamasaheft.eu/Dillmann/lemma/L2f96c25794c6485eb46c3ae163c2676c" which may have copypasted from the parser or from Dillmann.
    - morpology will contain a string input, using the values of the TraCES annotations separated by semi-column, e.g. "Third;Singular;Masculine" or "Common Noun;feminineNP;SingularP UnmarkedS;Nominative;Construct state", the list is below. Any order, any combination. Since the values are all different, the type of label will be associated by the application.
    - you can add comments, this are however not exported at the moment.
- once you are done, export the json file and commit it to the main branch of this repository. 
- [the application](https://github.com/BetaMasaheft/alpheios2fs) will transform the data and store it where needed so that it will be immediatly used.

list of allowed [values, extracted from current TraCES data](https://github.com/BetaMasaheft/alpheios2fs/blob/main/alpheiosannotations/tracesValues.xml) 

### number
SingularP UnmarkedS, SingularP SingularS, SingularP, Singular, Plural, PluralIntP PluralS, PluralIntP, PluralIntP SingularS+ PluralS, PluralIntP SingularS, unmarkedP SingularS, PluralIntP UnmarkedS, PluralPl, PluralExtP, , PluralExtP UnmarkedS, Collective, PluralExtP PluralS, unmarkedP UnmarkedS, PluralPlP UnmarkedS, SingularP PluralS, PluralExtP SingularS, PluralPlP PluralS, PluralExtP SingularS+ PluralS, SingularP SingularS+ PluralS, unmarkedP PluralS, PluralPlP SingularS, unmarkedP, Unmarked.

### case
Nominative, Accusative, Vocative.

### pos 
Preposition, Common Noun, Conjunction, Independent Personal Pronoun, Proper Name, Verb, Pronominal Suffix, Other Adverb, Relative Pronoun, Punctuation, Pronoun of Totality Base, Cardinal Numeral, Demonstrative Pronoun, Negative Particle, Presentational Particle Base, Verbs, Interrogative Adverb, Other Particle, Pronoun of Solitude Base, Adverb, Interrogative Pronoun, Object Pronoun Base, Interrogative Particle, Quotative Particle, Subject Pronoun Base, Deictic Imperative Particle, Existential Negative Base, Foreign Material, Affirmative Particle, Existential Affirmative Base, Interjection, Vocative Particle, Ordinal Numeral, Accusative Particle, Possesive Pronoun Base, Other Particles, Existentials Affirmative base, Adverbs.

### logogram
20, 3, 2, 1, 5, 4, 100, 10, 6, 9, 50, 7, 8, 80, 10000, 60, 30, 40, 70, 90.

### distance
Near, Far.

### gender
unmarked, masculineN, masculineS, masculineP, Communis, Masculine, Feminine, masculinePS, masculine, feminineS, Nominal state, feminineN, femininePS, feminineP, masculineNS, , S, Unmarked, S unmarked, masculineS feminineS, Pronominal state, masculineS femininePS, feminineNPS, masculineS feminineP, masculineNP, feminineNS, feminineNP, P, masculineNPS, masculineP feminineS, feminine, Sunmarked.

### person
First, Third, Second.

### tamp
Perfect, subjunctive, Gerund, , Imperfect.

### state
Nominal state, Construct state, Absolute state, Pronominal state, , Feminine.

### tam
Perfect, Imperfect, subjunctive, Subjunctive, infinitive, Gerund, Imperative, Infinitive, gerund.
