---
title: ASP.NET Core Razor sayfaları kullanmaya başlama
author: rick-anderson
description: Bu öğretici serisinde, ASP.NET Core Razor sayfaları kullanma işlemi gösterilmektedir. Model oluşturma, Razor sayfaları için kod oluşturmak, veri erişimi için Entity Framework Core ve SQL Server kullanmak, arama işlevi eklemek, giriş doğrulaması eklemek ve modeli güncelleştirmek için geçişleri kullanma hakkında bilgi edinin.
ms.author: riande
ms.date: 05/30/2018
uid: tutorials/razor-pages/razor-pages-start
ms.openlocfilehash: 2e1c84a704856a22e1e105f56612194d4bb9c234
ms.sourcegitcommit: 599ebae5c2d6fcb22dfa6ae7d1f4bdfcacb79af4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47211006"
---
# <a name="tutorial-get-started-with-razor-pages-in-aspnet-core"></a>Öğretici: ASP.NET Core Razor sayfaları kullanmaya başlayın

Tarafından [Rick Anderson](https://twitter.com/RickAndMSFT)

::: moniker range="= aspnetcore-2.0"

Bu öğreticide ASP.NET Core 2.1 sürümünü izleyin öneririz. Sahip **çok** izleyin daha kolay ve daha fazla özellikleri kapsar. Seçin **ASP.NET Core 2.1** sürüm Seçici içinde.

![Sürüm Seçici İçindekiler](razor-pages-start/_static/v21.png)

::: moniker-end

Bu öğreticide bir ASP.NET Core Razor sayfaları web uygulaması oluşturmaya ilişkin temel bilgileri size öğretir. Razor sayfaları, ASP.NET Core web uygulamaları için kullanıcı arabirimini derlemek için önerilen yoludur.

Bu öğretici üç sürümü vardır:

* Windows: Bu öğretici
* MacOS: [Mac için Visual Studio ile Razor sayfaları ile başlama](xref:tutorials/razor-pages-mac/razor-pages-start)
* macOS, Linux ve Windows: [Visual Studio code'da ASP.NET Core Razor sayfaları kullanmaya başlama](xref:tutorials/razor-pages-vsc/razor-pages-start)

[Görüntüleme veya indirme örnek kodu](https://github.com/aspnet/Docs/tree/master/aspnetcore/tutorials/razor-pages/razor-pages-start/sample) ([nasıl indirileceğini](xref:tutorials/index#how-to-download-a-sample))

::: moniker range=">= aspnetcore-2.1"

## <a name="prerequisites"></a>Önkoşullar

[!INCLUDE [Prerequisites](~/includes/net-core-prereqs-windows.md)]

## <a name="create-a-razor-web-app"></a>Razor web uygulaması oluşturma

* Visual Studio'dan **dosya** menüsünde **yeni** > **proje**.
* Yeni bir ASP.NET Core Web uygulaması oluşturun. Projeyi adlandırın **RazorPagesMovie**. Projeyi adlandırın önemlidir *RazorPagesMovie* ad alanları, kopyala/yapıştır kod olduğunda eşleşecek şekilde.
 ![Yeni ASP.NET Core Web uygulaması](razor-pages-start/_static/np_2.1.png)
* Seçin **ASP.NET Core 2.1** açılır ve ardından **Web uygulaması**.

 ![Yeni ASP.NET Core Web uygulaması](razor-pages-start/_static/np_2_2.1.png)

Visual Studio şablonu bir başlangıç projesi oluşturur:

![Çözüm Gezgini](razor-pages-start/_static/se2.1.png)

Tuşuna **F5** uygulamayı hata ayıklama modunda çalıştırmak için veya **Ctrl-F5** Haya ayıklayıcı eklemeden çalıştırılacak. Seçin **kabul** izleme için onay verme. Bu uygulama, kişisel bilgi izlemez. Oluşturulan şablon kodunun karşılamanıza yardımcı olmak üzere varlıkları içeren [genel veri koruma yönetmeliği (GDPR)](xref:security/gdpr).

![Giriş ya da dizin sayfası](razor-pages-start/_static/homeGDPR.png)

Aşağıdaki görüntüde, izleme kabul ettikten sonra uygulama gösterilir:

![Giriş ya da dizin sayfası](razor-pages-start/_static/home2.1.png)

* Visual Studio başlatır [IIS Express](/iis/extensions/introduction-to-iis-express/iis-express-overview) ve uygulamayı çalıştırır. Adres çubuğu gösterir `localhost:port#` gibi bir şey `example.com`. Çünkü `localhost` standart, yerel bilgisayar adıdır. Localhost yalnızca yerel bilgisayara gelen web isteklerini işlevi görür. Visual Studio, bir web projesi oluşturduğunda, web sunucusu için rastgele bir bağlantı noktası kullanılır. Yukarıdaki görüntüde, 5001 bağlantı noktası numarasıdır. Uygulamayı çalıştırdığınızda, farklı bir bağlantı noktası görürsünüz.
* Uygulamayı başlatma **Ctrl + F5** (hata ayıklama olmayan mod), kod değişiklikleri yapabilir, dosyayı kaydetmek, tarayıcıyı yenileyin ve kod değişikliklerini görebilirsiniz olanak sağlar. Geliştiricilerin çoğu, hızlı bir şekilde uygulamayı başlatın ve değişiklikleri görmek için hata ayıklama olmayan modu kullanmayı tercih eder.

[!INCLUDE [razor-pages-start](~/includes/RP/2.1/razor-pages-start.md)]

[!INCLUDE [F7](~/includes/RP/F7.md)]

::: moniker-end

::: moniker range="= aspnetcore-2.0"

## <a name="prerequisites"></a>Önkoşullar

[!INCLUDE [Prerequisites](~/includes/net-core-prereqs-windows.md)]

## <a name="create-a-razor-web-app"></a>Razor web uygulaması oluşturma

* Visual Studio'dan **dosya** menüsünde **yeni** > **proje**.
* Yeni bir ASP.NET Core Web uygulaması oluşturun. Projeyi adlandırın **RazorPagesMovie**. Projeyi adlandırın önemlidir *RazorPagesMovie* ad alanları, kopyala/yapıştır kod olduğunda eşleşecek şekilde.
  ![Yeni ASP.NET Core Web uygulaması](../../razor-pages/index/_static/np.png)
* Seçin **ASP.NET Core 2.0** açılır ve ardından **Web uygulaması**.

  [!INCLUDE [install 2.0](~/includes/dotnetcore-on-dotnetfx-vs.md)]

Visual Studio şablonu bir başlangıç projesi oluşturur:

![Çözüm Gezgini](razor-pages-start/_static/se.png)

Tuşuna **F5** uygulamayı hata ayıklama modunda çalıştırmak için veya **Ctrl-F5** Haya ayıklayıcı eklemeden çalıştırmak için

![Giriş ya da dizin sayfası](razor-pages-start/_static/home.png)

* Visual Studio başlatır [IIS Express](/iis/extensions/introduction-to-iis-express/iis-express-overview) ve uygulamanızı çalışır. Adres çubuğu gösterir `localhost:port#` gibi bir şey `example.com`. Çünkü `localhost` standart, yerel bilgisayar adıdır. Localhost yalnızca yerel bilgisayara gelen web isteklerini işlevi görür. Visual Studio, bir web projesi oluşturduğunda, web sunucusu için rastgele bir bağlantı noktası kullanılır. Yukarıdaki görüntüde, bağlantı noktası numarasını 5000'dir. Uygulamayı çalıştırdığınızda, farklı bir bağlantı noktası görürsünüz.
* Uygulamayı başlatma **Ctrl + F5** (hata ayıklama olmayan mod), kod değişiklikleri yapabilir, dosyayı kaydetmek, tarayıcıyı yenileyin ve kod değişikliklerini görebilirsiniz olanak sağlar. Geliştiricilerin çoğu, hızlı bir şekilde uygulamayı başlatın ve değişiklikleri görmek için hata ayıklama olmayan modu kullanmayı tercih eder.

[!INCLUDE [razor-pages-start](~/includes/RP/razor-pages-start.md)]

::: moniker-end

> [!div class="step-by-step"]
> [Sonraki: model ekleme](xref:tutorials/razor-pages/model)
