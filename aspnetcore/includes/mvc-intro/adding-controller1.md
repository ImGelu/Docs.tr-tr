Model-View-Controller (MVC) tasarım örüntüsü bir uygulamayı üç ana bileşenlerine ayırır: **M**odel, **V**görünümü, ve **C**ontroller. MVC örüntüsü daha sınanabilir ve daha kolay güncelleştirmek geleneksel tek yapılı uygulamalar uygulamalar oluşturmanıza yardımcı olur. MVC tabanlı uygulamalar içerir:

* **M**odels: uygulama verilerini temsil eden sınıf. Modeli sınıflarını doğrulama mantığını bu verilere iş kurallarını zorunlu tutmak için kullanın. Genellikle, model nesneleri alabilir ve model durumu bir veritabanında depolar. Bu öğreticide bir `Movie` model bir veritabanından film verileri alır, görünüme sağlar veya güncelleştirdiği. Güncelleştirilen verileri bir veritabanına yazılır.

* **V**iews: görünümler, uygulamanın kullanıcı arabirimini (UI) görüntüleme bileşenleridir. Genellikle, bu UI model verileri görüntüler.

* **C**ontrollers: tarayıcı isteklerini işleyen sınıflar. Bunlar, model verileri almak ve bir yanıt döndürür görünüm şablonları çağırın. Bir MVC uygulamasında görünüm yalnızca bilgileri görüntüler; Denetleyici işler ve kullanıcı girişini ve etkileşimini yanıt verir. Örneğin, denetleyici, rota veri ve sorgu dizesi değerlerini işler ve bu değerleri modele geçirir. Model, veritabanını sorgulamak için bu değerleri kullanabilirsiniz. Örneğin, `http://localhost:1234/Home/About` rota verilerini sahip `Home` (denetleyicisi) ve `About` (ev denetleyicisinde çağrılacak eylem yöntemi). `http://localhost:1234/Movies/Edit/5`Kimliğine sahip film düzenlemek için bir istek = film denetleyicisi kullanarak 5.  Biz, daha sonra öğreticide rota verilerini hakkında konuşun.

MVC örüntüsü, öğeler arasında gevşek bağlantı sağlarken (giriş mantığı, iş mantığı ve UI mantığı), uygulamanın farklı yönlerini ayıran uygulamalar oluşturmanıza yardımcı olur. Desen burada her bir mantık türünün uygulamada yer alması gerektiğini belirtir. UI mantığı görünümde yer alır. Giriş mantığı denetleyicide yer alır. İş mantığı modelde yer alır. Bu ayrım, bir uygulama oluşturduğunuzda, başka bir kod etkilemeden aynı anda bir yönüne çalışmak sağladığı için karışıklığı yönetmenize yardımcı olur. Örneğin, iş mantığı koduna bağlı olarak görünüm kodu olmadan üzerinde çalışabilir.

Biz Bu öğretici serisinde bu kavramları kapsar ve bunları bir film uygulaması oluşturmak için nasıl kullanılacağını gösterir. MVC projesini klasörleri içeren *denetleyicileri* ve *görünümleri*.