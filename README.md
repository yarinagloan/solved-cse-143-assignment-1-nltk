Download Link: https://assignmentchef.com/product/solved-cse-143-assignment-1-nltk
<br>



<h1>1           Getting Started with NLTK</h1>

Before going further you should install NLTK 3.0, downloadable for free from <a href="http://www.nltk.org/install.html">http://www.nltk.org/ </a><a href="http://www.nltk.org/install.html">install.html</a><a href="http://www.nltk.org/install.html">.</a> Follow the instructions there to download the appropriate version for your platform. In this course we will use Python 3.7 <em>ONLY</em>, so you <strong>MUST </strong>download that version. Also, you <strong>MUST </strong>download NumPy – this is not optional as the website says.

(<em>Note: Macs with Yosemite or higher have Python 2.7 as default in the terminal. You will need to run</em>

<em>“</em>sudo pip3 install -U nltk<em>” instead of “</em>sudo pip install -U nltk<em>” in order to install NLTK for Python 3.7. You should make a separate installation rather than updating/replacing your system default Python version.</em>)

Once you’ve installed NLTK, start up the Python interpreter:

<ul>

 <li>Windows: find and open “Python 3.7 (command line – 32bit)” in your start menu.</li>

 <li>Mac: type “python3” and press enter in your terminal.</li>

</ul>

Install the data required for the book by typing the following two commands at the Python prompt, then selecting the ”book” collection as shown in Figure 1 and pressing ”Download”.

Figure 1: Installing NLTK data.

<h1>2           Working with Corpora</h1>

In this assignment you will write a program to analyze two different narrative corpora and compare them. The first corpora is a collection of 25 Aesop’s fables. The second corpus is a collection of 11 personal narratives told by ordinary people on their weblogs. Both corpora are provided as zip archives with each individual file containing a different fable or blog.

Your program should take one command line argument that specifies which corpus you are going to analyze (<strong>fables </strong>or <strong>blogs</strong>). The input file for the fables corpus is the zip archive containing the 26 fables as text (<strong>fables.zip</strong>). The input for the blogs corpus is the zip archive containing the 12 blogs as text

(<strong>blogs.zip</strong>). Use the stub code assignment1-stub-s15.py to get started. For each of the corpora your program should do the following:

<ol>

 <li>Tokenization

  <ul>

   <li>Write the name of the corpus to stdout.</li>

   <li>Delimit the sentences for each document in the corpus. (c) Tokenize the words in each sentence of each document.</li>

  </ul></li>

</ol>

(d) Count the number of total words in the corpus and write the result to stdout.

<ol start="2">

 <li>Part-of-Speech

  <ul>

   <li>Apply the default part-of-speech tagger to each tokenized sentence.</li>

   <li>Write a file named CORPUS NAME-pos.txt that has each part-of-speech tagged sentence on a separate line and a blank newline separating documents. Where CORPUS NAME is either fables or blogs. The format of the tagging should be a word-tag pair with a / in between. For example:</li>

  </ul></li>

</ol>

The/DT boy/NN jumped/VBD ./.

<ol start="3">

 <li>Frequency

  <ul>

   <li>Write the vocabulary size of corpus to stdout. Please note that you should use the <strong>lowercased word</strong>.</li>

   <li>Write the most frequent part-of-speech tag and its frequency to the stdout.</li>

   <li>Write down the top 10 most frequent part-of-speech tags in the corpus with their frequency and relative frequency to the stdout in a decreasing order of frequency. Relative frequency should be rounded to 3 digits and can be computed by dividing the frequency by the total number of tokens in the corpus.</li>

   <li>Find the frequency of each unique word (after <strong>lowercasing</strong>) using the FreqDist module and write the list in <strong>decreasing order </strong>to a file named CORPUS NAME-word-freq.txt.</li>

   <li>Find the frequency of each word given its part-of-speech tag. Use a conditional frequency distribution for this (CondFreqDist) where the first item in the pair is the part-of-speech and the second item is the <strong>lowercased word</strong>. Note, the part-of-speech tagger requires uppercase words and returns the word/tag pair in the inverse order of what we are asking here. Use the tabulate() method of the CondFreqDist class to write the results to a file named CORPUS NAME-pos-word-freq.txt.</li>

  </ul></li>

 <li>Similar Words

  <ul>

   <li>For the most frequent word in the <strong>NN </strong>(nouns), <strong>VBD </strong>(past-tense verbs), <strong>JJ </strong>(adjectives) and <strong>RB </strong>(adverbs) part-of-speech tags, find the most similar words using similar(). Write the output to stdout (this will happen by default).</li>

  </ul></li>

 <li>Collocations

  <ul>

   <li>Write the collocations to the stdout.</li>

  </ul></li>

</ol>

<h1>3           Output Results</h1>

In conclusion, if you follow the steps in Section 2, your program should output the following information in standard output for each corpus:

<ol>

 <li>Corpus name:</li>

 <li>Total words in the corpus:</li>

 <li>Vocabulary size of the corpus:</li>

 <li>The most frequent part-of-speech tag is  with frequency</li>

 <li>Frequencies and relative frequencies of all part-of-speech tags in the corpus in decreasing order of frequency are: tag has frequency and relative frequency .</li>

 <li>The most frequent word in the POS (NN/VBD/JJ/RB, note that you need to output result for each of these POS) is and its similar words are:</li>

 <li>Collocations:</li>

</ol>

Your python program should also <strong>output three files for each corpus</strong>. For example, for fables corpus, it should output fables-pos.txt, fables-word-freq.txt and fables-pos-word-freq.txt.