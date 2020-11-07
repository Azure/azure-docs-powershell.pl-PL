---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4285a7423390f5d9b5384faa63f95c4206840d71
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889913"
---
# <span data-ttu-id="df57d-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="df57d-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="df57d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df57d-102">SYNOPSIS</span></span>
<span data-ttu-id="df57d-103">Zwraca listę wszystkich stanów każdego zasobu w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="df57d-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="df57d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df57d-104">SYNTAX</span></span>

### <span data-ttu-id="df57d-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="df57d-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="df57d-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="df57d-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> -ResourceRegistrationId <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="df57d-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="df57d-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="df57d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="df57d-108">DESCRIPTION</span></span>
<span data-ttu-id="df57d-109">Zwraca listę wszystkich stanów każdego zasobu w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="df57d-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="df57d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df57d-110">EXAMPLES</span></span>

### <span data-ttu-id="df57d-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="df57d-111">EXAMPLE 1</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="df57d-112">Zwraca listę wszystkich stanów każdego zasobu w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="df57d-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="df57d-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="df57d-113">EXAMPLE 2</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationId $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="df57d-114">Zwraca stan kondycji w obszarze a dla Microsoft. Fabric. Administrator.</span><span class="sxs-lookup"><span data-stu-id="df57d-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="df57d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df57d-115">PARAMETERS</span></span>

### <span data-ttu-id="df57d-116">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="df57d-116">-ServiceRegistrationId</span></span>
<span data-ttu-id="df57d-117">Identyfikator rejestracji usługi.</span><span class="sxs-lookup"><span data-stu-id="df57d-117">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df57d-118">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="df57d-118">-ResourceRegistrationId</span></span>


```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df57d-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="df57d-119">-Location</span></span>
<span data-ttu-id="df57d-120">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="df57d-120">Name of the region</span></span>

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

### <span data-ttu-id="df57d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df57d-121">-ResourceGroupName</span></span>
<span data-ttu-id="df57d-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df57d-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="df57d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df57d-123">-ResourceId</span></span>
<span data-ttu-id="df57d-124">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="df57d-124">The resource id.</span></span>

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

### <span data-ttu-id="df57d-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="df57d-125">-Filter</span></span>
<span data-ttu-id="df57d-126">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="df57d-126">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df57d-127">-Początek</span><span class="sxs-lookup"><span data-stu-id="df57d-127">-Top</span></span>
<span data-ttu-id="df57d-128">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="df57d-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="df57d-129">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="df57d-129">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df57d-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="df57d-130">-Skip</span></span>
<span data-ttu-id="df57d-131">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="df57d-131">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df57d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df57d-132">CommonParameters</span></span>
<span data-ttu-id="df57d-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df57d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df57d-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df57d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df57d-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df57d-135">INPUTS</span></span>

## <span data-ttu-id="df57d-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df57d-136">OUTPUTS</span></span>

### <span data-ttu-id="df57d-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="df57d-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="df57d-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df57d-138">NOTES</span></span>

## <span data-ttu-id="df57d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df57d-139">RELATED LINKS</span></span>
