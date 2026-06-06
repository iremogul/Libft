*Bu proje 42 müfredatının bir parçası olarak geliştirilmiş ve oluşturulmuştur.*

# Libft

## Açıklama (Description)
Libft, C programlama dilindeki standart kütüphane (libc) fonksiyonlarının birçoğunu ve çeşitli ek yardımcı fonksiyonları baştan yazdığımız ilk 42 projesidir. Amacımız, ilerideki tüm projelerimizde temel araç seti olarak kullanmak üzere güvenilir, optimize edilmiş ve standartlara uygun kendi statik kütüphanemizi (`libft.a`) oluşturmaktır.

Bu proje sayesinde bellek yönetimi (memory allocation), string manipülasyonu ve standart C fonksiyonlarının arka planda nasıl çalıştığına dair derinlemesine bir anlayış kazanılmıştır.

---

## İçerik ve Fonksiyonlar
Bu kütüphane, zorunlu (mandatory) bölüm gereksinimlerine göre iki ana kategorideki fonksiyonları içermektedir:

### 1. Libc Fonksiyonları
Standart C kütüphanesinde bulunan temel fonksiyonların yeniden yazılmış versiyonları:
* **Karakter Kontrolleri ve Dönüşümleri:** `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`, `ft_toupper`, `ft_tolower`
* **String İşlemleri:** `ft_strlen`, `ft_strlcpy`, `ft_strlcat`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`
* **Bellek (Memory) İşlemleri:** `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`
* **Dönüşüm ve Dinamik Bellek:** `ft_atoi`, `ft_calloc`, `ft_strdup`

### 2. Ek Fonksiyonlar (Additional Functions)
Standart kütüphanede yer almayan ancak 42 projelerinde sıkça ihtiyaç duyulan yardımcı fonksiyonlar:
* **String Manipülasyonu:** `ft_substr`, `ft_strjoin`, `ft_strtrim`, `ft_split`
* **Dönüşümler ve İterasyonlar:** `ft_itoa`, `ft_strmapi`, `ft_striteri`
* **Dosya Tanımlayıcı (File Descriptor) Çıktıları:** `ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd`

---

## Kurulum ve Kullanım (Instructions)

### Derleme
Kütüphaneyi derlemek ve `libft.a` statik kütüphane dosyasını oluşturmak için terminalde projenin kök dizinine gidip aşağıdaki komutu çalıştırmanız yeterlidir:
make

Bu işlem, tüm `.c` kaynak dosyalarınızı `-Wall -Wextra -Werror` bayraklarıyla derleyerek kütüphaneyi kullanıma hazır hale getirecektir. Projenizi derledikten sonra temizlik yapmak için aşağıdaki kuralları kullanabilirsiniz:
* `make clean`: Yalnızca derlenmiş nesne (object) dosyalarını (`.o`) siler.
* `make fclean`: Nesne dosyalarıyla birlikte oluşturulan `libft.a` dosyasını da siler.
* `make re`: Her şeyi tamamen temizler ve kütüphaneyi baştan derler.

### Kütüphanenin Kullanımı
Oluşturduğunuz `libft.a` dosyasını kendi C projelerinizde kullanmak için:
1. `libft.h` başlık (header) dosyasını ilgili kodlarınıza `#include "libft.h"` şeklinde ekleyin.
2. Kodunuzu derlerken kütüphaneyi derleyiciye bağlayın (link):
gcc main.c -L. -lft

---

## Kaynaklar ve Yapay Zeka Kullanımı (Resources)
* **Temel Referanslar:** Linux man sayfaları (manual pages) ve C programlama standartları.
* **Yapay Zeka (AI) Kullanımı:** Geliştirme sürecinde yapay zeka araçları; Makefile kurgusunun oluşturulması, `ft_split` gibi karmaşık bellek yönetimi gerektiren fonksiyonların mantıksal taslaklarının çıkarılması ve pointer aritmetiği konularında kavramsal açıklamalar almak amacıyla kullanılmıştır. Üretilen hiçbir çözüm projeye doğrudan kopyalanmamış; her bir fonksiyon manuel testlerden geçirilmiş ve çalışma mekanizması tamamen anlaşılarak koda entegre edilmiştir.
