# Analysis Using Hive Regex Serde modules of a Stackerflow website page
This project uses Hive managed and external tables on HDFS space and is a analysis of the stackoverflow website and uses its input directly as the html page.Concept of regular expressions is implemented using RegexSerde modules present in added jars from another location and is thus used in filling the managed and external tables.

Dataset's description :
The purpose of this assignment is to calculate some statistics of the stackoverflow.com website.

The input dataset contains two parts: users and posts (questions and answers) from StackOverflow site. Posts are in XML format, but it doesn't matter: you can interpret it as a text of independent lines, one post per each line.
While making the project page at https://stackoverflow.com/questions/11/calculate-relative-time-in-c-sharp was used as dataset.

The valid row contains the following fields and their order is not defined in the page specified as dataset : 

         * Id (integer) - id of the post
    		 * PostTypeId (integer: 1 or 2) - 1 for questions, 2 for answers
    		 * CreationDate (date) - post creation date in the format "YYYY-MM-DDTHH:MM:SS.ms"
    		 * Tags (string, optional) - list of post tags, each tag is wrapped with html entities '&lt;' and '&gt;'
    		 * OwnerUserId (integer, optional) - user id of the post's author
    		 * ParentId (integer, optional) - for answers - id of the question
    		 * Score (integer) - score (votes) of a question or an answer, can be negative (!)
    		 * FavoriteCount (integer, optional) - how many times the question was added in the favorites
 Various other tables are then generated and several hql queries are run on them to obtain desired analysis conclusions.
