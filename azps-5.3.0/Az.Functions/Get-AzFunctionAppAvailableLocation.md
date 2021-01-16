---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 3ab2ab4778b7fdb12334db416c953a7c373c63b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501021"
---
# <span data-ttu-id="5ec5b-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="5ec5b-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="5ec5b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ec5b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec5b-103">Pobiera lokalizację, w której jest dostępna aplikacja funkcji dla danego typu systemu operacyjnego i typu planu.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="5ec5b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ec5b-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5ec5b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ec5b-105">DESCRIPTION</span></span>
<span data-ttu-id="5ec5b-106">Pobiera lokalizację, w której jest dostępna aplikacja funkcji dla danego typu systemu operacyjnego i typu planu.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="5ec5b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ec5b-107">EXAMPLES</span></span>

### <span data-ttu-id="5ec5b-108">Przykład 1: Uzyskiwanie lokalizacji, w których dostępna jest wersja Premium dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="5ec5b-109">Jeśli nie określono żadnych parametrów, w obszarze Plantype jest ustawiona wartość "Premium", a OSType jest ustawiona na "Windows".</span><span class="sxs-lookup"><span data-stu-id="5ec5b-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
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

<span data-ttu-id="5ec5b-110">To polecenie umożliwia pobieranie lokalizacji, w których dostępna jest funkcja Premium dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="5ec5b-111">Przykład 2: Uzyskaj lokalizacje, w których dostępna jest wersja Premium dla Linux.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
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

<span data-ttu-id="5ec5b-112">To polecenie umożliwia pobieranie lokalizacji, w których dostępna jest wersja Premium dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="5ec5b-113">Przykład 3: Uzyskiwanie lokalizacji, w których zużycie jest dostępne dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
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

<span data-ttu-id="5ec5b-114">To polecenie umożliwia pobieranie lokalizacji, w których zużycie jest dostępne dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="5ec5b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ec5b-115">PARAMETERS</span></span>

### <span data-ttu-id="5ec5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ec5b-116">-DefaultProfile</span></span>
<span data-ttu-id="5ec5b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ec5b-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="5ec5b-118">-OSType</span></span>
<span data-ttu-id="5ec5b-119">Typ systemu operacyjnego dla planu usługi.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-119">The OS type for the service plan.</span></span>

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

### <span data-ttu-id="5ec5b-120">-Plantype</span><span class="sxs-lookup"><span data-stu-id="5ec5b-120">-PlanType</span></span>
<span data-ttu-id="5ec5b-121">Typ planu.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-121">The plan type.</span></span>
<span data-ttu-id="5ec5b-122">Prawidłowe dane wejściowe: zużycie lub Premium</span><span class="sxs-lookup"><span data-stu-id="5ec5b-122">Valid inputs: Consumption or Premium</span></span>

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

### <span data-ttu-id="5ec5b-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5ec5b-123">-SubscriptionId</span></span>
<span data-ttu-id="5ec5b-124">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-124">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="5ec5b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec5b-125">CommonParameters</span></span>
<span data-ttu-id="5ec5b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ec5b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec5b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ec5b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec5b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ec5b-128">INPUTS</span></span>

## <span data-ttu-id="5ec5b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ec5b-129">OUTPUTS</span></span>

### <span data-ttu-id="5ec5b-130">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="5ec5b-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="5ec5b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ec5b-131">NOTES</span></span>

<span data-ttu-id="5ec5b-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="5ec5b-132">ALIASES</span></span>

## <span data-ttu-id="5ec5b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ec5b-133">RELATED LINKS</span></span>

