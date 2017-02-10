---
layout: relation
title: 'compound:vo'
shortdef: 'verb-object compound'
udver: '2'
---

The `compound:vo` relation is used for verb-object compounds where the combination is semantically one unit but syntactically separate. These are known as 離合詞 "separable words" in Chinese linguistics.

These compounds run the range of:

- (i) light verb constructions where the noun carries more semantic weight than the verb
  - e.g., 打␣電話 / _dǎ-diànhuà_ hit-telephone "make a phone call" (which might be equivalent to `compound:lvc` in other languages) 
- (ii) both the verb and noun contributing relatively equal semantic weight
  - e.g., 讀␣書 / _dú-shū_ read-book "study"
- (iii) situations where the verb carries the semantic weight over a redundant or relatively empty noun
  - e.g., 睡␣覺 / _shuì-jiào_ sleep-sense "sleep", where the noun 覺 no longer has a modern lexical usage and in fact the verb 睡 can be and is often used on its own to convey the same meaning

All of the above cases have the same syntactic distribution, where the object behaves like a direct object of the verb. Therefore, verb-object compounds never take another object as direct object, and the object can be separated from the verb as in regular non-compound situations. 

For example, aspect markers as well as adverbials of duration and frequency, when present, come in between:

~~~ conllu
# visual-style 1 5 compound:vo	color:blue
1	打	_	VERB	_	_	0	root	_	hit
2	了	_	AUX	_	_	1	aux	_	PERF
3	幾	_	DET	_	_	4	det	_	several
4	次	_	NOUN	_	_	1	advmod:df	_	CL:times
5	針	_	NOUN	_	_	1	compound:vo	_	needle

1	"have	_	_	_	_	0	_	_	_
2	gotten/given	_	_	_	_	0	_	_	_
3	an	_	_	_	_	0	_	_	_
4	injection	_	_	_	_	0	_	_	_
5	several	_	_	_	_	0	_	_	_
6	times"	_	_	_	_	0	_	_	_

~~~

When undergoing verb-verb compounding (see [compound:vv]()), it is the verb in the verb-object compound that undergoes the compounding, rather than the entire verb-object unit, resulting in a VVO order instead of a VOV order:

~~~ conllu
# visual-style 2 4 compound:vo	color:blue
1	我	_	PRON	_	_	2	nsubj	_	1SG
2	讀	_	VERB	_	_	0	root	_	read
3	完	_	VERB	_	_	2	compound:vv	_	finish
4	書	_	NOUN	_	_	2	compound:vo	_	book
5	了	_	PART	_	_	2	discourse:sp	_	SP

1	"I've	_	_	_	_	0	_	_	_
2	finished	_	_	_	_	0	_	_	_
3	studying."	_	_	_	_	0	_	_	_

~~~

Additionally, the object in a verb-object compound may be modified (by an adjective or possessive), and also fronted to topic position (in which case the object is linked to the verb as a [dislocated:vo]() dependent):

~~~ conllu
# visual-style 5 3 dislocated:vo	color:blue
1	你	_	PRON	_	_	3	nmod	_	2SG
2	的	_	PART	_	_	1	case	_	GEN
3	電話	_	NOUN	_	_	5	dislocated:vo	_	phone
4	怎麼	_	ADV	_	_	5	advmod	_	how
5	打	_	VERB	_	_	7	advcl	_	hit
6	都	_	ADV	_	_	7	advmod	_	still
7	沒	_	VERB	_	_	0	root	_	not-exist
8	人	_	NOUN	_	_	7	obj	_	people
9	接	_	VERB	_	_	8	acl	_	receive

1	"You're	_	_	_	_	0	_	_	_
2	phone,	_	_	_	_	0	_	_	_
3	no	_	_	_	_	0	_	_	_
4	matter	_	_	_	_	0	_	_	_
5	how	_	_	_	_	0	_	_	_
6	one	_	_	_	_	0	_	_	_
7	calls	_	_	_	_	0	_	_	_
8	it,	_	_	_	_	0	_	_	_
9	nobody	_	_	_	_	0	_	_	_
10	picks	_	_	_	_	0	_	_	_
11	it	_	_	_	_	0	_	_	_
12	up."	_	_	_	_	0	_	_	_

~~~

Note that when both the verb and the object are monosyllabic and they are adjacent without intervening material, they are treated as a single word in the tokenization stage.
