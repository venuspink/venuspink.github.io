---
layout: post
title: 모델 간 관계설정
category: Django
tags: [django,model,relationships]
comments: true
---

장고의 모델은 ORM을 아주 잘 구현하고 있다.

쉽고 정확하다.

다음 코드는 고양이 클래스에 주인 속성을 선언한 것이다.

```python
class Cat(models.Model):
	name = models.CharField(max_length=30)
	owner = models.ForignKey(Owner, null=True)
    
nicolas = Owner.objects.get(pk=1)    
bunns = Cat.objects.get(id=2)
bunns.owner = nicolas
bunns.save()
```



foreign key는 주인 모델을 향하고, 주인 모델은 새로운 속성을 갖게된다. 그 이름은 cat_set 의 형태로 구성된다.

```Python
nicolas = Owner.objects.get(pk=1)
nico_cats = nicolas.cat_set.all() #cat_set은 정의되어 있지 않지만 foreign key에 의해 자동 생성
```

cat_set은 nicolas가 가지고 있는 모든 고양이 목록이다.

###ManyToMany

```python
class Owner(models.Model):
	following = models.ManyToManyField('self')
	followers = models.ManyToManyField('self')
    
jisu = Owner.objects.get(pk=2)
pedro = Owner.objects.get(pk=3)
nicolas.follwers.add(jisu, pedro)    
```

