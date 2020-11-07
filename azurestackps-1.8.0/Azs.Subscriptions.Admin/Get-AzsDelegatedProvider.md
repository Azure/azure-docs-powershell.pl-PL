---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889286"
---
# <span data-ttu-id="a53d4-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="a53d4-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="a53d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a53d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a53d4-103">Pobierz listę delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="a53d4-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="a53d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a53d4-104">SYNTAX</span></span>

### <span data-ttu-id="a53d4-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a53d4-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="a53d4-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="a53d4-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="a53d4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a53d4-107">DESCRIPTION</span></span>
<span data-ttu-id="a53d4-108">Pobierz listę delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="a53d4-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="a53d4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a53d4-109">EXAMPLES</span></span>

### <span data-ttu-id="a53d4-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a53d4-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="a53d4-111">Uzyskaj listę dostawców delegowanych.</span><span class="sxs-lookup"><span data-stu-id="a53d4-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="a53d4-112">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a53d4-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="a53d4-113">Uzyskiwanie określonego dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="a53d4-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="a53d4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a53d4-114">PARAMETERS</span></span>

### <span data-ttu-id="a53d4-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="a53d4-115">-DelegatedProviderId</span></span>
<span data-ttu-id="a53d4-116">{{Fill DelegatedProviderId Description}}</span><span class="sxs-lookup"><span data-stu-id="a53d4-116">{{Fill DelegatedProviderId Description}}</span></span>

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

### <span data-ttu-id="a53d4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a53d4-117">CommonParameters</span></span>
<span data-ttu-id="a53d4-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a53d4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a53d4-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a53d4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a53d4-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a53d4-120">INPUTS</span></span>

## <span data-ttu-id="a53d4-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a53d4-121">OUTPUTS</span></span>

### <span data-ttu-id="a53d4-122">Microsoft. AzureStack. Management. Subscriptions. admin. modele. Subscription</span><span class="sxs-lookup"><span data-stu-id="a53d4-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="a53d4-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a53d4-123">NOTES</span></span>

## <span data-ttu-id="a53d4-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a53d4-124">RELATED LINKS</span></span>

