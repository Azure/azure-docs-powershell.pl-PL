---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d73e2db2f09ba504e9c6adbf15a0bbc2629452ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710691"
---
# <span data-ttu-id="98147-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="98147-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="98147-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98147-102">SYNOPSIS</span></span>
<span data-ttu-id="98147-103">Zwraca listę wszystkich stanów każdego zasobu w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="98147-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="98147-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98147-104">SYNTAX</span></span>

### <span data-ttu-id="98147-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="98147-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="98147-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="98147-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="98147-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="98147-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="98147-108">Opis</span><span class="sxs-lookup"><span data-stu-id="98147-108">DESCRIPTION</span></span>
<span data-ttu-id="98147-109">Zwraca listę wszystkich stanów każdego zasobu w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="98147-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="98147-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98147-110">EXAMPLES</span></span>

### <span data-ttu-id="98147-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="98147-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="98147-112">Zwraca listę wszystkich stanów każdego zasobu w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="98147-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="98147-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="98147-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="98147-114">Zwraca stan kondycji w obszarze a dla Microsoft. Fabric. Administrator.</span><span class="sxs-lookup"><span data-stu-id="98147-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="98147-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98147-115">PARAMETERS</span></span>

### <span data-ttu-id="98147-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="98147-116">-Filter</span></span>
<span data-ttu-id="98147-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="98147-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="98147-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="98147-118">-Location</span></span>
<span data-ttu-id="98147-119">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="98147-119">Name of the region</span></span>

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

### <span data-ttu-id="98147-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98147-120">-Name</span></span>
<span data-ttu-id="98147-121">Nazwa zasobu obiektu kondycji, który odpowiada identyfikatorowi rejestracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="98147-121">The resource name of the health object which corresponds to the resource registration id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98147-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98147-122">-ResourceGroupName</span></span>
<span data-ttu-id="98147-123">Nazwa grupy zasobów, w której znajduje się dany zasób.</span><span class="sxs-lookup"><span data-stu-id="98147-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="98147-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98147-124">-ResourceId</span></span>
<span data-ttu-id="98147-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="98147-125">The resource id.</span></span>

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

### <span data-ttu-id="98147-126">-Serviceregistrationname</span><span class="sxs-lookup"><span data-stu-id="98147-126">-ServiceRegistrationName</span></span>
<span data-ttu-id="98147-127">Identyfikator rejestracji usługi.</span><span class="sxs-lookup"><span data-stu-id="98147-127">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ServiceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98147-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="98147-128">-Skip</span></span>
<span data-ttu-id="98147-129">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="98147-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="98147-130">-Początek</span><span class="sxs-lookup"><span data-stu-id="98147-130">-Top</span></span>
<span data-ttu-id="98147-131">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="98147-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="98147-132">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="98147-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="98147-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98147-133">CommonParameters</span></span>
<span data-ttu-id="98147-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98147-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98147-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98147-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98147-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98147-136">INPUTS</span></span>

## <span data-ttu-id="98147-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98147-137">OUTPUTS</span></span>

### <span data-ttu-id="98147-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="98147-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="98147-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98147-139">NOTES</span></span>

## <span data-ttu-id="98147-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98147-140">RELATED LINKS</span></span>

