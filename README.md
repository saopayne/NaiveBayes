Naive Bayes :)


Setting up the database for storage
    '''
    To test  here, A mysql db is needed to store which can be done with
    :) Compatible with the any mysql client, tested on Linux ubuntu 13.10
    with love from Nigeria.

    create database bayes;
    create table word(word varchar(75), doctype varchar(75), count int);
    create table doctype_count(doctype varchar(75), count int);

    create index i1 on word(word, doctype);

    delete from word;
    update doctype_count set count = 0;

    '''


Training

  
To train the utility, use the following command:

    python bayes.py learn <doctype> <file> <count>

e.g.

    python bayes.py learn spam ../train/spam0.txt 10
    python bayes.py learn ham ../train/ham10.txt 10

Classify



    bayes.py classify <file> <doctype> <doctype>
e.g. 

    python bayes.py classify ../train/sampletext.txt spam ham
    > Probability that document is spam rather than ham is 1.00
