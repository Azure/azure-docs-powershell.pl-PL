---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 1e3310b99173c0a7fa83dcada286833747457213
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964874"
---
# <span data-ttu-id="c1d78-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="c1d78-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="c1d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1d78-102">SYNOPSIS</span></span>
<span data-ttu-id="c1d78-103">Powoduje zatrzymanie uruchomienia wyzwalacza w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="c1d78-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="c1d78-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c1d78-104">SYNTAX</span></span>

### <span data-ttu-id="c1d78-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="c1d78-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1d78-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c1d78-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1d78-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c1d78-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1d78-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c1d78-108">DESCRIPTION</span></span>
<span data-ttu-id="c1d78-109">Polecenie **cmdlet Stop-AzDataFactoryV2TriggerRun** zatrzymuje uruchomienie wyzwalacza w fabrycznej bazie danych określonej za pomocą nazwy wyzwalacza i identyfikatora uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="c1d78-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="c1d78-110">Obecnie obsługiwane tylko dla języka TumblingWindowTriggers w stanie WaitingOnDependency.</span><span class="sxs-lookup"><span data-stu-id="c1d78-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="c1d78-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c1d78-111">EXAMPLES</span></span>

### <span data-ttu-id="c1d78-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c1d78-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="c1d78-113">To polecenie powoduje zatrzymanie uruchomienia wyzwalacza o identyfikatorze "08586002468005888497807248799CU16" w fabrycznym pliku WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c1d78-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="c1d78-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1d78-114">PARAMETERS</span></span>

### <span data-ttu-id="c1d78-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1d78-115">-DataFactory</span></span>
<span data-ttu-id="c1d78-116">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="c1d78-116">The data factory object.</span></span>

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

### <span data-ttu-id="c1d78-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c1d78-117">-DataFactoryName</span></span>
<span data-ttu-id="c1d78-118">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="c1d78-118">The data factory name.</span></span>

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

### <span data-ttu-id="c1d78-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d78-119">-DefaultProfile</span></span>
<span data-ttu-id="c1d78-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1d78-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1d78-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1d78-121">-InputObject</span></span>
<span data-ttu-id="c1d78-122">Informacje o uruchomieniu wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="c1d78-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="c1d78-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1d78-123">-PassThru</span></span>
<span data-ttu-id="c1d78-124">Jeśli określono polecenie cmdlet write true (zapisz na wypadek, gdyby operacja zakończyła się powodzeniem).</span><span class="sxs-lookup"><span data-stu-id="c1d78-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="c1d78-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1d78-125">-ResourceGroupName</span></span>
<span data-ttu-id="c1d78-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c1d78-126">The resource group name.</span></span>

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

### <span data-ttu-id="c1d78-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="c1d78-127">-TriggerName</span></span>
<span data-ttu-id="c1d78-128">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="c1d78-128">The trigger name.</span></span>

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

### <span data-ttu-id="c1d78-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="c1d78-129">-TriggerRunId</span></span>
<span data-ttu-id="c1d78-130">Identyfikator uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="c1d78-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="c1d78-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1d78-131">-Confirm</span></span>
<span data-ttu-id="c1d78-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c1d78-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1d78-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1d78-133">-WhatIf</span></span>
<span data-ttu-id="c1d78-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1d78-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1d78-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c1d78-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1d78-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d78-136">CommonParameters</span></span>
<span data-ttu-id="c1d78-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1d78-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d78-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1d78-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d78-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1d78-139">INPUTS</span></span>

### <span data-ttu-id="c1d78-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="c1d78-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="c1d78-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c1d78-141">System.String</span></span>

### <span data-ttu-id="c1d78-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c1d78-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="c1d78-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1d78-143">OUTPUTS</span></span>

### <span data-ttu-id="c1d78-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1d78-144">System.Boolean</span></span>

## <span data-ttu-id="c1d78-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c1d78-145">NOTES</span></span>

## <span data-ttu-id="c1d78-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1d78-146">RELATED LINKS</span></span>
