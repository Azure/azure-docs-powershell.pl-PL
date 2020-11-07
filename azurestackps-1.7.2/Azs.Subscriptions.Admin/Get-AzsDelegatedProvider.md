---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704790"
---
# <span data-ttu-id="836b0-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="836b0-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="836b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="836b0-102">SYNOPSIS</span></span>
<span data-ttu-id="836b0-103">Pobierz listę delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="836b0-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="836b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="836b0-104">SYNTAX</span></span>

### <span data-ttu-id="836b0-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="836b0-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="836b0-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="836b0-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="836b0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="836b0-107">DESCRIPTION</span></span>
<span data-ttu-id="836b0-108">Pobierz listę delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="836b0-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="836b0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="836b0-109">EXAMPLES</span></span>

### <span data-ttu-id="836b0-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="836b0-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="836b0-111">Uzyskaj listę dostawców delegowanych.</span><span class="sxs-lookup"><span data-stu-id="836b0-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="836b0-112">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="836b0-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="836b0-113">Uzyskiwanie określonego dostawcy delegowanego.</span><span class="sxs-lookup"><span data-stu-id="836b0-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="836b0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="836b0-114">PARAMETERS</span></span>

### <span data-ttu-id="836b0-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="836b0-115">-DelegatedProviderId</span></span>
<span data-ttu-id="836b0-116">Identyfikator DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="836b0-116">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="836b0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="836b0-117">CommonParameters</span></span>
<span data-ttu-id="836b0-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="836b0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="836b0-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="836b0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="836b0-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="836b0-120">INPUTS</span></span>

## <span data-ttu-id="836b0-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="836b0-121">OUTPUTS</span></span>

### <span data-ttu-id="836b0-122">Microsoft. AzureStack. Management. Subscriptions. admin. modele. Subscription</span><span class="sxs-lookup"><span data-stu-id="836b0-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="836b0-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="836b0-123">NOTES</span></span>

## <span data-ttu-id="836b0-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="836b0-124">RELATED LINKS</span></span>

