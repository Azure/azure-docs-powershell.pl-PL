---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 987c4e351e024452231b5a5367ea7c2905d57863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969089"
---
# <span data-ttu-id="e2a38-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="e2a38-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="e2a38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2a38-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a38-103">Pobiera lokalizację, w której jest dostępna aplikacja funkcji dla danego systemu operacyjnego i typu planu.</span><span class="sxs-lookup"><span data-stu-id="e2a38-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="e2a38-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e2a38-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e2a38-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e2a38-105">DESCRIPTION</span></span>
<span data-ttu-id="e2a38-106">Pobiera lokalizację, w której jest dostępna aplikacja funkcji dla danego systemu operacyjnego i typu planu.</span><span class="sxs-lookup"><span data-stu-id="e2a38-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="e2a38-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e2a38-107">EXAMPLES</span></span>

### <span data-ttu-id="e2a38-108">Przykład 1. Uzyskaj lokalizacje, w których wersja Premium jest dostępna dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="e2a38-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="e2a38-109">Jeśli nie określono żadnych parametrów, dla parametru PlanType ustawiono wartość "Premium", a dla typu OS — "Windows".</span><span class="sxs-lookup"><span data-stu-id="e2a38-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
West India
South India
Canada Central
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
Germany West Central
Norway East
```

<span data-ttu-id="e2a38-110">To polecenie pobiera lokalizacje, w których wersja Premium jest dostępna dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="e2a38-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="e2a38-111">Przykład 2. Uzyskaj lokalizacje, w których wersja Premium jest dostępna dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="e2a38-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Premium -OSType Linux

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
West India
Canada Central
West Central US
West US 2
UK West
UK South
Central US EUAP
Korea Central
France Central
Norway East
```

<span data-ttu-id="e2a38-112">To polecenie pobiera lokalizacje, w których wersja Premium jest dostępna dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="e2a38-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="e2a38-113">Przykład 3. Uzyskaj lokalizacje, w których dla systemu Windows jest dostępne zużycie.</span><span class="sxs-lookup"><span data-stu-id="e2a38-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Consumption -OSType Windows

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
Central India
West India
South India
Canada Central
Canada East
West Central US
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
South Africa North
Switzerland North
Germany West Central
```

<span data-ttu-id="e2a38-114">To polecenie pobiera lokalizacje, w których dla systemu Windows jest dostępne zużycie.</span><span class="sxs-lookup"><span data-stu-id="e2a38-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="e2a38-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2a38-115">PARAMETERS</span></span>

### <span data-ttu-id="e2a38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a38-116">-DefaultProfile</span></span>
<span data-ttu-id="e2a38-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a38-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a38-118">- OSType</span><span class="sxs-lookup"><span data-stu-id="e2a38-118">-OSType</span></span>
<span data-ttu-id="e2a38-119">Typ systemu operacyjnego dla planu usługi.</span><span class="sxs-lookup"><span data-stu-id="e2a38-119">The OS type for the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a38-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="e2a38-120">-PlanType</span></span>
<span data-ttu-id="e2a38-121">Typ planu.</span><span class="sxs-lookup"><span data-stu-id="e2a38-121">The plan type.</span></span>
<span data-ttu-id="e2a38-122">Prawidłowe dane wejściowe: Zużycie lub Premium</span><span class="sxs-lookup"><span data-stu-id="e2a38-122">Valid inputs: Consumption or Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a38-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2a38-123">-SubscriptionId</span></span>
<span data-ttu-id="e2a38-124">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a38-124">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a38-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a38-125">CommonParameters</span></span>
<span data-ttu-id="e2a38-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2a38-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a38-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2a38-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a38-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2a38-128">INPUTS</span></span>

## <span data-ttu-id="e2a38-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2a38-129">OUTPUTS</span></span>

### <span data-ttu-id="e2a38-130">Microsoft.Azure.PowerShell.Cmdlet.Functions.Models.Api20190801.IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="e2a38-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="e2a38-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e2a38-131">NOTES</span></span>

<span data-ttu-id="e2a38-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e2a38-132">ALIASES</span></span>

## <span data-ttu-id="e2a38-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2a38-133">RELATED LINKS</span></span>

