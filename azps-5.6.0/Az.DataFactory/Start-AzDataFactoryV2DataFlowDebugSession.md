---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: be94460a2296874acefab3232f4a73d394a523d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964913"
---
# <span data-ttu-id="74c95-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="74c95-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="74c95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74c95-102">SYNOPSIS</span></span>
<span data-ttu-id="74c95-103">Rozpoczynanie sesji debugowania przepływu danych w usłudze Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="74c95-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="74c95-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74c95-104">SYNTAX</span></span>

### <span data-ttu-id="74c95-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="74c95-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74c95-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="74c95-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74c95-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="74c95-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74c95-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="74c95-108">DESCRIPTION</span></span>
<span data-ttu-id="74c95-109">To długo działające polecenie uruchamia sesję debugowania przepływu danych dla nadchodzących poleceń debugowania.</span><span class="sxs-lookup"><span data-stu-id="74c95-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="74c95-110">To polecenie można dołączyć z definicją środowiska uruchomieniowego integracji, aby skonfigurować rozmiar i typ klastrów sesji debugowania.</span><span class="sxs-lookup"><span data-stu-id="74c95-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="74c95-111">Sekwencja poleceń programu PowerShell dla przepływu pracy debugowania przepływu danych powinna być:</span><span class="sxs-lookup"><span data-stu-id="74c95-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="74c95-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="74c95-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="74c95-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="74c95-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="74c95-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (powtórz ten krok dla różnych poleceń/celów lub powtórz krok 2-3, aby zmienić plik pakietu)</span><span class="sxs-lookup"><span data-stu-id="74c95-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="74c95-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="74c95-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="74c95-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74c95-116">EXAMPLES</span></span>

### <span data-ttu-id="74c95-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="74c95-117">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $job = Start-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName jikma0601sea -AsJob
PS C:\WINDOWS\system32> $job 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            Start-AzDataFactoryV2D...

(After 5 minutes)

PS C:\WINDOWS\system32> $job

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Completed     True            localhost            Start-AzDataFactoryV2D...


PS C:\WINDOWS\system32> $job.Output

SessionId                            Status
---------                            ------
550effe4-93a3-485c-8525-eaf25259efbd Succeeded

```

<span data-ttu-id="74c95-118">Rozpoczyna sesję debugowania z flagą AsJob.</span><span class="sxs-lookup"><span data-stu-id="74c95-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="74c95-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74c95-119">PARAMETERS</span></span>

### <span data-ttu-id="74c95-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="74c95-120">-AsJob</span></span>
<span data-ttu-id="74c95-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="74c95-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74c95-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="74c95-122">-DataFactory</span></span>
<span data-ttu-id="74c95-123">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="74c95-123">The data factory object.</span></span>

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

### <span data-ttu-id="74c95-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="74c95-124">-DataFactoryName</span></span>
<span data-ttu-id="74c95-125">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="74c95-125">The data factory name.</span></span>

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

### <span data-ttu-id="74c95-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c95-126">-DefaultProfile</span></span>
<span data-ttu-id="74c95-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74c95-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74c95-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="74c95-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="74c95-129">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="74c95-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c95-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c95-130">-ResourceGroupName</span></span>
<span data-ttu-id="74c95-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74c95-131">The resource group name.</span></span>

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

### <span data-ttu-id="74c95-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74c95-132">-ResourceId</span></span>
<span data-ttu-id="74c95-133">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="74c95-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="74c95-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74c95-134">-Confirm</span></span>
<span data-ttu-id="74c95-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74c95-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74c95-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74c95-136">-WhatIf</span></span>
<span data-ttu-id="74c95-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74c95-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74c95-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="74c95-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74c95-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c95-139">CommonParameters</span></span>
<span data-ttu-id="74c95-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c95-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c95-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74c95-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c95-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74c95-142">INPUTS</span></span>

### <span data-ttu-id="74c95-143">System.String</span><span class="sxs-lookup"><span data-stu-id="74c95-143">System.String</span></span>

### <span data-ttu-id="74c95-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="74c95-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="74c95-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74c95-145">OUTPUTS</span></span>

### <span data-ttu-id="74c95-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="74c95-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="74c95-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74c95-147">NOTES</span></span>
<span data-ttu-id="74c95-148">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="74c95-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="74c95-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74c95-149">RELATED LINKS</span></span>

[<span data-ttu-id="74c95-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="74c95-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="74c95-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="74c95-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="74c95-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="74c95-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="74c95-153">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="74c95-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)