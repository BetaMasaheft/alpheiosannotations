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
- edit the text to split tokens in the transliteration (conjunctions, pronouns, etc.)
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


### pos 
<val>Preposition</val>
        <val>Common Noun</val>,
        <val>Conjunction</val>,
        <val>Independent Personal Pronoun</val>,
        <val>Proper Name</val>,
        <val>Verb</val>,
        <val>Pronominal Suffix</val>,
        <val>Other Adverb</val>,
        <val>Relative Pronoun</val>,
        <val>Punctuation</val>,
        <val>Pronoun of Totality Base</val>,
        <val>Cardinal Numeral</val>,
        <val>Demonstrative Pronoun</val>,
        <val>Negative Particle</val>,
        <val>Presentational Particle Base</val>,
        <val>Interrogative Adverb</val>,
        <val>Other Particle</val>,
        <val>Pronoun of Solitude Base</val>,
        <val>Adverb</val>,
        <val>Interrogative Pronoun</val>,
        <val>Object Pronoun Base</val>,
        <val>Interrogative Particle</val>,
        <val>Quotative Particle</val>,
        <val>Subject Pronoun Base</val>,
        <val>Deictic Imperative Particle</val>,
        <val>Existential Negative Base</val>,
        <val>Foreign Material</val>,
        <val>Affirmative Particle</val>,
        <val>Existential Affirmative Base</val>,
        <val>Interjection</val>,
        <val>Vocative Particle</val>,
        <val>Ordinal Numeral</val>,
        <val>Accusative Particle</val>,
        <val>Possesive Pronoun Base</val>
        
### number
 <val>Singular</val>,
        <val>Plural</val>,
        <val>Unmarked</val>,
        <val>SingularS</val>,
        <val>PluralS</val>,
        <val>UnmarkedS</val>,
        <val>SingularP</val>,
        <val>PluralIntP</val>,
        <val>PluralExtP</val>,
        <val>PluralPlP</val>,
        <val>PluralPl</val>,
        <val>UnmarkedP</val>,
        <val>Collective</val>
  (multiple values possible)   

### case
Nominative, Accusative, Vocative.

### logogram
20, 3, 2, 1, 5, 4, 100, 10, 6, 9, 50, 7, 8, 80, 10000, 60, 30, 40, 70, 90.

### distance
Near, Far.

### gender
 <val>Unmarked</val>,
        <val>MasculineN</val>,
        <val>MasculineS</val>,
        <val>MasculineP</val>,
        <val>Communis</val>,
        <val>Masculine</val>,
        <val>Feminine</val>,
        <val>MasculinePS</val>,
        <val>FeminineS</val>,
        <val>FeminineN</val>,
        <val>FemininePS</val>,
        <val>FeminineP</val>,
        <val>MasculineNS</val>,
        <val>S</val>,
        <val>Sunmarked</val>,
        <val>FeminineNPS</val>,
        <val>MasculineNP</val>,
        <val>FeminineNS</val>,
        <val>FeminineNP</val>,
        <val>P</val>,
        <val>MasculineNPS</val>
(multiple values possible)

### person
First, Third, Second.

### state
Nominal state, Construct state, Absolute state, Pronominal state.

### temp
Perfect, Imperfect, Subjunctive, Gerund, Imperative, Infinitive.
