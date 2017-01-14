#Named entity disambiguation for questions in CQA
This corpus may be used by researchers who are interested in the task of NED in CQA.
It contains four files, two xml files for the labeled data and
two text files for examples of mention-candidate dictionaries.</br>

1. NED_labels_Wikipedia.xml</br>
This file contains 1,686 human labeled English questions. The questions were crawled from Yahoo! Answers,
and entity mentions in questions are mapped to entries in Wikipedia. The format is the
following:</br>
  - Each question is stored inside a "\<question\>" XML element.</br>
  - The subject of each question is stored inside a "\<title\>" element.</br>
  - Each question may have an optional "\<detail\>" element, which contains additional detail about the question.<br>
  - The leaf category information of each question is stored inside a "\<category\>" element.</br>
  - The top 5 answers posted for this question are given to help understanding the ambiguous entities,
  and each answer is stored inside the "\<answer\>" element.</br>
  - Each labeled mention is stored inside a "\<mention\>" element. Element "\<name\>" stores the mention name,
  and element "\<KBEntry\>" stores the referent entity's entry in the knowledge base.</br>

2. NED_labels_BaiduBaike.xml</br>
This file contains 5,101 human labeled Chinese questions. The questions were crawled from Baidu Knows,
and entity mentions in questions are mapped to entries in Baidu Baike. The format is the same as the above xml file.</br>

3. MentionCandidates_Wikipedia.txt</br>
To recognize entity mentions and associate them with entity candidates in Wikipedia, we built an English mention-candidate
dictionary from a Wikipedia dump on May 3, 2013. This file contains some examples of the dictionary.
Each line is a mention-candidate map. The entity candidate is represented by its entry in Wikipedia.</br>
The data format is: \<mention\>\t\<entity candidate's KB entry\>

4. MentionCandidates_BaiduBaike.txt</br>
This file contains some examples of the Chinese mention-candidate dictionary. The format is the same as "MentionCandidates_Wikipedia.txt"
