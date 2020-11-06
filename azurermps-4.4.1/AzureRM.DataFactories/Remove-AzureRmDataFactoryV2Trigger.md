---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 771097c11aceabb9bd2011c6024e469a37a39f4e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525530"
---
# <span data-ttu-id="e8692-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e8692-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="e8692-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8692-102">SYNOPSIS</span></span>
<span data-ttu-id="e8692-103">Usuwa wyzwalacz z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e8692-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8692-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8692-104">SYNTAX</span></span>

### <span data-ttu-id="e8692-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e8692-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8692-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8692-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8692-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8692-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8692-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e8692-108">DESCRIPTION</span></span>
<span data-ttu-id="e8692-109">Polecenie cmdlet **Remove-AzureRmDataFactoryV2Trigger** usuwa wyzwalacz z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e8692-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="e8692-110">Jeśli parametr _Force_ jest określony, przed usunięciem wyzwalacza nie jest wyświetlany monit cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8692-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="e8692-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8692-111">EXAMPLES</span></span>

### <span data-ttu-id="e8692-112">Przykład 1: usuwanie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="e8692-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="e8692-113">Usuwanie wyzwalacza o nazwie "ScheduledTrigger" z fabryki danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="e8692-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="e8692-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8692-114">PARAMETERS</span></span>

### <span data-ttu-id="e8692-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8692-115">-Confirm</span></span>
<span data-ttu-id="e8692-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8692-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8692-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e8692-117">-DataFactoryName</span></span>
<span data-ttu-id="e8692-118">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e8692-118">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8692-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e8692-119">-Force</span></span>
<span data-ttu-id="e8692-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e8692-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8692-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8692-121">-Name</span></span>
<span data-ttu-id="e8692-122">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="e8692-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8692-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8692-123">-ResourceGroupName</span></span>
<span data-ttu-id="e8692-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8692-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8692-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8692-125">-ResourceId</span></span>
<span data-ttu-id="e8692-126">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e8692-126">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8692-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e8692-127">-InputObject</span></span>
<span data-ttu-id="e8692-128">Obiekt wyzwalacza do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e8692-128">The Trigger object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8692-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8692-129">-WhatIf</span></span>
<span data-ttu-id="e8692-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8692-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e8692-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8692-131">-DefaultProfile</span></span>
<span data-ttu-id="e8692-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8692-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8692-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8692-133">CommonParameters</span></span>
<span data-ttu-id="e8692-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8692-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8692-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8692-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8692-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8692-136">INPUTS</span></span>

### <span data-ttu-id="e8692-137">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="e8692-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="e8692-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e8692-138">System.String</span></span>

## <span data-ttu-id="e8692-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8692-139">OUTPUTS</span></span>

### <span data-ttu-id="e8692-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="e8692-140">System.Object</span></span>

## <span data-ttu-id="e8692-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8692-141">NOTES</span></span>

## <span data-ttu-id="e8692-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8692-142">RELATED LINKS</span></span>

[<span data-ttu-id="e8692-143">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e8692-143">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e8692-144">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e8692-144">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e8692-145">Start — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e8692-145">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e8692-146">Zatrzymaj — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e8692-146">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

