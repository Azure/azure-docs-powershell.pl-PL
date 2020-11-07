---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 45419ede425b5d5ea3ba9fcbbbfb024fe8ba9358
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706006"
---
# <span data-ttu-id="24f65-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="24f65-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="24f65-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24f65-102">SYNOPSIS</span></span>
<span data-ttu-id="24f65-103">Akcja Debuguj w sesji debugowania przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="24f65-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="24f65-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24f65-104">SYNTAX</span></span>

### <span data-ttu-id="24f65-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="24f65-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24f65-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="24f65-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24f65-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24f65-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24f65-108">Opis</span><span class="sxs-lookup"><span data-stu-id="24f65-108">DESCRIPTION</span></span>
<span data-ttu-id="24f65-109">To polecenie wykonuje Podgląd danych/podgląd statystyk/Podgląd wyrażeń dla różnych strumieni przepływu danych w sesji debugowania.</span><span class="sxs-lookup"><span data-stu-id="24f65-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="24f65-110">Sekwencja poleceń programu PowerShell dla przepływu pracy debugowania przepływu danych powinna być:</span><span class="sxs-lookup"><span data-stu-id="24f65-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="24f65-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="24f65-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="24f65-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="24f65-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="24f65-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (Powtórz ten krok dla różnych poleceń/obiektów docelowych) lub Powtórz krok 2-3 w celu zmiany pliku pakietu)</span><span class="sxs-lookup"><span data-stu-id="24f65-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="24f65-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="24f65-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="24f65-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24f65-115">EXAMPLES</span></span>

### <span data-ttu-id="24f65-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24f65-116">Example 1</span></span>
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

<span data-ttu-id="24f65-117">Ten przykład wywołuje polecenie Podgląd danych dla sesji debug "fd76cd0d-8b37-4dc0-A370-3f9d43ac686d" w fabryce danych "WiKiADF", a następnie Konwertuj dane wyjściowe w formacie JSON na ciąg czytelny.</span><span class="sxs-lookup"><span data-stu-id="24f65-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="24f65-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24f65-118">PARAMETERS</span></span>

### <span data-ttu-id="24f65-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24f65-119">-AsJob</span></span>
<span data-ttu-id="24f65-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="24f65-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24f65-121">-Columns</span><span class="sxs-lookup"><span data-stu-id="24f65-121">-Columns</span></span>
<span data-ttu-id="24f65-122">Lista kolumny dla podglądu statystyk przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="24f65-122">The columns list for data flow statistics preview.</span></span>

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

### <span data-ttu-id="24f65-123">-Command</span><span class="sxs-lookup"><span data-stu-id="24f65-123">-Command</span></span>
<span data-ttu-id="24f65-124">Polecenie Debuguj przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="24f65-124">The data flow debug command.</span></span> <span data-ttu-id="24f65-125">Argument opcjonalne to executePreviewQuery, executeStatisticsQuery i executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="24f65-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

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

### <span data-ttu-id="24f65-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="24f65-126">-DataFactory</span></span>
<span data-ttu-id="24f65-127">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="24f65-127">The data factory object.</span></span>

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

### <span data-ttu-id="24f65-128">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="24f65-128">-DataFactoryName</span></span>
<span data-ttu-id="24f65-129">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="24f65-129">The data factory name.</span></span>

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

### <span data-ttu-id="24f65-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f65-130">-DefaultProfile</span></span>
<span data-ttu-id="24f65-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24f65-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24f65-132">-Wyrażenie</span><span class="sxs-lookup"><span data-stu-id="24f65-132">-Expression</span></span>
<span data-ttu-id="24f65-133">Wyrażenie dla podglądu wyrażenia przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="24f65-133">The expression for data flow expression preview.</span></span>

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

### <span data-ttu-id="24f65-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f65-134">-ResourceGroupName</span></span>
<span data-ttu-id="24f65-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="24f65-135">The resource group name.</span></span>

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

### <span data-ttu-id="24f65-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24f65-136">-ResourceId</span></span>
<span data-ttu-id="24f65-137">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="24f65-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="24f65-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="24f65-138">-RowLimits</span></span>
<span data-ttu-id="24f65-139">Limit wierszy dla podglądu danych przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="24f65-139">The row limit for data flow data preview.</span></span>

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

### <span data-ttu-id="24f65-140">-Identyfikator_sesji</span><span class="sxs-lookup"><span data-stu-id="24f65-140">-SessionId</span></span>
<span data-ttu-id="24f65-141">Identyfikator sesji debugowania przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="24f65-141">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="24f65-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="24f65-142">-StreamName</span></span>
<span data-ttu-id="24f65-143">Nazwa strumienia przepływu danych do debugowania.</span><span class="sxs-lookup"><span data-stu-id="24f65-143">The stream name of data flow for debugging.</span></span>

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

### <span data-ttu-id="24f65-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24f65-144">-Confirm</span></span>
<span data-ttu-id="24f65-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24f65-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24f65-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24f65-146">-WhatIf</span></span>
<span data-ttu-id="24f65-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24f65-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24f65-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24f65-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24f65-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f65-149">CommonParameters</span></span>
<span data-ttu-id="24f65-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24f65-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f65-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24f65-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f65-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24f65-152">INPUTS</span></span>

### <span data-ttu-id="24f65-153">System. String</span><span class="sxs-lookup"><span data-stu-id="24f65-153">System.String</span></span>

### <span data-ttu-id="24f65-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="24f65-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="24f65-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24f65-155">OUTPUTS</span></span>

### <span data-ttu-id="24f65-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="24f65-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="24f65-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24f65-157">NOTES</span></span>
<span data-ttu-id="24f65-158">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, factoriesKeywords: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="24f65-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="24f65-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24f65-159">RELATED LINKS</span></span>

[<span data-ttu-id="24f65-160">Start — AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="24f65-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="24f65-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="24f65-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="24f65-162">Dodaj-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="24f65-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="24f65-163">Zatrzymaj — AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="24f65-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
