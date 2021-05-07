# graphql-introduction

## 参考記事
https://dev.classmethod.jp/articles/graphql-tutorial-nodejsexpress/
https://medium.com/codingthesmartway-com-blog/creating-a-graphql-server-with-node-js-and-express-f6dddc5320e1

## getSingleCourse
### クエリ
```
query getSingleCourse($courseID: Int!) {
 course(id: $courseID) {
  title
  author
  description
  topic
  url
 }
}
```

### クエリ変数
```
{ 
 "courseID":1
}

```

## getCourses
### クエリ
```
query getCourses($topic: String!) {
 courses(topic: $topic) {
  title
  url
 }
}
```

### クエリ変数
```
{ 
 "topic":"Node.js"
}
```

## updateCourseTopic
### クエリ
```
mutation updateCourseTopic($id: Int!, $topic: String!) {
  updateCourseTopic(id: $id, topic: $topic) {
    title
    author
    description
    topic
    url
  }
}
```

### クエリ変数
```
{
 "id": 1,
 "topic": "トピックタイトル"
}
```
