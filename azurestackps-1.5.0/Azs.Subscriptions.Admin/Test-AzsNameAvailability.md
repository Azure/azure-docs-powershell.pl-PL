---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 267a5bf4c3f864c987c0bc747eefce9dd3ffe6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710710"
---
# <span data-ttu-id="9a954-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9a954-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="9a954-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a954-102">SYNOPSIS</span></span>
<span data-ttu-id="9a954-103">Zwraca wartość Avaialbility określonego typu i nazwy zasobu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9a954-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9a954-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a954-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="9a954-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9a954-105">DESCRIPTION</span></span>
<span data-ttu-id="9a954-106">Zwraca wartość Avaialbility określonego typu i nazwy zasobu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9a954-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9a954-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a954-107">EXAMPLES</span></span>

### <span data-ttu-id="9a954-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9a954-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="9a954-109">Zwraca wartość Avaialbility określonego typu i nazwy zasobu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9a954-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9a954-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a954-110">PARAMETERS</span></span>

### <span data-ttu-id="9a954-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9a954-111">-Name</span></span>
<span data-ttu-id="9a954-112">Nazwa zasobu do zweryfikowania.</span><span class="sxs-lookup"><span data-stu-id="9a954-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="9a954-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9a954-113">-ResourceType</span></span>
<span data-ttu-id="9a954-114">Typ zasobu do zweryfikowania.</span><span class="sxs-lookup"><span data-stu-id="9a954-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="9a954-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a954-115">CommonParameters</span></span>
<span data-ttu-id="9a954-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a954-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a954-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a954-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a954-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a954-118">INPUTS</span></span>

## <span data-ttu-id="9a954-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a954-119">OUTPUTS</span></span>

### <span data-ttu-id="9a954-120">Microsoft. AzureStack. Management. Subscriptions. admin. models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9a954-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="9a954-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a954-121">NOTES</span></span>

## <span data-ttu-id="9a954-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a954-122">RELATED LINKS</span></span>

