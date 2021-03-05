---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 62ef80d7af7ce9b9a10a7a18b38fbf5c6f1db562
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994260"
---
# <span data-ttu-id="8c759-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="8c759-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="8c759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c759-102">SYNOPSIS</span></span>
<span data-ttu-id="8c759-103">Konfiguracje aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="8c759-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="8c759-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c759-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c759-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c759-105">DESCRIPTION</span></span>
<span data-ttu-id="8c759-106">Polecenie **cmdlet Get-AzFrontDoorRulesEngine** pobiera określoną konfigurację aparatu reguł lub wszystkie konfiguracje aparatów reguł skojarzone z drzwiami frontonu.</span><span class="sxs-lookup"><span data-stu-id="8c759-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="8c759-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c759-107">EXAMPLES</span></span>

### <span data-ttu-id="8c759-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8c759-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="8c759-109">Uzyskaj konkretną konfigurację aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="8c759-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="8c759-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8c759-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="8c759-111">Uzyskaj wszystkie konfiguracje aparatów reguł w drzwiach frontowych.</span><span class="sxs-lookup"><span data-stu-id="8c759-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="8c759-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8c759-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="8c759-113">Oczekiwane dane wyjściowe podczas uzyskiwania nieistniejącego aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="8c759-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="8c759-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c759-114">PARAMETERS</span></span>

### <span data-ttu-id="8c759-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c759-115">-DefaultProfile</span></span>
<span data-ttu-id="8c759-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c759-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c759-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8c759-117">-FrontDoorName</span></span>
<span data-ttu-id="8c759-118">Nazwa drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="8c759-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c759-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8c759-119">-Name</span></span>
<span data-ttu-id="8c759-120">Nazwa aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="8c759-120">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c759-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c759-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c759-122">Nazwa grupy zasobów, w przypadku których zostanie utworzona brama frontowa.</span><span class="sxs-lookup"><span data-stu-id="8c759-122">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c759-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c759-123">CommonParameters</span></span>
<span data-ttu-id="8c759-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c759-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c759-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c759-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c759-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c759-126">INPUTS</span></span>

### <span data-ttu-id="8c759-127">Brak</span><span class="sxs-lookup"><span data-stu-id="8c759-127">None</span></span>

## <span data-ttu-id="8c759-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c759-128">OUTPUTS</span></span>

### <span data-ttu-id="8c759-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="8c759-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="8c759-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c759-130">NOTES</span></span>

## <span data-ttu-id="8c759-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c759-131">RELATED LINKS</span></span>
