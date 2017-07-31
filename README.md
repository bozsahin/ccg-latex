The commands in the <code>ccg-latex.sty</code> file can be used to typeset Combinatory Categorial Grammar (CCG) derivations.

Example file shows how.

The basic command is <code>\begin{ccg}..\end{ccg}</ccg>. It typesets
derivations without glosses. It has a variant, <code>\begin{ccgg}..\end{ccgg}</code>,
which typesets glosses before the top lines are drawn.

Both are based on <code>\cgex{n}{ders}</code>, which is kept for legacy code, where <code>n</code> is the number of columns,
and <code>ders</code> is the <code>\\</code>-separated lines of at most that many columns.
