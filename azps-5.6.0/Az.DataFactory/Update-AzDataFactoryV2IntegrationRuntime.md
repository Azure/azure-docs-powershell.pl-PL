---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: fa9e9e0b2de02a320cb5140aac21e30f7c2b5bbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006906"
---
# <span data-ttu-id="c9d00-101">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c9d00-101">Update-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="c9d00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9d00-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d00-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="c9d00-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="c9d00-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9d00-104">SYNTAX</span></span>

### <span data-ttu-id="c9d00-105">ByIntegrationRuntimeName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c9d00-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9d00-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c9d00-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9d00-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c9d00-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9d00-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9d00-108">DESCRIPTION</span></span>
<span data-ttu-id="c9d00-109">Polecenie **cmdlet Update-AzDataFactoryV2IntegrationRuntime** aktualizuje właściwości środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="c9d00-109">The **Update-AzDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="c9d00-110">Obecnie polecenie cmdlet obsługuje tylko aktualizowanie "AutoUpdate" i "AutoUpdateDelayOffset" dla środowiska uruchomieniowego integracji z własnym hostem.</span><span class="sxs-lookup"><span data-stu-id="c9d00-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="c9d00-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9d00-111">EXAMPLES</span></span>

### <span data-ttu-id="c9d00-112">Przykład 1. Aktualizacja środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="c9d00-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzDataFactoryV2IntegrationRuntime `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -Name 'test-selfhost-ir' `
    -AutoUpdate Off `
    -AutoUpdateDelayOffset $ts

Nodes                     : {Node_1}
CreateTime                : 11/18/2017 2:45:38 PM
InternalChannelEncryption : 
Version                   : 3.2.6519.3
Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
ScheduledUpdateDate       : 
UpdateDelayOffset         : 
LocalTimeZoneOffset       : 
AutoUpdate                : Off
ServiceUrls               : {wu.frontend.int.clouddatahub-int.net, *.servicebus.windows.net}
State                     : Online
Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
Type                      : SelfHosted
ResourceGroupName         : rg-test-dfv2
DataFactoryName           : test-df-eu2
Name                      : test-selfhost-ir
Description               : New 2 description
```

<span data-ttu-id="c9d00-113">Polecenie cmdlet aktualizuje środowisko uruchomieniowe integracji samoobsługowej o nazwie "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="c9d00-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="c9d00-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9d00-114">PARAMETERS</span></span>

### <span data-ttu-id="c9d00-115">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="c9d00-115">-AutoUpdate</span></span>
<span data-ttu-id="c9d00-116">Włącz lub wyłącz automatyczną aktualizację środowiska integracji z własnym środowiskiem uruchomieniowym.</span><span class="sxs-lookup"><span data-stu-id="c9d00-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d00-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="c9d00-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="c9d00-118">Czas w godzinie na automatyczną aktualizację środowiska integracji z własnym środowiskiem uruchomieniowym.</span><span class="sxs-lookup"><span data-stu-id="c9d00-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d00-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c9d00-119">-DataFactoryName</span></span>
<span data-ttu-id="c9d00-120">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="c9d00-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d00-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d00-121">-DefaultProfile</span></span>
<span data-ttu-id="c9d00-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d00-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9d00-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9d00-123">-InputObject</span></span>
<span data-ttu-id="c9d00-124">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="c9d00-124">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d00-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c9d00-125">-Name</span></span>
<span data-ttu-id="c9d00-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="c9d00-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d00-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d00-127">-ResourceGroupName</span></span>
<span data-ttu-id="c9d00-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9d00-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d00-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9d00-129">-ResourceId</span></span>
<span data-ttu-id="c9d00-130">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d00-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d00-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9d00-131">-Confirm</span></span>
<span data-ttu-id="c9d00-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9d00-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9d00-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9d00-133">-WhatIf</span></span>
<span data-ttu-id="c9d00-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9d00-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9d00-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c9d00-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9d00-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d00-136">CommonParameters</span></span>
<span data-ttu-id="c9d00-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d00-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d00-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d00-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d00-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9d00-139">INPUTS</span></span>

### <span data-ttu-id="c9d00-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c9d00-140">System.String</span></span>

### <span data-ttu-id="c9d00-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c9d00-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c9d00-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9d00-142">OUTPUTS</span></span>

### <span data-ttu-id="c9d00-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="c9d00-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="c9d00-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9d00-144">NOTES</span></span>
<span data-ttu-id="c9d00-145">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="c9d00-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="c9d00-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9d00-146">RELATED LINKS</span></span>

<span data-ttu-id="c9d00-147">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="c9d00-147">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

