---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889985"
---
# <span data-ttu-id="9e2ba-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9e2ba-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="9e2ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e2ba-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2ba-103">Zwraca wartość Avaialbility określonego typu i nazwy zasobu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9e2ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e2ba-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="9e2ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9e2ba-105">DESCRIPTION</span></span>
<span data-ttu-id="9e2ba-106">Zwraca wartość Avaialbility określonego typu i nazwy zasobu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9e2ba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e2ba-107">EXAMPLES</span></span>

### <span data-ttu-id="9e2ba-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9e2ba-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="9e2ba-109">Zwraca wartość Avaialbility określonego typu i nazwy zasobu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9e2ba-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e2ba-110">PARAMETERS</span></span>

### <span data-ttu-id="9e2ba-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e2ba-111">-Name</span></span>
<span data-ttu-id="9e2ba-112">Nazwa zasobu do zweryfikowania.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-112">The resource name to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2ba-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9e2ba-113">-ResourceType</span></span>
<span data-ttu-id="9e2ba-114">Typ zasobu do zweryfikowania.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-114">The resource type to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2ba-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2ba-115">CommonParameters</span></span>
<span data-ttu-id="9e2ba-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2ba-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e2ba-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2ba-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e2ba-118">INPUTS</span></span>

## <span data-ttu-id="9e2ba-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e2ba-119">OUTPUTS</span></span>

### <span data-ttu-id="9e2ba-120">Microsoft. AzureStack. Management. Subscriptions. admin. models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9e2ba-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="9e2ba-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e2ba-121">NOTES</span></span>

## <span data-ttu-id="9e2ba-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e2ba-122">RELATED LINKS</span></span>

