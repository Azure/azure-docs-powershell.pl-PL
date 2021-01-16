---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348874"
---
# <span data-ttu-id="e2694-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="e2694-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="e2694-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2694-102">SYNOPSIS</span></span>
<span data-ttu-id="e2694-103">Tworzenie nowej konfiguracji aparatu dla określonego przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="e2694-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="e2694-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2694-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2694-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e2694-105">DESCRIPTION</span></span>
<span data-ttu-id="e2694-106">Tworzenie nowej konfiguracji aparatu dla określonego przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="e2694-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="e2694-107">Użyj polecenia cmdlet "New-AzFrontDoorRulesEngineRule", aby skonstruować reguły aparatu, które zostaną przekazane do parametru "-Rules" tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2694-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="e2694-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2694-108">EXAMPLES</span></span>

### <span data-ttu-id="e2694-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e2694-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="e2694-110">Utwórz nowe reguły konfiguracji aparatu dla określonych przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="e2694-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="e2694-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2694-111">PARAMETERS</span></span>

### <span data-ttu-id="e2694-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2694-112">-DefaultProfile</span></span>
<span data-ttu-id="e2694-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2694-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2694-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="e2694-114">-FrontDoorName</span></span>
<span data-ttu-id="e2694-115">Imię i nazwisko drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="e2694-115">Front Door name.</span></span>

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

### <span data-ttu-id="e2694-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2694-116">-Name</span></span>
<span data-ttu-id="e2694-117">Nazwa aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="e2694-117">Rules engine name.</span></span>

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

### <span data-ttu-id="e2694-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2694-118">-ResourceGroupName</span></span>
<span data-ttu-id="e2694-119">Nazwa grupy zasobów, w której zostaną utworzone drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="e2694-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="e2694-120">— Reguła</span><span class="sxs-lookup"><span data-stu-id="e2694-120">-Rule</span></span>
<span data-ttu-id="e2694-121">Lista reguł, które definiują określoną konfigurację aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="e2694-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2694-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2694-122">-Confirm</span></span>
<span data-ttu-id="e2694-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2694-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2694-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2694-124">-WhatIf</span></span>
<span data-ttu-id="e2694-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2694-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2694-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e2694-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2694-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2694-127">CommonParameters</span></span>
<span data-ttu-id="e2694-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2694-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2694-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2694-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2694-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2694-130">INPUTS</span></span>

### <span data-ttu-id="e2694-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e2694-131">None</span></span>

## <span data-ttu-id="e2694-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2694-132">OUTPUTS</span></span>

### <span data-ttu-id="e2694-133">Microsoft. Azure. Commands. FrontDoor. models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="e2694-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="e2694-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2694-134">NOTES</span></span>

## <span data-ttu-id="e2694-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2694-135">RELATED LINKS</span></span>
