---
layout: post
title: Migrating , 슈퍼유저 생성
category: Django
tags: [django,migration]
comments: true
---

 ```
$ python manage.py makemigrations
$ python manage.py migrate
 ```

모델의 필드를 추가하거나 수정했을 경우 위와 같이 마이그레이션을 실행한다.



## 슈퍼유저 생성

```
$ python manage.py createsuperuser
```



http://localhost:8000/admin

이미 빌트된 어드민 패널이 존재한다. 