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
https://www.evernote.com/l/AGD08pwCwxFPlbxmVpOu90cK3LGG7ggDrL4
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
        Method : GET
     4- Downvote answer
        localhost:8080/post/<question_id>/ans/<answer_id>/downvote
        Method : GET
        
   # LLD Diagram / Class Diagram
   ![image of Class Diagram](https://user-images.githubusercontent.com/20575442/123557178-0e0d5180-d7ad-11eb-9c9f-833ab2c2d665.png)
