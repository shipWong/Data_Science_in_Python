# Hacker News Posts — the Best Post Submission Times that You Need to Know

## Introduction
In this project, we analyse a [modified dataset](https://dq-content.s3.amazonaws.com/356/hacker_news.csv) of post submissions to [Hacker News](https://news.ycombinator.com/) (abbreviated as HN). Hacker News is a social news website started by incubator [Y Combinator](https://en.wikipedia.org/wiki/Y_Combinator) with a focus on technology and entrepreneurship. The original dataset can be found [here](https://www.kaggle.com/datasets/hacker-news/hacker-news-posts).

On Hacker News, users can upvote or downvote posts — this eventually contribute to the number of points the posts receive. The higher the number of points a post obtain, the greater its approval rate. The number of points is calculated as below:

```
num_points = the total number of upvotes - the total number of downvotes
```

There are three types of posts on Hacker News:
- `Ask HN`: The posts for **asking** Hacker News community questions.
- `Show HN`: The posts for **sharing** with the community a project, product, or just generally something interesting.
- Other posts

The column descriptions of the dataset are as below:

- `id`: The unique identifier for the post
- `title`: The post title
- `url`: The URL that the posts link to (if the post has a URL)
- `num_points`: The number of points the post obtained
- `num_comments`: The number of comments received by a post
- `author`: The username of the person who submitted the post
- `created_at`: The date and time at which the post was submitted (timezone - Eastern Time in the US)

### The goal of the project
Our main interests are analysing the posts with titles starting with `Ask HN` and `Show HN`. 

The project aims to answer these questions:
- What type of post receive more comments on average?
- What is the submission time that posts attract more comments on average?
- What type of post obtain more points (higher approval rate) on average?
- What is the publishing time that posts earn more points on average?

### Summary of the results
- **`Ask HN`** posts receive **more comments** on average. Their prime submission times are:
    - **15:00 - 16:00 EDT** (or 21:00 - 22:00 CEST)
    - **2:00 - 3:00 EDT** (or 8:00 - 9:00 CEST)
    - **20:00 - 21:00 EDT** (or 2:00 - 3:00 CEST)

- **`Show HN`** obtain a **higher approval rate** on average. Their best publishing time blocks are:
    - **22:00 - 1:00 EDT** (or 4:00 - 7:00 CEST)
    - **11:00 - 13:00 EDT** (or 17:00 - 18:00 CEST)

- Both `Ask HN` and `Show HN` demonstrate distinct peak times for acquiring a high number of comments and points, respectively.

- We deduce that most responders are from the US timezone or countries in the nearer timezones.

Note:
- EDT : Eastern Daylight Time
- CEST : Central European Summer Time
