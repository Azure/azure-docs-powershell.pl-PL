---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896249"
---
# <span data-ttu-id="bbf10-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="bbf10-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="bbf10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bbf10-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf10-103">Zatrzymuje sesję debugowania przepływu danych w usłudze Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="bbf10-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="bbf10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bbf10-104">SYNTAX</span></span>

### <span data-ttu-id="bbf10-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bbf10-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbf10-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bbf10-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbf10-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bbf10-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbf10-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bbf10-108">DESCRIPTION</span></span>
<span data-ttu-id="bbf10-109">To polecenie zatrzymuje sesję debugowania, w przeciwnym razie sesja będzie automatycznie wyłączana w zależności od czasu na ustawienie sesji debugowania.</span><span class="sxs-lookup"><span data-stu-id="bbf10-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="bbf10-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bbf10-110">EXAMPLES</span></span>

### <span data-ttu-id="bbf10-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bbf10-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="bbf10-112">Zatrzymuje sesję debugowania przepływu danych "fd76cd0d-8b37-4dc0-A370-3f9d43ac686d" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="bbf10-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="bbf10-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bbf10-113">PARAMETERS</span></span>

### <span data-ttu-id="bbf10-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bbf10-114">-DataFactory</span></span>
<span data-ttu-id="bbf10-115">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="bbf10-115">The data factory object.</span></span>

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

### <span data-ttu-id="bbf10-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="bbf10-116">-DataFactoryName</span></span>
<span data-ttu-id="bbf10-117">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="bbf10-117">The data factory name.</span></span>

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

### <span data-ttu-id="bbf10-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf10-118">-DefaultProfile</span></span>
<span data-ttu-id="bbf10-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf10-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbf10-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbf10-120">-PassThru</span></span>
<span data-ttu-id="bbf10-121">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="bbf10-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="bbf10-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="bbf10-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="bbf10-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbf10-123">-ResourceGroupName</span></span>
<span data-ttu-id="bbf10-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bbf10-124">The resource group name.</span></span>

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

### <span data-ttu-id="bbf10-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbf10-125">-ResourceId</span></span>
<span data-ttu-id="bbf10-126">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf10-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="bbf10-127">-Identyfikator_sesji</span><span class="sxs-lookup"><span data-stu-id="bbf10-127">-SessionId</span></span>
<span data-ttu-id="bbf10-128">Identyfikator sesji debugowania przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="bbf10-128">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="bbf10-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bbf10-129">-Confirm</span></span>
<span data-ttu-id="bbf10-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbf10-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbf10-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbf10-131">-WhatIf</span></span>
<span data-ttu-id="bbf10-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbf10-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbf10-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bbf10-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbf10-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf10-134">CommonParameters</span></span>
<span data-ttu-id="bbf10-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbf10-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf10-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbf10-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf10-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbf10-137">INPUTS</span></span>

### <span data-ttu-id="bbf10-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bbf10-138">System.String</span></span>

### <span data-ttu-id="bbf10-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bbf10-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="bbf10-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bbf10-140">OUTPUTS</span></span>

### <span data-ttu-id="bbf10-141">System. void</span><span class="sxs-lookup"><span data-stu-id="bbf10-141">System.Void</span></span>

### <span data-ttu-id="bbf10-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bbf10-142">System.Boolean</span></span>

## <span data-ttu-id="bbf10-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bbf10-143">NOTES</span></span>
<span data-ttu-id="bbf10-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="bbf10-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bbf10-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbf10-145">RELATED LINKS</span></span>

[<span data-ttu-id="bbf10-146">Start — AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="bbf10-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="bbf10-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="bbf10-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="bbf10-148">Dodaj-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="bbf10-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="bbf10-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="bbf10-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)