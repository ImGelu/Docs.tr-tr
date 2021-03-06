---
uid: web-forms/overview/ajax-control-toolkit/confirmbutton/using-a-confirmbutton-in-a-repeater-vb
title: (VB) Repeater'da ConfirmButton kullanma | Microsoft Docs
author: wenz
description: Evet, AJAX Denetim Araç Seti ConfirmButton genişletici oluşturur/Kullanıcı bir düğmeyi tıkladığında açılır penceresi (LinkButton denetim dahil). Yalnızca Evet ise...
ms.author: riande
ms.date: 06/02/2008
ms.assetid: 18c31709-3f9d-4d93-8b01-f1356bf610b4
msc.legacyurl: /web-forms/overview/ajax-control-toolkit/confirmbutton/using-a-confirmbutton-in-a-repeater-vb
msc.type: authoredcontent
ms.openlocfilehash: 38ac40776c2fdd14af046b5e13df0701c71a4ad0
ms.sourcegitcommit: 45ac74e400f9f2b7dbded66297730f6f14a4eb25
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2018
ms.locfileid: "41755539"
---
<a name="using-a-confirmbutton-in-a-repeater-vb"></a>(VB) Repeater'da ConfirmButton kullanma
====================
tarafından [Christian Wenz](https://github.com/wenz)

[Kodu indir](http://download.microsoft.com/download/8/6/d/86dea6c6-bb92-4fa6-aa14-f8c0f82100f5/ConfirmButton1.vb.zip) veya [PDF olarak indirin](http://download.microsoft.com/download/b/6/a/b6ae89ee-df69-4c87-9bfb-ad1eb2b23373/confirmbutton1VB.pdf)

> Evet, AJAX Denetim Araç Seti ConfirmButton genişletici oluşturur/Kullanıcı bir düğmeyi tıkladığında açılır penceresi (LinkButton denetim dahil). Yalnızca Evet tıklandığında, düğmenin eylemi, aksi takdirde iptal yürütülür. Bu aynı zamanda repeater'da mümkündür.


## <a name="overview"></a>Genel Bakış

Evet, AJAX Denetim Araç Seti ConfirmButton genişletici oluşturur/Kullanıcı bir düğmeyi tıkladığında açılır penceresi (LinkButton denetim dahil). Yalnızca Evet tıklandığında, düğmenin eylemi, aksi takdirde iptal yürütülür. Bu aynı zamanda repeater'da mümkündür.

## <a name="steps"></a>Adımlar

İlk olarak bir veri kaynağı gereklidir. Bu örnekte, AdventureWorks veritabanını ve Microsoft SQL Server 2005 Express Edition kullanır. Veritabanı (express sürüm dahil) bir Visual Studio yüklemesi isteğe bağlı bir parçasıdır ve ayrıca altında ayrı bir indirme olarak kullanılabilir [ https://go.microsoft.com/fwlink/?LinkId=64064 ](https://go.microsoft.com/fwlink/?LinkId=64064). AdventureWorks veritabanı SQL Server 2005 örnekleri ve örnek veritabanları parçasıdır (adresinden [ https://www.microsoft.com/downloads/details.aspx?FamilyID=e719ecf7-9f46-4312-af89-6ad8702e4e6e&amp; DisplayLang = tr](https://www.microsoft.com/downloads/details.aspx?FamilyID=e719ecf7-9f46-4312-af89-6ad8702e4e6e&amp;DisplayLang=en)). En kolay yolu, veritabanını ayarlamak için Microsoft SQL Server Management Studio Express kullanmaktır ([https://www.microsoft.com/downloads/details.aspx?FamilyID=c243a5ae-4bd1-4e3d-94b8-5a0f62bf7796&amp; DisplayLang = tr](https://www.microsoft.com/downloads/details.aspx?FamilyID=c243a5ae-4bd1-4e3d-94b8-5a0f62bf7796&amp;DisplayLang=en)) ve ekleme `AdventureWorks.mdf` veritabanı dosyası.

Bu örnek için SQL Server 2005 Express Edition örneğini çağrıldığından emin olan varsayıyoruz `SQLEXPRESS` ve web sunucusu; ile aynı makinede bulunan varsayılan kurulumu da budur. Kurulumunuzu farklıysa, veritabanı için bağlantı bilgilerini uymak zorunda.

ASP.NET AJAX Denetim Araç Seti ve işlevlerini etkinleştirmek için `ScriptManager` denetim gerekir yerleştirmek herhangi bir sayfada (ancak içinde `<form>` öğesi):

[!code-aspx[Main](using-a-confirmbutton-in-a-repeater-vb/samples/sample1.aspx)]

Ardından, bir veri kaynağı gereklidir. Basitleştirmek amacıyla, yalnızca ilk beş girişleri satıcıları tablosunda AdventureWorks alınır. Tablo adı veri kaynağını oluşturmak için Visual Studio Sihirbazı'nı kullanırken dikkat edin (`Vendors`) şu anda doğru ön ekine sahip değil `Purchasing`. Aşağıdaki biçimlendirmede doğru olur:

[!code-aspx[Main](using-a-confirmbutton-in-a-repeater-vb/samples/sample2.aspx)]

Bu veri kaynağı, bir yineleyici içinde kullanılabilir. Her zamanki şekilde `DataBinder.Eval()` yöntemi, veri kaynağından veri alır. `ConfirmButtonExtender` Denetim sonra yerleştirilmelidir içinde `<ItemTemplate>` BT'nin veri kaynağındaki her giriş için görünmesi yineleyicinin bölümü.

[!code-aspx[Main](using-a-confirmbutton-in-a-repeater-vb/samples/sample3.aspx)]


[![Her giriş veri kaynağından yanında Onayla düğmesi görünür](using-a-confirmbutton-in-a-repeater-vb/_static/image2.png)](using-a-confirmbutton-in-a-repeater-vb/_static/image1.png)

Her giriş veri kaynağından yanında Onayla düğmesi görünür ([tam boyutlu görüntüyü görmek için tıklatın](using-a-confirmbutton-in-a-repeater-vb/_static/image3.png))

> [!div class="step-by-step"]
> [Önceki](using-a-confirmbutton-in-a-repeater-cs.md)
