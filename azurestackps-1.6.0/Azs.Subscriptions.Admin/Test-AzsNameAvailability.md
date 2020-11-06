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
ms.locfileid: "93523438"
---
# <span data-ttu-id="54a34-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="54a34-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="54a34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54a34-102">SYNOPSIS</span></span>
<span data-ttu-id="54a34-103">Zwraca wartość Avaialbility określonego typu i nazwy zasobu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="54a34-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="54a34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54a34-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="54a34-105">Opis</span><span class="sxs-lookup"><span data-stu-id="54a34-105">DESCRIPTION</span></span>
<span data-ttu-id="54a34-106">Zwraca wartość Avaialbility określonego typu i nazwy zasobu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="54a34-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="54a34-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54a34-107">EXAMPLES</span></span>

### <span data-ttu-id="54a34-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="54a34-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="54a34-109">Zwraca wartość Avaialbility określonego typu i nazwy zasobu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="54a34-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="54a34-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54a34-110">PARAMETERS</span></span>

### <span data-ttu-id="54a34-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="54a34-111">-Name</span></span>
<span data-ttu-id="54a34-112">Nazwa zasobu do zweryfikowania.</span><span class="sxs-lookup"><span data-stu-id="54a34-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="54a34-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="54a34-113">-ResourceType</span></span>
<span data-ttu-id="54a34-114">Typ zasobu do zweryfikowania.</span><span class="sxs-lookup"><span data-stu-id="54a34-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="54a34-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a34-115">CommonParameters</span></span>
<span data-ttu-id="54a34-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54a34-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a34-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54a34-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a34-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54a34-118">INPUTS</span></span>

## <span data-ttu-id="54a34-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54a34-119">OUTPUTS</span></span>

### <span data-ttu-id="54a34-120">Microsoft. AzureStack. Management. Subscriptions. admin. models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="54a34-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="54a34-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54a34-121">NOTES</span></span>

## <span data-ttu-id="54a34-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54a34-122">RELATED LINKS</span></span>

