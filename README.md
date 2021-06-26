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
    # View all post (all questions with tag)
      localhost:8080/post
    # View by question id or title
      localhost:8080/post/<question_id>/ans
      localhost:8080/post/<title>/ans
    # Upvote answer/question
      localhost:8080/post/<question_id>/ans/<answer_id>/upvote
      localhost:8080/post/<question_id>/ques/upvote
    # Down vote question/answer
      localhost:8080/post/<question_id>/ans/<answer_id>/downvote
      localhost:8080/post/<question_id>/ques/downvote
    # View user id dashboard
      localhost:8080/user/<user_id>
    # Send notification [search in db who all are associated with eventId and notify them]
      localhost:8080/notification/event_id
