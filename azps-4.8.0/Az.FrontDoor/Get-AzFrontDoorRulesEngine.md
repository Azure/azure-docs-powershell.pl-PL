---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223924"
---
# <span data-ttu-id="c5270-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="c5270-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="c5270-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5270-102">SYNOPSIS</span></span>
<span data-ttu-id="c5270-103">Pobierz reguły konfiguracji aparatu.</span><span class="sxs-lookup"><span data-stu-id="c5270-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="c5270-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5270-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5270-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c5270-105">DESCRIPTION</span></span>
<span data-ttu-id="c5270-106">Polecenie cmdlet **Get-AzFrontDoorRulesEngine** pobiera określoną konfigurację aparatu reguł lub wszystkie konfiguracje aparatów skojarzonych z przednim drzwiem.</span><span class="sxs-lookup"><span data-stu-id="c5270-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="c5270-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5270-107">EXAMPLES</span></span>

### <span data-ttu-id="c5270-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c5270-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="c5270-109">Uzyskiwanie konfiguracji aparatu określonej reguły.</span><span class="sxs-lookup"><span data-stu-id="c5270-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="c5270-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c5270-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="c5270-111">Pobierz wszystkie reguły konfiguracji aparatu w przednich drzwiach.</span><span class="sxs-lookup"><span data-stu-id="c5270-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="c5270-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c5270-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="c5270-113">Podczas uzyskiwania nieistniejącego aparatu reguł oczekiwano danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c5270-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="c5270-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5270-114">PARAMETERS</span></span>

### <span data-ttu-id="c5270-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5270-115">-DefaultProfile</span></span>
<span data-ttu-id="c5270-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5270-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5270-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c5270-117">-FrontDoorName</span></span>
<span data-ttu-id="c5270-118">Imię i nazwisko drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="c5270-118">Front Door name.</span></span>

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

### <span data-ttu-id="c5270-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c5270-119">-Name</span></span>
<span data-ttu-id="c5270-120">Nazwa aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="c5270-120">Rules engine name.</span></span>

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

### <span data-ttu-id="c5270-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5270-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5270-122">Nazwa grupy zasobów, w której zostaną utworzone drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="c5270-122">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="c5270-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5270-123">CommonParameters</span></span>
<span data-ttu-id="c5270-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5270-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5270-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5270-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5270-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5270-126">INPUTS</span></span>

### <span data-ttu-id="c5270-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c5270-127">None</span></span>

## <span data-ttu-id="c5270-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5270-128">OUTPUTS</span></span>

### <span data-ttu-id="c5270-129">Microsoft. Azure. Commands. FrontDoor. models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="c5270-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="c5270-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5270-130">NOTES</span></span>

## <span data-ttu-id="c5270-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5270-131">RELATED LINKS</span></span>
