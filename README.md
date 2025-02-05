# Работа по StyleCLIP и StyleGAN-NADA

В репозитории представлен [обзор](https://github.com/Bravi-study/stylegan_nada/blob/main/review.ipynb) научных работ по [StyleCLIP](https://arxiv.org/abs/2103.17249) и [StyleGAN-NADA](https://arxiv.org/abs/2108.00946),  
а также реализация последней в [StyleGAN_NADA.ipynb](https://github.com/Bravi-study/stylegan_nada/blob/main/StyleGAN_NADA.ipynb)

Предложенные в них методы позволяют направлять обучение StyleGAN в сторону, задаваемую текстом. 

Веса, использованные в работе и не только, доступны по ссылкам:
- Добавление очков (MetFaces): [painting_sunglasses_trained_generator.pt](https://www.dropbox.com/scl/fi/f27ay2kzleyxsg02xbo3g/painting_sunglasses_trained_generator.pt?rlkey=0e6s16xsde9ubfplys3fuc66x&dl=1)
- Аниме: [photo_anime_trained_generator.pt](https://www.dropbox.com/scl/fi/aw22wdwe402upob0teo54/photo_anime_trained_generator.pt?rlkey=zzg11fh6s6rlyk9hn1tmoykoi&dl=1)
- Борода и усы: [photo_beard_and_mustache_trained_generator.pt](https://www.dropbox.com/scl/fi/fvw8behwldox64hwlx3tv/photo_beard_and_mustache_trained_generator.pt?rlkey=fy44023kicu9u17av0zbpyzf4&dl=1)
- Классицизм: [photo_classicism_portrait_trained_generator.pt](https://www.dropbox.com/scl/fi/is9mb8tk9uc3xw7d64wuo/photo_classicism_portrait_trained_generator.pt?rlkey=hlraml2tl0z9dpcvuvyijj494&dl=1)
- Кубизм: [photo_cubism_trained_generator.pt](https://www.dropbox.com/scl/fi/h6ddyfdjcytzrpb4ajp7t/photo_cubism_trained_generator.pt?rlkey=8p9zf6wapz6e6u8ean6l37kkv&dl=1)
- Импрессионизм: [photo_impressionist_portrait_trained_generator.pt](https://www.dropbox.com/scl/fi/orx321kx53umcgwctm80a/photo_impressionist_portrait_trained_generator.pt?rlkey=92kzpq7x3gkrnp23wamnwhyve&dl=1)
- Масляные краски: [photo_oil_painting_trained_generator.pt](https://www.dropbox.com/scl/fi/1dovh7u7uo2lla6xxdxbw/photo_oil_painting_trained_generator.pt?rlkey=xf6z5q8anmhr7dnx8an5op489&dl=1)
- Панк: [photo_punk_style_trained_generator.pt](https://www.dropbox.com/scl/fi/nnmilhg59gajos37o6s6q/photo_punk_style_trained_generator.pt?rlkey=uts7evkbsy2qm86vjhi9wxvix&dl=1)
- Рембрандт: [photo_rembrandt_trained_generator.pt](https://www.dropbox.com/scl/fi/cidiv1brgzqstfzt2y5e8/photo_rembrandt_trained_generator.pt?rlkey=mgv2ft3ks0jne03hnxh6copto&dl=1)
- Шрек: [photo_shrek_trained_generator.pt](https://www.dropbox.com/scl/fi/06wjezmnfjlqfabgg6vg6/photo_shrek_trained_generator.pt?rlkey=uw8t9999wg2gq1mbq44hmliuk&dl=1)

Использование:
```
checkpoint = torch.load(checkpoint_path, map_location=device, weights_only=False)
stylegan_generator.load_state_dict(checkpoint["generator_state_dict"])
```

## Генерация

- Пример изображений, созданных в стиле кубизма:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/cubism_generated.png" height="400"/>

- Аниме:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/anime_generated.png" height="400"/>

### До и После стилизации

- Солнцезащитные очки, мода эпохи Папы Бенедикта XIII:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/sunglasses_generated.png" height="400"/>

- Импрессионизм:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/impressionism_comparison.png" height="400"/>

- Портрет масляными красками:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/oil_comparison.png" height="400"/>

- Аниме:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/anime_comparison.png" height="400"/>

## Редактирование

- Исходное изображение:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/input_img.jpg" width="300" height="300"/>

- Редактированное изображение, кубизм:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/cubism.png" width="300" height="300"/>

- Добавление бороды и усов:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/beard.png" width="300" height="300"/>

- Портрет:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/painting.png" width="300" height="300"/>

- Аниме:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/anime.png" width="300" height="300"/>

- Импрессионизм:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/impressionism.png" width="300" height="300"/>

- Масляные краски:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/oil.png" width="300" height="300"/>

- В стиле Рембрандта:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/rembrandt.png" width="300" height="300"/>

- И достопочтенный образ в очках:
<img src="https://github.com/Bravi-study/stylegan_nada/blob/main/images/sunglasses.png" width="300" height="300"/>
