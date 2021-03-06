---
layout: post
title: Menangani Salah Ketik di Chatbot Bahasa Indonesia
date: 2018-3-2
published: false
---
Typo simply called as misspelling.
Kesalahan ketik (_typing error_ atau _typo_) dan kesalahan ejaan (_spelling error_)
secara sederhana disebut _spelling error_. [1]

While that the chatbot is combining messaging and AI.
Selama diketahui chatbot [kombinasi]({% post_url 2018-2-27-Mekanisme-Chatbot %}) antara
pesan instan dan kecerdasan buatan.

Many people take less care the right spell of a word these day. (Sapul, 2016).
Pengaruh teknologi teks seperti layanan IM [_Instant Messaging_] dan jejaring sosial
membuat banyak orang cenderung melupakan bentuk yang tepat dari sebuah kata.
Dan banyak orang menaruh sedikit perhatian kepada ejaan yang benar. [2]

There will be another rule on chatbot to handle any misspelling case. (Nawaf Ali, 2014: 13).
> Chat bots responses are coming from artificially intelligent knowledge base that has rules,
so the chance for a chat bot to present a misspelled word is close to none,
unless the chat bot programmer did add them intentionally (Nawaf Ali, 2014: 13).

Since not pretend to be human (Tiwari et al, 2017).

The correct word can same misused as misspelled.

To detect spelling case in Indonesian word by using Soundex.
It will keep the first letter, so the mistaken of the word depend on first letter.
Contradict to Kukich statement, while few error from the first letter.

Just handle some like  
tjuan  
tjn  
Could be known as tujuan.

The Soundex can achieved by the use of sql query. It has implemented as function. Soundex() different with sounds like query.

The result from Soundex string given still need to
String similarity measurement
Measure the similarity of word or string

the smallest distance the correct word is. Still word dictionary based. The challenge to time access and  more on less space.

Note that it just not wise if the mistaken word can be considered as one distance but then create or save any record only for it.
Credit to split row https://stackoverflow.com/a/19073575/5315239  
Can also limit the distancing as 1 distance.

Since 80% can be handled allowing one operation of four: they are deletion, insertion, replacement and transposition.
While transposition is on interest. Using only classical Levenshtein distance, it not considering transposition as 1 operation.

Damerau-Levenshtein distance knowing transposition as 1. May still the Damerau-Levenshtein not support triangle equality.

Although on a research Jaro-Winkler take being the better. Since chatbot is about natural language.

As Wikipedia says here on Damerau-Levenshtein topic.
Damerau-Levenshtein plays an important role on natural language. In natural language string are short and the number misspelling rarely exceed 2.

Bhatti _et al_. (2012). Spelling Error Trends and Patterns in Sindhi.

Min _et al_. (2000). Typographical and Orthographical Spelling Error Correction.

van Berkel, Brigitte & Koenraad De Smedt. (1988). Triphone Analysis: A Combined Method For The Correction Of ORTHOGRAPHICAL and TYPOGRAPHICAL Errors. Proc. of the Second Conference on Applied Natural Language Processing, Austin TX, 9-12 Feb. 1988 (pp. 77-83).

Kukich, Karen. (1992). Techniques for Automatically Correcting Words in Text. ACM Computing Surveys, Vol. 24, No. 4, December 1992.

OMID KASHEFI, MOHSEN SHARIFI and BEHROOZ MINAIE (2013). A novel string distance metric for ranking Persian respelling suggestions. Natural Language Engineering, 19, pp 259-284