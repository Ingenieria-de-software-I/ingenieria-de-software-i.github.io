# ingenieria-de-software-i.github.io
Sitio web del curso Leveroni de Ingenieria de Software I

## Cómo correr localmente
Podés ver una explicación en video de este readme [aquí](https://youtu.be/cNCuhskP_Ks)
Para correr la página necesitás [Git](https://git-scm.com/downloads) y [Ruby](https://www.ruby-lang.org/es/downloads/) instalados en tu computadora. Una vez que cumplas esos requisitos debés seguir los siguientes pasos:

```
# Primero instalamos jekill
gem install jekyll bundler

# Luego nos paramos sobre la carpeta de la página web
cd ingenieria-de-software-i.github.io

# Luego instalamos y corremos localmente la página. --livereload nos permite ver los cambios en vivo.
bundle install
bundle exec jekyll serve --livereload
```

Podés encontrar más información en la página de Jekyll.

## Cómo actualizar la página web
Github automáticamente actualiza la página web cuando recibe un nuevo commit. Con pushear tus cambios a la rama main alcanza para actualizar la página web, luego de unos minutos podrás ver los cambios. 
