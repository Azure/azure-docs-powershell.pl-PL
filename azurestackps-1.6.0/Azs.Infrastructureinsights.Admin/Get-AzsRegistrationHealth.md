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
ms.locfileid: "93523598"
---
# <span data-ttu-id="62798-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="62798-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="62798-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62798-102">SYNOPSIS</span></span>
<span data-ttu-id="62798-103">Zwraca listę wszystkich stanów każdego zasobu w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="62798-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="62798-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62798-104">SYNTAX</span></span>

### <span data-ttu-id="62798-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="62798-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="62798-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="62798-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="62798-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="62798-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="62798-108">Opis</span><span class="sxs-lookup"><span data-stu-id="62798-108">DESCRIPTION</span></span>
<span data-ttu-id="62798-109">Zwraca listę wszystkich stanów każdego zasobu w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="62798-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="62798-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62798-110">EXAMPLES</span></span>

### <span data-ttu-id="62798-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="62798-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="62798-112">Zwraca listę wszystkich stanów każdego zasobu w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="62798-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="62798-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="62798-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="62798-114">Zwraca stan kondycji w obszarze a dla Microsoft. Fabric. Administrator.</span><span class="sxs-lookup"><span data-stu-id="62798-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="62798-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62798-115">PARAMETERS</span></span>

### <span data-ttu-id="62798-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="62798-116">-Filter</span></span>
<span data-ttu-id="62798-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="62798-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="62798-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="62798-118">-Location</span></span>
<span data-ttu-id="62798-119">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="62798-119">Name of the region</span></span>

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

### <span data-ttu-id="62798-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62798-120">-Name</span></span>
<span data-ttu-id="62798-121">Nazwa zasobu obiektu kondycji, który odpowiada identyfikatorowi rejestracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="62798-121">The resource name of the health object which corresponds to the resource registration id.</span></span>

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

### <span data-ttu-id="62798-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62798-122">-ResourceGroupName</span></span>
<span data-ttu-id="62798-123">Nazwa grupy zasobów, w której znajduje się dany zasób.</span><span class="sxs-lookup"><span data-stu-id="62798-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="62798-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62798-124">-ResourceId</span></span>
<span data-ttu-id="62798-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="62798-125">The resource id.</span></span>

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

### <span data-ttu-id="62798-126">-Serviceregistrationname</span><span class="sxs-lookup"><span data-stu-id="62798-126">-ServiceRegistrationName</span></span>
<span data-ttu-id="62798-127">Identyfikator rejestracji usługi.</span><span class="sxs-lookup"><span data-stu-id="62798-127">Service registration id.</span></span>

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

### <span data-ttu-id="62798-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="62798-128">-Skip</span></span>
<span data-ttu-id="62798-129">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="62798-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="62798-130">-Początek</span><span class="sxs-lookup"><span data-stu-id="62798-130">-Top</span></span>
<span data-ttu-id="62798-131">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="62798-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="62798-132">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="62798-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="62798-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62798-133">CommonParameters</span></span>
<span data-ttu-id="62798-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62798-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62798-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62798-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62798-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62798-136">INPUTS</span></span>

## <span data-ttu-id="62798-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62798-137">OUTPUTS</span></span>

### <span data-ttu-id="62798-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="62798-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="62798-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62798-139">NOTES</span></span>

## <span data-ttu-id="62798-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62798-140">RELATED LINKS</span></span>

