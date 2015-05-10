# NaiveBayes
This is an implementation of the popular naive bayes algorithm in python.


To test::

1. SETTING UP THE DATABASE;

  '''
  To test  here, A mysql db is needed to store which can be done with
  :) Compatible with the any mysql client, tested on Linux ubuntu 13.10
  with love from Nigeria.

  - create database bayes;
  - create table word(word varchar(75), doctype varchar(75), count int);
  - create table doctype_count(doctype varchar(75), count int);
  - create index i1 on word(word, doctype);
  - delete from word;
  - update doctype_count set count = 0;

'''

2. TRAINING THE ALGORITHM

   python bayes.py learn "doctype" "file" "count"

   e.g.  - python bayes.py learn spam spam0.txt  1
   
        - python bayes.py learn ham ham10.txt  2

3. CLASSIFY A FILE

   - python bayes.py classify "file" "doctype" "doctype" 
   
   - python bayes.py classify sampletest.txt spam ham
   
    >> Probability that document is spam rather than ham is 0.90
