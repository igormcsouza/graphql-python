# GraphQL with Python

Lately I decided to study a little more about graphql just on curiosity. Well,
I just fall in love for it! So much I decided to try implement it.

## Learn GraphQL-Graphene

I watched two amazing videos on how to use it with python (Django). I'm going to
list the links below. I also use the **Graphene** (below) which is the package
to use GraphQL on python in general, but it also has an pluguin for Django. I'll
put a Talk from a guy talking about GraphQL and Graphene for Django.

- [GraphQL with Django - Intro, Install and first query](https://www.youtube.com/watch?v=kP7wQoFXUSc)
- [GraphQL Python Tutorial With Graphene (+ Django Integration)](https://www.youtube.com/watch?v=-0uxxht4mko)
- [Graphene](https://graphene-python.org/)
- [[PyBR14] Apresentando graphene uma lib graphql para o django - Ciro Valente Filho](https://www.youtube.com/watch?v=S8egx3NS8sQ)

## Test Cookbok

I followed [this](https://docs.graphene-python.org/projects/django/en/latest/tutorial-plain/)
basic tutorial just to get the first impressions.. Well It is very interesting
then...

## How to make requests

I tested using **insomnia** and it worked with 3 ways: post graphql, post and
get. They all return the answer you expected.

1. Post GraphQL

Link:

```
http://host/graphql
```

GraphQL Body:

```
query {
  allIngredients {
    id
    name
  }
}
```

2. Post

Link:

```
http://host/graphql
```

JSON Body:

```
{
  "query": "{allIngredients{id,name}}"
}
```

3. Get

Link:

```
http://host/graphql?query={allIngredients{id,name}}
```

## Run this guy

I'm using poetry to deal with environment. Install poetry from **pip** and run
the command `poetry install` to have all the packages installed.

I followed the documentation fron graphene. It uses Django for api. Run the
server by running the command below.

```
python manage.py runserver
```
