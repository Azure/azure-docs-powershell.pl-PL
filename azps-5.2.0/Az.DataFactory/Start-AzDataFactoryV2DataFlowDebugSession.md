---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 27a7f0ee401f044cc693cecf103f2bed1e8ce946
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324483"
---
# <span data-ttu-id="a1d1f-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a1d1f-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="a1d1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d1f-103">Rozpoczynanie sesji debugowania przepływu danych w usłudze Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="a1d1f-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="a1d1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1d1f-104">SYNTAX</span></span>

### <span data-ttu-id="a1d1f-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a1d1f-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d1f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a1d1f-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1d1f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d1f-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1d1f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a1d1f-108">DESCRIPTION</span></span>
<span data-ttu-id="a1d1f-109">To długie uruchomione polecenie rozpoczyna sesję debugowania przepływu danych dla nadchodzących poleceń debugowania.</span><span class="sxs-lookup"><span data-stu-id="a1d1f-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="a1d1f-110">To polecenie może zostać dołączone za pomocą definicji środowiska uruchomieniowego integracji w celu skonfigurowania rozmiaru/typu klastra sesji debugowania.</span><span class="sxs-lookup"><span data-stu-id="a1d1f-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="a1d1f-111">Sekwencja poleceń programu PowerShell dla przepływu pracy debugowania przepływu danych powinna być:</span><span class="sxs-lookup"><span data-stu-id="a1d1f-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="a1d1f-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a1d1f-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="a1d1f-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="a1d1f-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="a1d1f-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (Powtórz ten krok dla różnych poleceń/obiektów docelowych) lub Powtórz krok 2-3 w celu zmiany pliku pakietu)</span><span class="sxs-lookup"><span data-stu-id="a1d1f-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="a1d1f-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a1d1f-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="a1d1f-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1d1f-116">EXAMPLES</span></span>

### <span data-ttu-id="a1d1f-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a1d1f-117">Example 1</span></span>
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

<span data-ttu-id="a1d1f-118">Rozpoczyna sesję debugowania z flagą AsJob.</span><span class="sxs-lookup"><span data-stu-id="a1d1f-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="a1d1f-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1d1f-119">PARAMETERS</span></span>

### <span data-ttu-id="a1d1f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1d1f-120">-AsJob</span></span>
<span data-ttu-id="a1d1f-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a1d1f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1d1f-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a1d1f-122">-DataFactory</span></span>
<span data-ttu-id="a1d1f-123">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="a1d1f-123">The data factory object.</span></span>

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

### <span data-ttu-id="a1d1f-124">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a1d1f-124">-DataFactoryName</span></span>
<span data-ttu-id="a1d1f-125">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="a1d1f-125">The data factory name.</span></span>

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

### <span data-ttu-id="a1d1f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d1f-126">-DefaultProfile</span></span>
<span data-ttu-id="a1d1f-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d1f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1d1f-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="a1d1f-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="a1d1f-129">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="a1d1f-129">The JSON file path.</span></span>

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

### <span data-ttu-id="a1d1f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d1f-130">-ResourceGroupName</span></span>
<span data-ttu-id="a1d1f-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1d1f-131">The resource group name.</span></span>

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

### <span data-ttu-id="a1d1f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d1f-132">-ResourceId</span></span>
<span data-ttu-id="a1d1f-133">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d1f-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a1d1f-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1d1f-134">-Confirm</span></span>
<span data-ttu-id="a1d1f-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1d1f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1d1f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d1f-136">-WhatIf</span></span>
<span data-ttu-id="a1d1f-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1d1f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1d1f-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a1d1f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1d1f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d1f-139">CommonParameters</span></span>
<span data-ttu-id="a1d1f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1d1f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d1f-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1d1f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d1f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1d1f-142">INPUTS</span></span>

### <span data-ttu-id="a1d1f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a1d1f-143">System.String</span></span>

### <span data-ttu-id="a1d1f-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a1d1f-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a1d1f-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1d1f-145">OUTPUTS</span></span>

### <span data-ttu-id="a1d1f-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a1d1f-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="a1d1f-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1d1f-147">NOTES</span></span>
<span data-ttu-id="a1d1f-148">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="a1d1f-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a1d1f-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1d1f-149">RELATED LINKS</span></span>

[<span data-ttu-id="a1d1f-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a1d1f-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="a1d1f-151">Dodaj-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="a1d1f-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="a1d1f-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="a1d1f-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="a1d1f-153">Zatrzymaj — AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a1d1f-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)