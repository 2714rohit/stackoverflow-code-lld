# stackoverflow-code-lld
https://stackoverflow.com/users/9093208/rohit-maurya

# Requirements
    1- Post questions and add Category / Tag
    2- Search based on title, tag or question id
    3- Add answers to questions
    4- Upvote and Downvote to questions and answers
    5- View users dashboard [earned badges]
    6- Send notification to the user 1, if any other user add commente/upvote/downvote/answer to the user 1 activity

# API Details
  # GET Methods
    1- View all post (all questions with tag)
       localhost:8080/post
    2- View by question id or title
       localhost:8080/post/<question_id>/ans
       localhost:8080/post/<title>/ans
    3- Upvote answer/question
       localhost:8080/post/<question_id>/ans/<answer_id>/upvote
       localhost:8080/post/<question_id>/ques/upvote
    4- Down vote question/answer
       localhost:8080/post/<question_id>/ans/<answer_id>/downvote
       localhost:8080/post/<question_id>/ques/downvote
    5- View user id dashboard
       localhost:8080/user/<user_id>
    6- Send notification [search in db who all are associated with eventId and notify them]
       localhost:8080/notification/event_id
  # Post Methods
    1- Add new question
       localhost:8080/user/<user_id>
       Method POST

       Request body:

       {
       "question": "How to learn to code lld in Java",
       "tags": [
               {
                "tagName": "Java"
                }
       ]
       }
     2- Add new answer for question id <question_id>
        localhost:8080/post/<question_id>

        Method :POST


        Request Body
        {
        "answer": "If you learn Design Pattern, you can learn how to code lld in any language"
     3- Upvote answer
        localhost:8080/post/<question_id>/ans/<answer_id>/upvote
        Method : POST
     4- Downvote answer
        localhost:8080/post/<question_id>/ans/<answer_id>/downvote
        Method : POST
        
   # LLD Diagram / Class Diagram
   ![image](https://user-images.githubusercontent.com/20575442/123557934-4747c080-d7b1-11eb-891b-84a40603b3db.png)

   # Database table design
   *User_Table* : user_id, name, email_id, designation, reputation, badge_id
   
   *Question_Table* : qes_id, description, title, user_id, TimeStamp, total_vote_count
   
                      total_vote_count => it will help to fetch all vote for a particular question, helps to reduce query
                      
   *Answer_Table* : asn_id, description, user_id, event_id, event_type, TimeStamp, total_vote_count
   
                    event_id => comment on answer/question or Answer for question
                    event_type => comment or answer
                    ans_Id : use same table for both comment as well as Answer
                 
   *Badge_Table* : badge_id, type
   
                    in this table badge_id and type both together will be PK, the reason of having both togehter as key is one user
                    may achive multiple badges
