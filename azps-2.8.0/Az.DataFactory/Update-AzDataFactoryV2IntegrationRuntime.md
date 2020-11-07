---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: d2177e2ca7705f579921b9e2eb9fc64ab0e0c33a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705907"
---
# <span data-ttu-id="733d3-101">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="733d3-101">Update-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="733d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="733d3-102">SYNOPSIS</span></span>
<span data-ttu-id="733d3-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="733d3-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="733d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="733d3-104">SYNTAX</span></span>

### <span data-ttu-id="733d3-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="733d3-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="733d3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="733d3-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="733d3-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="733d3-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="733d3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="733d3-108">DESCRIPTION</span></span>
<span data-ttu-id="733d3-109">Polecenie cmdlet **Update-AzDataFactoryV2IntegrationRuntime** umożliwia aktualizowanie właściwości środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="733d3-109">The **Update-AzDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="733d3-110">Obecnie polecenie cmdlet obsługuje tylko aktualizowanie "Autoaktualizacja" i "AutoUpdateDelayOffset" w przypadku środowiska uruchomieniowego integracji samodzielnego.</span><span class="sxs-lookup"><span data-stu-id="733d3-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="733d3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="733d3-111">EXAMPLES</span></span>

### <span data-ttu-id="733d3-112">Przykład 1: aktualizowanie środowiska wykonawczego integracji</span><span class="sxs-lookup"><span data-stu-id="733d3-112">Example 1: Updates an integration runtime</span></span>
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

<span data-ttu-id="733d3-113">Polecenie cmdlet aktualizuje samowyodrębniający się środowisko uruchomieniowe integracji o nazwie "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="733d3-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="733d3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="733d3-114">PARAMETERS</span></span>

### <span data-ttu-id="733d3-115">-Aktualizacje automatyczne</span><span class="sxs-lookup"><span data-stu-id="733d3-115">-AutoUpdate</span></span>
<span data-ttu-id="733d3-116">Włączanie lub wyłączanie automatycznej aktualizacji funkcji automatycznego aktualizowania środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="733d3-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="733d3-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="733d3-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="733d3-118">Czas w godzinie dnia dla automatycznej aktualizacji funkcji automatycznego aktualizowania w czasie wykonywania integracji.</span><span class="sxs-lookup"><span data-stu-id="733d3-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="733d3-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="733d3-119">-DataFactoryName</span></span>
<span data-ttu-id="733d3-120">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="733d3-120">The data factory name.</span></span>

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

### <span data-ttu-id="733d3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="733d3-121">-DefaultProfile</span></span>
<span data-ttu-id="733d3-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="733d3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="733d3-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="733d3-123">-InputObject</span></span>
<span data-ttu-id="733d3-124">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="733d3-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="733d3-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="733d3-125">-Name</span></span>
<span data-ttu-id="733d3-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="733d3-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="733d3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="733d3-127">-ResourceGroupName</span></span>
<span data-ttu-id="733d3-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="733d3-128">The resource group name.</span></span>

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

### <span data-ttu-id="733d3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="733d3-129">-ResourceId</span></span>
<span data-ttu-id="733d3-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="733d3-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="733d3-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="733d3-131">-Confirm</span></span>
<span data-ttu-id="733d3-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="733d3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="733d3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="733d3-133">-WhatIf</span></span>
<span data-ttu-id="733d3-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="733d3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="733d3-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="733d3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="733d3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="733d3-136">CommonParameters</span></span>
<span data-ttu-id="733d3-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="733d3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="733d3-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="733d3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="733d3-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="733d3-139">INPUTS</span></span>

### <span data-ttu-id="733d3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="733d3-140">System.String</span></span>

### <span data-ttu-id="733d3-141">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="733d3-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="733d3-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="733d3-142">OUTPUTS</span></span>

### <span data-ttu-id="733d3-143">Microsoft. Azure. Commands. DataFactoryV2. models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="733d3-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="733d3-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="733d3-144">NOTES</span></span>
<span data-ttu-id="733d3-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="733d3-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="733d3-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="733d3-146">RELATED LINKS</span></span>

<span data-ttu-id="733d3-147">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="733d3-147">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>
