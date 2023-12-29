
- Превью: https://kseylo.github.io/testimonials-grid-section/
## Установка:

Установка зависимостей
```
pnpm install
```

Запуск
```
pnpm dev
```

## Скриншоты:
### ПК:
![desktop](screenshots/desktop.jpeg)
### Планшет:
![tablet](screenshots/tablet.jpeg)
### Телефон:
![mobile](screenshots/phone.jpeg)
## Технологии которые использовал:
- HTML
- SASS

## Проблемы с которыми столкнулся:
- Как стилизовать каждую карточку индивидуально используя sass
  Решение к которому я пришел:
```html
<!-- Добавлять к каждому div какой-то уникальный div -->
<div class="card card--violet">  
</div>  
<div class="card card--grayish">  
</div>  
<div class="card card--white">  
</div>  
<div class="card card--blackish">  
</div>  
<div class="card card--white">  
</div>
```
SASS:
```scss
.card {  
    border-radius: 0.5rem;  
    padding: 2rem;  
    display: grid;  
    gap: 1rem;  
    // card__avatar
    &__avatar {  
        width: 2.5rem;  
        height: 2.5rem;  
        border-radius: 50%;  
    }  
    
    // Violet
    // card--violet  
    &--violet {  
        background: $moderate-violet;  
        background-image: url('assets/images/bg-pattern-quotation.svg');  
        background-position-x: 90%;  
        background-repeat: no-repeat;
        
        .card__avatar {  
            border: 0.2rem solid lighten($moderate-violet, 10%);  
        }  
    }  

}
```