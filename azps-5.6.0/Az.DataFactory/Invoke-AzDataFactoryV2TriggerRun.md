---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 91eb23f3af613cf349219f82d133d08dd6e65b5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975018"
---
# <span data-ttu-id="10168-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="10168-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="10168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10168-102">SYNOPSIS</span></span>
 <span data-ttu-id="10168-103">Wywołuje kolejne wystąpienie uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="10168-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="10168-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10168-104">SYNTAX</span></span>

### <span data-ttu-id="10168-105">ByFactoryNameByParameterFile (domyślne)</span><span class="sxs-lookup"><span data-stu-id="10168-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10168-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="10168-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10168-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="10168-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10168-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="10168-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10168-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="10168-109">DESCRIPTION</span></span>
<span data-ttu-id="10168-110">Polecenie **Invoke-AzDataFactoryV2TriggerRun** uruchamia kolejne wystąpienie uruchomienia wyzwalacza z nowym identyfikatorem uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="10168-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="10168-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10168-111">EXAMPLES</span></span>

### <span data-ttu-id="10168-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10168-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="10168-113">Uruchamia kolejne wystąpienie uruchomienia wyzwalacza z nowym identyfikatorem uruchomienia wyzwalacza, zachowując ten sam identyfikator windowStartTime i windowEndTime co oryginalne uruchomienie wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="10168-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="10168-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10168-114">PARAMETERS</span></span>

### <span data-ttu-id="10168-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="10168-115">-DataFactory</span></span>
<span data-ttu-id="10168-116">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="10168-116">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10168-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="10168-117">-DataFactoryName</span></span>
<span data-ttu-id="10168-118">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="10168-118">The data factory name.</span></span>

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

### <span data-ttu-id="10168-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10168-119">-DefaultProfile</span></span>
<span data-ttu-id="10168-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10168-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10168-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10168-121">-InputObject</span></span>
<span data-ttu-id="10168-122">Informacje o uruchomieniu wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="10168-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10168-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10168-123">-PassThru</span></span>
<span data-ttu-id="10168-124">Jeśli określono polecenie cmdlet write true (zapisz na wypadek, gdyby operacja zakończyła się powodzeniem).</span><span class="sxs-lookup"><span data-stu-id="10168-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="10168-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10168-125">-ResourceGroupName</span></span>
<span data-ttu-id="10168-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10168-126">The resource group name.</span></span>

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

### <span data-ttu-id="10168-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="10168-127">-TriggerName</span></span>
<span data-ttu-id="10168-128">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="10168-128">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10168-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="10168-129">-TriggerRunId</span></span>
<span data-ttu-id="10168-130">Identyfikator uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="10168-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10168-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10168-131">-Confirm</span></span>
<span data-ttu-id="10168-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="10168-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10168-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10168-133">-WhatIf</span></span>
<span data-ttu-id="10168-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10168-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10168-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="10168-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10168-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10168-136">CommonParameters</span></span>
<span data-ttu-id="10168-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10168-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10168-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10168-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10168-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10168-139">INPUTS</span></span>

### <span data-ttu-id="10168-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="10168-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="10168-141">System.String</span><span class="sxs-lookup"><span data-stu-id="10168-141">System.String</span></span>

### <span data-ttu-id="10168-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="10168-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="10168-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10168-143">OUTPUTS</span></span>

### <span data-ttu-id="10168-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="10168-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="10168-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10168-145">NOTES</span></span>

## <span data-ttu-id="10168-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10168-146">RELATED LINKS</span></span>
