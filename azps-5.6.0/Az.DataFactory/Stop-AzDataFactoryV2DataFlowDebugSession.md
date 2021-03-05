---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 21c8d30cfeec7e0138ec659074a94bd5914e5124
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006922"
---
# <span data-ttu-id="81944-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="81944-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="81944-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81944-102">SYNOPSIS</span></span>
<span data-ttu-id="81944-103">Zatrzymuje sesję debugowania przepływu danych w usłudze Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="81944-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="81944-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="81944-104">SYNTAX</span></span>

### <span data-ttu-id="81944-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="81944-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81944-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="81944-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81944-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="81944-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81944-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="81944-108">DESCRIPTION</span></span>
<span data-ttu-id="81944-109">To polecenie zatrzymuje sesję debugowania, jeśli nie, sesja zostanie automatycznie wyłączona zgodnie z ustawieniem czas na żywo sesji debugowania.</span><span class="sxs-lookup"><span data-stu-id="81944-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="81944-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="81944-110">EXAMPLES</span></span>

### <span data-ttu-id="81944-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81944-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="81944-112">Zatrzymuje sesję debugowania przepływu danych "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" w ustawieniach fabrycznych danych "WikiADF"</span><span class="sxs-lookup"><span data-stu-id="81944-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="81944-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81944-113">PARAMETERS</span></span>

### <span data-ttu-id="81944-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="81944-114">-DataFactory</span></span>
<span data-ttu-id="81944-115">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="81944-115">The data factory object.</span></span>

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

### <span data-ttu-id="81944-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="81944-116">-DataFactoryName</span></span>
<span data-ttu-id="81944-117">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="81944-117">The data factory name.</span></span>

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

### <span data-ttu-id="81944-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81944-118">-DefaultProfile</span></span>
<span data-ttu-id="81944-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="81944-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81944-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81944-120">-PassThru</span></span>
<span data-ttu-id="81944-121">Jeśli zostanie określona, w przypadku gdy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="81944-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="81944-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="81944-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="81944-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81944-123">-ResourceGroupName</span></span>
<span data-ttu-id="81944-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81944-124">The resource group name.</span></span>

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

### <span data-ttu-id="81944-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81944-125">-ResourceId</span></span>
<span data-ttu-id="81944-126">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="81944-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="81944-127">- SessionId</span><span class="sxs-lookup"><span data-stu-id="81944-127">-SessionId</span></span>
<span data-ttu-id="81944-128">Identyfikator sesji debugowania przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="81944-128">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81944-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81944-129">-Confirm</span></span>
<span data-ttu-id="81944-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="81944-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81944-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81944-131">-WhatIf</span></span>
<span data-ttu-id="81944-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81944-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81944-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="81944-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81944-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81944-134">CommonParameters</span></span>
<span data-ttu-id="81944-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81944-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81944-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81944-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81944-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81944-137">INPUTS</span></span>

### <span data-ttu-id="81944-138">System.String</span><span class="sxs-lookup"><span data-stu-id="81944-138">System.String</span></span>

### <span data-ttu-id="81944-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="81944-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="81944-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81944-140">OUTPUTS</span></span>

### <span data-ttu-id="81944-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="81944-141">System.Void</span></span>

### <span data-ttu-id="81944-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="81944-142">System.Boolean</span></span>

## <span data-ttu-id="81944-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="81944-143">NOTES</span></span>
<span data-ttu-id="81944-144">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="81944-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="81944-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81944-145">RELATED LINKS</span></span>

[<span data-ttu-id="81944-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="81944-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="81944-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="81944-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="81944-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="81944-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="81944-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="81944-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)