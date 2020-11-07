---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889945"
---
# <span data-ttu-id="8afef-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="8afef-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="8afef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8afef-102">SYNOPSIS</span></span>
<span data-ttu-id="8afef-103">Zwraca przydziały określające limity przydziałów dla obiektów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="8afef-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="8afef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8afef-104">SYNTAX</span></span>

### <span data-ttu-id="8afef-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="8afef-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="8afef-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="8afef-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="8afef-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="8afef-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8afef-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8afef-108">DESCRIPTION</span></span>
<span data-ttu-id="8afef-109">Zapoznaj się z listą istniejących przydziałów.</span><span class="sxs-lookup"><span data-stu-id="8afef-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="8afef-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8afef-110">EXAMPLES</span></span>

### <span data-ttu-id="8afef-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8afef-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="8afef-112">Pobieranie wszystkich przydziałów obliczeń w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8afef-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="8afef-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8afef-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="8afef-114">Uzyskiwanie określonego przydziału obliczeń.</span><span class="sxs-lookup"><span data-stu-id="8afef-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="8afef-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8afef-115">PARAMETERS</span></span>

### <span data-ttu-id="8afef-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8afef-116">-Location</span></span>
<span data-ttu-id="8afef-117">{{Opis lokalizacji wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="8afef-117">{{Fill Location Description}}</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afef-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8afef-118">-Name</span></span>
<span data-ttu-id="8afef-119">Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="8afef-119">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afef-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8afef-120">-ResourceId</span></span>
<span data-ttu-id="8afef-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="8afef-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8afef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8afef-122">CommonParameters</span></span>
<span data-ttu-id="8afef-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8afef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8afef-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8afef-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8afef-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8afef-125">INPUTS</span></span>

## <span data-ttu-id="8afef-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8afef-126">OUTPUTS</span></span>

### <span data-ttu-id="8afef-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="8afef-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="8afef-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8afef-128">NOTES</span></span>

## <span data-ttu-id="8afef-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8afef-129">RELATED LINKS</span></span>

