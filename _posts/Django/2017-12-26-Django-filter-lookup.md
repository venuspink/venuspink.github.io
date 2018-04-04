---
layout: post
title: filter() lookups 요소
category: Django
tags: [django,filter,lookups]
comments: true
---

코딩하면서 가장 궁금했던 부분. 어떤 코딩컨벤션이 있을거라 생각했는데 , 생각보다 기능이 다양하다.

```python
#blog 모델의 헤드라인이 test를 포함한 것
Entry.objects.filter(blog__headline__contains='test')

#blog모델이 갖고있는 author모델이 낫널, 
#그리고 author모델의 name필드가 null 인 것. 모두 만족해야 함.
Entry.objects.filter(blog__authors__isnull=False, blog__authors__name__isnull=True)

모델 이름을 소문자로 쓴다.
```

lookups 에 다음과 같은 주요 정의 된 함수가 있다.

exact, iexact(앞에 i가 붙으면 대소문자 구분하지 않음), contains, in, gt, gte, lt, lte, startswith, istartswith,

Endswith, range, date, year, month, day, week, week_day, quarter, hour, time, second, is null, regex 등.

[장고문서참조](https://docs.djangoproject.com/en/2.0/ref/models/querysets/#field-lookups)



