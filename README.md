# Gtree-д тавтай морил
Gtree бол Монголын гитар сонирхогчдын нээлттэй бүлгэм ба бидний сайт болох gtree.mn гитар таб, кордын нэгдсэн сан бүрдүүлэх зорилготойгоор энд нээлттэй хөгжүүлэгдэж байна. Нээлттэй учир та ч гэсэн бидэнтэй нэгдэж, хамт хөгжүүлэлцэж болно шүү.

Сайт нь social механизмыг ашиглан хэн ч нээлттэйгээр хүссэн гитар таб, кордоо оруулах, түүнийгээ түгээх, найз нөхөдтэйгөө нийлж нөгжүүлэх, үүсгэх, засварлах гэх зэрэг боломжуудаар хангахыг зорьж байна.

# Ашигласан системүүд
* Ruby (programming language) - http://wiki.limnux.net/wiki/Ruby
* Ruby on Rails (web app framework on ruby) - http://wiki.limnux.net/wiki/Ruby_on_Rails
* Mongrel (server)
* MySQL (database)
* Blueprint (CSS framework)

# Github-тай холбох
Github-ын талаар монгол хэл дээрх гарын авлагыг http://wiki.limnux.net/wiki/Github хаягаас авна уу.
Энэ системийг өөрийн сервер, үгүй бол тооцоолуур дээрээ ажиллуулахын тулд эхлээд энэ github/gtree агуулгаа тооцоолууртаа холбох хэрэгтэй. Ингэхийн тулд Github-ын гарын авлагын дагуу энэ агуулгыг fork хийнэ. Түүнийхээ дараа terminal нээгээд:
 $ mkdir gtree
 $ cd gtree
 $ git init
 $ git remote add origin git@github.com:user_name/gtree.git
 $ git pull origin master
Ийнхүү зөв холбосон бол ls тушаалын үр дүнд агуулах харагдах ёстой. Ингээд ажиллуулах алхамыг хийцгээе.

# Ажиллуулах
Ажиллуулахын тулд танд юуны түрүүнд дээрх Ашигласан системүүд сэдэв доторх бүх системүүд таны тооцоолуурт суусан байх шаардлагатай ба дараах алхмуудыг хийж хөрсийг бэлдэнэ.

* Хэрэгцээт програмуудыг суулгах, хэрвээ суучихсан програм бол хэрэггүй. Мөн Ruby болон Ruby on Rails-ийг дээр заасан холбоосоор орж гарын авлагатай танилцаж, сулугах зааврын дагуу суулгана уу. Харин одоо terminal-аа нээгээд:
 $ sudo apt-get install mysql
 $ gem install mongrel

* Үндсэн хөрс энд хүрээд бэлтгэгдэх ба одоо тохиргоонуудыг хийнэ.
Хамгийн түрүүнд config/database.yml файлыг нээж development хэсгийн хамгийн доод талын хоёр мөрийг дараах байдлаар өөрчлөнө:
 password: [энд mysql-ийн root нууц үг байна]
 host: localhost

За одоо баазаа үүсгэх ба дараах мөрийг terminal дээр өгнө:
 $ rake db:create RAILS_ENV='development'
 $ rake db:migrate

* Одоо бүх зүйл бэлэн болсон болохоор ажиллуулна:
 $ ruby script/server
Ингээд өөрийн http://localhost:3000 гээд ороод үз дэ. Хэрвээ бүх зүйл ном ёсоор болсон бол Gtree сайт маань ажиллаж байх болно.


Once your script is in place, edit `lib/github/markups.rb` and tell
GitHub Markup about it. Again we look to [rest2html][r2hc] for
guidance:

    command(:rest2html, /re?st(.txt)?/)

Here we're telling GitHub Markup of the existence of a `rest2html`
command which should be used for any file ending in `rest`,
`rst`, `rest.txt` or `rst.txt`. Any regular expression will do.
