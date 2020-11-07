---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: def0ff5b525f4ced0ac1510fdc65b1dfd746cc6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705920"
---
# <span data-ttu-id="2f01f-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="2f01f-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="2f01f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f01f-102">SYNOPSIS</span></span>
<span data-ttu-id="2f01f-103">Zatrzymuje sesję debugowania przepływu danych w usłudze Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="2f01f-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="2f01f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f01f-104">SYNTAX</span></span>

### <span data-ttu-id="2f01f-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2f01f-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f01f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2f01f-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f01f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f01f-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f01f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2f01f-108">DESCRIPTION</span></span>
<span data-ttu-id="2f01f-109">To polecenie zatrzymuje sesję debugowania, w przeciwnym razie sesja będzie automatycznie wyłączana w zależności od czasu na ustawienie sesji debugowania.</span><span class="sxs-lookup"><span data-stu-id="2f01f-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="2f01f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f01f-110">EXAMPLES</span></span>

### <span data-ttu-id="2f01f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2f01f-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="2f01f-112">Zatrzymuje sesję debugowania przepływu danych "fd76cd0d-8b37-4dc0-A370-3f9d43ac686d" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="2f01f-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="2f01f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f01f-113">PARAMETERS</span></span>

### <span data-ttu-id="2f01f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2f01f-114">-DataFactory</span></span>
<span data-ttu-id="2f01f-115">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="2f01f-115">The data factory object.</span></span>

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

### <span data-ttu-id="2f01f-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2f01f-116">-DataFactoryName</span></span>
<span data-ttu-id="2f01f-117">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="2f01f-117">The data factory name.</span></span>

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

### <span data-ttu-id="2f01f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f01f-118">-DefaultProfile</span></span>
<span data-ttu-id="2f01f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f01f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f01f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f01f-120">-PassThru</span></span>
<span data-ttu-id="2f01f-121">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="2f01f-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="2f01f-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2f01f-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="2f01f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f01f-123">-ResourceGroupName</span></span>
<span data-ttu-id="2f01f-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2f01f-124">The resource group name.</span></span>

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

### <span data-ttu-id="2f01f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f01f-125">-ResourceId</span></span>
<span data-ttu-id="2f01f-126">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2f01f-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2f01f-127">-Identyfikator_sesji</span><span class="sxs-lookup"><span data-stu-id="2f01f-127">-SessionId</span></span>
<span data-ttu-id="2f01f-128">Identyfikator sesji debugowania przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="2f01f-128">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="2f01f-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f01f-129">-Confirm</span></span>
<span data-ttu-id="2f01f-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f01f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f01f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f01f-131">-WhatIf</span></span>
<span data-ttu-id="2f01f-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f01f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f01f-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f01f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f01f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f01f-134">CommonParameters</span></span>
<span data-ttu-id="2f01f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f01f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f01f-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f01f-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f01f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f01f-137">INPUTS</span></span>

### <span data-ttu-id="2f01f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2f01f-138">System.String</span></span>

### <span data-ttu-id="2f01f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2f01f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2f01f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f01f-140">OUTPUTS</span></span>

### <span data-ttu-id="2f01f-141">System. void</span><span class="sxs-lookup"><span data-stu-id="2f01f-141">System.Void</span></span>

### <span data-ttu-id="2f01f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f01f-142">System.Boolean</span></span>

## <span data-ttu-id="2f01f-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f01f-143">NOTES</span></span>
<span data-ttu-id="2f01f-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="2f01f-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2f01f-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f01f-145">RELATED LINKS</span></span>

[<span data-ttu-id="2f01f-146">Start — AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="2f01f-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="2f01f-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="2f01f-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="2f01f-148">Dodaj-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="2f01f-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="2f01f-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="2f01f-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)