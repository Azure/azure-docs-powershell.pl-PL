---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 3ab2ab4778b7fdb12334db416c953a7c373c63b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243506"
---
# <span data-ttu-id="c3855-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="c3855-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="c3855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3855-102">SYNOPSIS</span></span>
<span data-ttu-id="c3855-103">Pobiera lokalizację, w której jest dostępna aplikacja funkcji dla danego systemu operacyjnego i typu planu.</span><span class="sxs-lookup"><span data-stu-id="c3855-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="c3855-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c3855-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c3855-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c3855-105">DESCRIPTION</span></span>
<span data-ttu-id="c3855-106">Pobiera lokalizację, w której jest dostępna aplikacja funkcji dla danego systemu operacyjnego i typu planu.</span><span class="sxs-lookup"><span data-stu-id="c3855-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="c3855-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c3855-107">EXAMPLES</span></span>

### <span data-ttu-id="c3855-108">Przykład 1. Uzyskaj lokalizacje, w których wersja Premium jest dostępna dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="c3855-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="c3855-109">Jeśli nie określono żadnych parametrów, dla parametru PlanType ustawiono wartość "Premium", a dla typu OS — "Windows".</span><span class="sxs-lookup"><span data-stu-id="c3855-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
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

<span data-ttu-id="c3855-110">To polecenie pobiera lokalizacje, w których wersja Premium jest dostępna dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="c3855-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="c3855-111">Przykład 2. Uzyskaj lokalizacje, w których wersja Premium jest dostępna dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="c3855-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
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

<span data-ttu-id="c3855-112">To polecenie pobiera lokalizacje, w których wersja Premium jest dostępna dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="c3855-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="c3855-113">Przykład 3. Uzyskaj lokalizacje, w których dla systemu Windows jest dostępne zużycie.</span><span class="sxs-lookup"><span data-stu-id="c3855-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
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

<span data-ttu-id="c3855-114">To polecenie pobiera lokalizacje, w których dla systemu Windows jest dostępne zużycie.</span><span class="sxs-lookup"><span data-stu-id="c3855-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="c3855-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3855-115">PARAMETERS</span></span>

### <span data-ttu-id="c3855-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3855-116">-DefaultProfile</span></span>
<span data-ttu-id="c3855-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3855-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3855-118">- OSType</span><span class="sxs-lookup"><span data-stu-id="c3855-118">-OSType</span></span>
<span data-ttu-id="c3855-119">Typ systemu operacyjnego dla planu usługi.</span><span class="sxs-lookup"><span data-stu-id="c3855-119">The OS type for the service plan.</span></span>

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

### <span data-ttu-id="c3855-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="c3855-120">-PlanType</span></span>
<span data-ttu-id="c3855-121">Typ planu.</span><span class="sxs-lookup"><span data-stu-id="c3855-121">The plan type.</span></span>
<span data-ttu-id="c3855-122">Prawidłowe dane wejściowe: Zużycie lub Premium</span><span class="sxs-lookup"><span data-stu-id="c3855-122">Valid inputs: Consumption or Premium</span></span>

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

### <span data-ttu-id="c3855-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3855-123">-SubscriptionId</span></span>
<span data-ttu-id="c3855-124">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c3855-124">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="c3855-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3855-125">CommonParameters</span></span>
<span data-ttu-id="c3855-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3855-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3855-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3855-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3855-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3855-128">INPUTS</span></span>

## <span data-ttu-id="c3855-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3855-129">OUTPUTS</span></span>

### <span data-ttu-id="c3855-130">Microsoft.Azure.PowerShell.Cmdlet.Functions.Models.Api20190801.IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="c3855-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="c3855-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c3855-131">NOTES</span></span>

<span data-ttu-id="c3855-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c3855-132">ALIASES</span></span>

## <span data-ttu-id="c3855-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3855-133">RELATED LINKS</span></span>

