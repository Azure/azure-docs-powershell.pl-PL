---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 4009835b2efe8346ff873bde59870954c73ab5d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371903"
---
# <span data-ttu-id="0911e-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="0911e-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="0911e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0911e-102">SYNOPSIS</span></span>
<span data-ttu-id="0911e-103">Akcja Debuguj w sesji debugowania przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="0911e-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="0911e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0911e-104">SYNTAX</span></span>

### <span data-ttu-id="0911e-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0911e-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0911e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0911e-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0911e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0911e-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0911e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0911e-108">DESCRIPTION</span></span>
<span data-ttu-id="0911e-109">To polecenie wykonuje Podgląd danych/podgląd statystyk/Podgląd wyrażeń dla różnych strumieni przepływu danych w sesji debugowania.</span><span class="sxs-lookup"><span data-stu-id="0911e-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="0911e-110">Sekwencja poleceń programu PowerShell dla przepływu pracy debugowania przepływu danych powinna być:</span><span class="sxs-lookup"><span data-stu-id="0911e-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="0911e-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="0911e-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="0911e-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="0911e-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="0911e-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (Powtórz ten krok dla różnych poleceń/obiektów docelowych) lub Powtórz krok 2-3 w celu zmiany pliku pakietu)</span><span class="sxs-lookup"><span data-stu-id="0911e-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="0911e-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="0911e-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="0911e-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0911e-115">EXAMPLES</span></span>

### <span data-ttu-id="0911e-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0911e-116">Example 1</span></span>
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

<span data-ttu-id="0911e-117">Ten przykład wywołuje polecenie Podgląd danych dla sesji debug "fd76cd0d-8b37-4dc0-A370-3f9d43ac686d" w fabryce danych "WiKiADF", a następnie Konwertuj dane wyjściowe w formacie JSON na ciąg czytelny.</span><span class="sxs-lookup"><span data-stu-id="0911e-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="0911e-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0911e-118">PARAMETERS</span></span>

### <span data-ttu-id="0911e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0911e-119">-AsJob</span></span>
<span data-ttu-id="0911e-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0911e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0911e-121">-Columns</span><span class="sxs-lookup"><span data-stu-id="0911e-121">-Columns</span></span>
<span data-ttu-id="0911e-122">Lista kolumny dla podglądu statystyk przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="0911e-122">The columns list for data flow statistics preview.</span></span>

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

### <span data-ttu-id="0911e-123">-Command</span><span class="sxs-lookup"><span data-stu-id="0911e-123">-Command</span></span>
<span data-ttu-id="0911e-124">Polecenie Debuguj przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="0911e-124">The data flow debug command.</span></span> <span data-ttu-id="0911e-125">Argument opcjonalne to executePreviewQuery, executeStatisticsQuery i executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="0911e-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

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

### <span data-ttu-id="0911e-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0911e-126">-DataFactory</span></span>
<span data-ttu-id="0911e-127">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0911e-127">The data factory object.</span></span>

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

### <span data-ttu-id="0911e-128">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0911e-128">-DataFactoryName</span></span>
<span data-ttu-id="0911e-129">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0911e-129">The data factory name.</span></span>

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

### <span data-ttu-id="0911e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0911e-130">-DefaultProfile</span></span>
<span data-ttu-id="0911e-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0911e-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0911e-132">-Wyrażenie</span><span class="sxs-lookup"><span data-stu-id="0911e-132">-Expression</span></span>
<span data-ttu-id="0911e-133">Wyrażenie dla podglądu wyrażenia przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="0911e-133">The expression for data flow expression preview.</span></span>

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

### <span data-ttu-id="0911e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0911e-134">-ResourceGroupName</span></span>
<span data-ttu-id="0911e-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0911e-135">The resource group name.</span></span>

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

### <span data-ttu-id="0911e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0911e-136">-ResourceId</span></span>
<span data-ttu-id="0911e-137">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0911e-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0911e-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="0911e-138">-RowLimits</span></span>
<span data-ttu-id="0911e-139">Limit wierszy dla podglądu danych przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="0911e-139">The row limit for data flow data preview.</span></span>

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

### <span data-ttu-id="0911e-140">-Identyfikator_sesji</span><span class="sxs-lookup"><span data-stu-id="0911e-140">-SessionId</span></span>
<span data-ttu-id="0911e-141">Identyfikator sesji debugowania przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="0911e-141">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="0911e-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="0911e-142">-StreamName</span></span>
<span data-ttu-id="0911e-143">Nazwa strumienia przepływu danych do debugowania.</span><span class="sxs-lookup"><span data-stu-id="0911e-143">The stream name of data flow for debugging.</span></span>

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

### <span data-ttu-id="0911e-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0911e-144">-Confirm</span></span>
<span data-ttu-id="0911e-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0911e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0911e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0911e-146">-WhatIf</span></span>
<span data-ttu-id="0911e-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0911e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0911e-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0911e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0911e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0911e-149">CommonParameters</span></span>
<span data-ttu-id="0911e-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0911e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0911e-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0911e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0911e-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0911e-152">INPUTS</span></span>

### <span data-ttu-id="0911e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="0911e-153">System.String</span></span>

### <span data-ttu-id="0911e-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0911e-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0911e-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0911e-155">OUTPUTS</span></span>

### <span data-ttu-id="0911e-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="0911e-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="0911e-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0911e-157">NOTES</span></span>
<span data-ttu-id="0911e-158">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, factoriesKeywords: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="0911e-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0911e-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0911e-159">RELATED LINKS</span></span>

[<span data-ttu-id="0911e-160">Start — AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="0911e-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="0911e-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="0911e-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="0911e-162">Dodaj-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="0911e-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="0911e-163">Zatrzymaj — AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="0911e-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
