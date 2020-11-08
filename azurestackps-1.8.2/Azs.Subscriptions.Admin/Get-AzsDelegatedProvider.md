---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061560"
---
# <span data-ttu-id="b1f0f-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="b1f0f-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="b1f0f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f0f-103">Pobierz listę delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="b1f0f-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="b1f0f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1f0f-104">SYNTAX</span></span>

### <span data-ttu-id="b1f0f-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b1f0f-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="b1f0f-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="b1f0f-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="b1f0f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b1f0f-107">DESCRIPTION</span></span>
<span data-ttu-id="b1f0f-108">Pobierz listę delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="b1f0f-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="b1f0f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1f0f-109">EXAMPLES</span></span>

### <span data-ttu-id="b1f0f-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1f0f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="b1f0f-111">Uzyskaj listę dostawców delegowanych.</span><span class="sxs-lookup"><span data-stu-id="b1f0f-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="b1f0f-112">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1f0f-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="b1f0f-113">Uzyskiwanie określonego dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="b1f0f-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="b1f0f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1f0f-114">PARAMETERS</span></span>

### <span data-ttu-id="b1f0f-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="b1f0f-115">-DelegatedProviderId</span></span>
<span data-ttu-id="b1f0f-116">{{Fill DelegatedProviderId Description}}</span><span class="sxs-lookup"><span data-stu-id="b1f0f-116">{{Fill DelegatedProviderId Description}}</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f0f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f0f-117">CommonParameters</span></span>
<span data-ttu-id="b1f0f-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f0f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f0f-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1f0f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f0f-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1f0f-120">INPUTS</span></span>

## <span data-ttu-id="b1f0f-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1f0f-121">OUTPUTS</span></span>

### <span data-ttu-id="b1f0f-122">Microsoft. AzureStack. Management. Subscriptions. admin. modele. Subscription</span><span class="sxs-lookup"><span data-stu-id="b1f0f-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="b1f0f-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1f0f-123">NOTES</span></span>

## <span data-ttu-id="b1f0f-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1f0f-124">RELATED LINKS</span></span>

