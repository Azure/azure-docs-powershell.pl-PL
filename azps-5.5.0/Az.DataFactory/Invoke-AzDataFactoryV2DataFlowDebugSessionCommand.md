---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 4009835b2efe8346ff873bde59870954c73ab5d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198178"
---
# <span data-ttu-id="a4cff-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="a4cff-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="a4cff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4cff-102">SYNOPSIS</span></span>
<span data-ttu-id="a4cff-103">Wywołaj akcję debugowania w sesji debugowania przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="a4cff-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="a4cff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a4cff-104">SYNTAX</span></span>

### <span data-ttu-id="a4cff-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="a4cff-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4cff-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a4cff-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4cff-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a4cff-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4cff-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a4cff-108">DESCRIPTION</span></span>
<span data-ttu-id="a4cff-109">To polecenie wykonuje podgląd danych/podgląd statystyk/podgląd wyrażenia dla innego strumienia przepływu danych w sesji debugowania.</span><span class="sxs-lookup"><span data-stu-id="a4cff-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="a4cff-110">Sekwencja poleceń programu PowerShell dla przepływu pracy debugowania przepływu danych powinna być:</span><span class="sxs-lookup"><span data-stu-id="a4cff-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="a4cff-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a4cff-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="a4cff-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="a4cff-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="a4cff-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (powtórz ten krok dla różnych poleceń/celów lub powtórz krok 2-3, aby zmienić plik pakietu)</span><span class="sxs-lookup"><span data-stu-id="a4cff-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="a4cff-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a4cff-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="a4cff-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a4cff-115">EXAMPLES</span></span>

### <span data-ttu-id="a4cff-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4cff-116">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $result = Invoke-AzDataFactoryV2DataFlowDebugSessionCommand -ResourceGroupName adf -DataFactoryName WiKiADF -Command executePreviewQuery -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d -StreamName source1 -RowLimits 100 -AsJob
PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Running       True            localhost            Invoke-AzDataFactoryV2...


(After 2 minutes)

PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Completed     True            localhost            Invoke-AzDataFactoryV2...

PS C:\WINDOWS\system32> $output = ConvertFrom-Json($result.Output.Data)
PS C:\WINDOWS\system32> $output.output

    {
      "schema": "output(ResourceAgencyNum as string, PublicName as string)" ,
      "data": [["4445679354", "Syrian Refugee Information", 1], ["44456793", "Syrian Refugee Information", 1]]
    }


```

<span data-ttu-id="a4cff-117">W tym przykładzie jest wywoływane polecenie podglądu danych dla sesji debugowania "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" w factory danych "WiKiADF", a następnie konwertowanie danych wyjściowych JSON na ciąg czytelny.</span><span class="sxs-lookup"><span data-stu-id="a4cff-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="a4cff-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4cff-118">PARAMETERS</span></span>

### <span data-ttu-id="a4cff-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a4cff-119">-AsJob</span></span>
<span data-ttu-id="a4cff-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a4cff-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4cff-121">— Kolumny</span><span class="sxs-lookup"><span data-stu-id="a4cff-121">-Columns</span></span>
<span data-ttu-id="a4cff-122">Lista kolumn dla podglądu statystyki przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="a4cff-122">The columns list for data flow statistics preview.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4cff-123">- Command</span><span class="sxs-lookup"><span data-stu-id="a4cff-123">-Command</span></span>
<span data-ttu-id="a4cff-124">Polecenie debugowania przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="a4cff-124">The data flow debug command.</span></span> <span data-ttu-id="a4cff-125">Opcjonalnie: executePreviewQuery, executeStatisticsQuery i executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="a4cff-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4cff-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a4cff-126">-DataFactory</span></span>
<span data-ttu-id="a4cff-127">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="a4cff-127">The data factory object.</span></span>

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

### <span data-ttu-id="a4cff-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a4cff-128">-DataFactoryName</span></span>
<span data-ttu-id="a4cff-129">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="a4cff-129">The data factory name.</span></span>

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

### <span data-ttu-id="a4cff-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4cff-130">-DefaultProfile</span></span>
<span data-ttu-id="a4cff-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4cff-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4cff-132">-Expression</span><span class="sxs-lookup"><span data-stu-id="a4cff-132">-Expression</span></span>
<span data-ttu-id="a4cff-133">Wyrażenie podglądu wyrażenia przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="a4cff-133">The expression for data flow expression preview.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4cff-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4cff-134">-ResourceGroupName</span></span>
<span data-ttu-id="a4cff-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4cff-135">The resource group name.</span></span>

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

### <span data-ttu-id="a4cff-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4cff-136">-ResourceId</span></span>
<span data-ttu-id="a4cff-137">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="a4cff-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a4cff-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="a4cff-138">-RowLimits</span></span>
<span data-ttu-id="a4cff-139">Limit wierszy dla podglądu danych przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="a4cff-139">The row limit for data flow data preview.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4cff-140">- SessionId</span><span class="sxs-lookup"><span data-stu-id="a4cff-140">-SessionId</span></span>
<span data-ttu-id="a4cff-141">Identyfikator sesji debugowania przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="a4cff-141">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4cff-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="a4cff-142">-StreamName</span></span>
<span data-ttu-id="a4cff-143">Nazwa przepływu danych strumienia do debugowania.</span><span class="sxs-lookup"><span data-stu-id="a4cff-143">The stream name of data flow for debugging.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4cff-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4cff-144">-Confirm</span></span>
<span data-ttu-id="a4cff-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4cff-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4cff-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4cff-146">-WhatIf</span></span>
<span data-ttu-id="a4cff-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4cff-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4cff-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a4cff-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4cff-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4cff-149">CommonParameters</span></span>
<span data-ttu-id="a4cff-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4cff-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4cff-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4cff-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4cff-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4cff-152">INPUTS</span></span>

### <span data-ttu-id="a4cff-153">System.String</span><span class="sxs-lookup"><span data-stu-id="a4cff-153">System.String</span></span>

### <span data-ttu-id="a4cff-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a4cff-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a4cff-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4cff-155">OUTPUTS</span></span>

### <span data-ttu-id="a4cff-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="a4cff-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="a4cff-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a4cff-157">NOTES</span></span>
<span data-ttu-id="a4cff-158">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="a4cff-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a4cff-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4cff-159">RELATED LINKS</span></span>

[<span data-ttu-id="a4cff-160">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a4cff-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="a4cff-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a4cff-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="a4cff-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="a4cff-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="a4cff-163">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a4cff-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
