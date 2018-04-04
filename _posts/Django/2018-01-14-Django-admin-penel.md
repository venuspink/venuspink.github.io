---
layout: post
title: 장고 어드민 설정
category: Django
tags: [django,model,admin]
comments: true
---

장고의 관리자 화면은 강력하다. 따로 관리자 페이지를 만들지 않아도 모델 기반으로 알아서 생성해주며 커스터마이징도 가능하다.

[장고 어드민 문서 참조](https://docs.djangoproject.com/en/2.0/ref/contrib/admin/)

해당 app의 admin.py에 다음과 같이 정의하면 된다.(커스터마이징)

```python
@admin.register(models.Image)
class ImageAdmin(admin.ModelAdmin):
    list_display_links = (
        'location',
    )

    search_fields = (
        'location',
        'caption',
    )

    list_filter = (
        'location',
        'creator',
    )

    list_display = (
        'file',
        'location',
        'caption',
        'creator',
        'created_at',
        'updated_at',
    )

@admin.register(models.Like)
class LikeAdmin(admin.ModelAdmin):
    list_display = (
        'creator',
        'image',
        'created_at',
        'updated_at',
    )

@admin.register(models.Comment)
class CommentAdmin(admin.ModelAdmin):
    list_display = (
        'message',
        'creator',
        'image',
        'created_at',
        'updated_at',
    )
```



