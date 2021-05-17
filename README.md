# ccg-latex

The commands in the <code>ccg-latex.sty</code> file can be used to typeset Combinatory Categorial Grammar (CCG) derivations in latex.

The example file shows how.

The basic command is <code>\begin{ccg}{n}{data}{ders}\end{ccg}</code>. 

It typesets
in n columns data, possibly multilined with <code>\\\\</code>, and derivations (ders), each line separated by <code>\\\\</code>, without glosses. 

It has a variant, <code>\begin{ccgg}{n}{data}{gloss}{ders}\end{ccgg}</code>,
which typesets glosses before the top lines are drawn.

Both are based on <code>\cgex{n}{lines}</code>, which is kept for legacy code, where <code>n</code> is the number of columns,
and <code>lines</code> is the double-backslash-separated lines of at most that many columns.

Basic commands other than above (see the style file for a full list:

<code>\cgf{..}</code> typesets the syntactic category.

<code>\cat{..}</code> typesets the syntactic category. It is an alias of <code>\cgf{..}</code>.

<code>\lf{..}</code> typesets the logical form, including the colon and math mode.

<code>\fs</code> is the forward slash. We also have <code>\bs, \us, \fss, \bss</code>
as backslash, undirectional slash, double forward slash and backward, etc.
Use <code>\fs</code> and <code>\bs</code> consistently, rather than '/' for forward slash and say <code>\bs</code> for backslash,
for consistent rendering of the syntactic types.

Some of these slashes have aliases. <code>\fss, \bss, \uss</code> are resp. <code>\rds, \lds, \uds</code>.

<code>\combx</code> typesets the combinator x in bold Curry and Feys notation.

<code>\cgs{cat}{features}</code> typesets category cat subscripting the features. For example NP<sub>acc</sub> is \cgs{NP}{acc}.
VP<sub>fin=+,agr=3s</sub> is \cgs{VP}{fin=+,agr=3s}.

<code>\cgline{n}{rulename}</code> draws a CCG line across n columns, and indexes it with the rule. 

Rule names are <code>\cgfa, \cgba, \cgfc, \cgbc</code> etc. Rulename need not be a pre-defined rule name.

<code>\cgres{n}{..}</code> typesets the CG result in the material .. across n columns. The ... is typeset as \cgf{...}. If there is math mode in it,
that is typeset in math mode.

<code>\cglines{n}</code> typesets n undecorated lines separated by blanks, which is common practice after lexical assumptions.
These are entered by default in {ccg} and {ccgg} environments above.

<code>\badline{n}{rulename}</code> typesets a line spanning n columns with <code>***</code> in the middle, with rule name at the end.

<code>\mc{n}{text}</code> typesets the text multi-column centered over n columns; useful for foreign language glossing.

<code>\fstars</code> is a forward slash with star modality, i.e. <code>/*</code>. 

<code>\bxs</code> is a backward slash with crossing modality, i.e. <code>\x</code>. 

Defined for all slashes and modalities.

enjoy.

-cem bozsahin
