---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 2c20752dd1e29962f128f687344b3b165f0a09ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545387"
---
# <span data-ttu-id="be9ac-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="be9ac-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="be9ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be9ac-102">SYNOPSIS</span></span>
<span data-ttu-id="be9ac-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="be9ac-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be9ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be9ac-104">SYNTAX</span></span>

### <span data-ttu-id="be9ac-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="be9ac-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be9ac-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="be9ac-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be9ac-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="be9ac-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be9ac-108">Opis</span><span class="sxs-lookup"><span data-stu-id="be9ac-108">DESCRIPTION</span></span>
<span data-ttu-id="be9ac-109">Polecenie cmdlet **Update-AzureRmDataFactoryV2IntegrationRuntime** umożliwia aktualizowanie właściwości środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="be9ac-109">The **Update-AzureRmDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="be9ac-110">Obecnie polecenie cmdlet obsługuje tylko aktualizowanie "Autoaktualizacja" i "AutoUpdateDelayOffset" w przypadku środowiska uruchomieniowego integracji samodzielnego.</span><span class="sxs-lookup"><span data-stu-id="be9ac-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="be9ac-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be9ac-111">EXAMPLES</span></span>

### <span data-ttu-id="be9ac-112">Przykład 1: aktualizowanie środowiska wykonawczego integracji</span><span class="sxs-lookup"><span data-stu-id="be9ac-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntime `
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

<span data-ttu-id="be9ac-113">Polecenie cmdlet aktualizuje samowyodrębniający się środowisko uruchomieniowe integracji o nazwie "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="be9ac-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="be9ac-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be9ac-114">PARAMETERS</span></span>

### <span data-ttu-id="be9ac-115">-Aktualizacje automatyczne</span><span class="sxs-lookup"><span data-stu-id="be9ac-115">-AutoUpdate</span></span>
<span data-ttu-id="be9ac-116">Włączanie lub wyłączanie automatycznej aktualizacji funkcji automatycznego aktualizowania środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="be9ac-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="be9ac-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="be9ac-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="be9ac-118">Czas w godzinie dnia dla automatycznej aktualizacji funkcji automatycznego aktualizowania w czasie wykonywania integracji.</span><span class="sxs-lookup"><span data-stu-id="be9ac-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="be9ac-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="be9ac-119">-DataFactoryName</span></span>
<span data-ttu-id="be9ac-120">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="be9ac-120">The data factory name.</span></span>

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

### <span data-ttu-id="be9ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be9ac-121">-DefaultProfile</span></span>
<span data-ttu-id="be9ac-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="be9ac-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be9ac-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="be9ac-123">-InputObject</span></span>
<span data-ttu-id="be9ac-124">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="be9ac-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="be9ac-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be9ac-125">-Name</span></span>
<span data-ttu-id="be9ac-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="be9ac-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="be9ac-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be9ac-127">-ResourceGroupName</span></span>
<span data-ttu-id="be9ac-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="be9ac-128">The resource group name.</span></span>

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

### <span data-ttu-id="be9ac-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be9ac-129">-ResourceId</span></span>
<span data-ttu-id="be9ac-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="be9ac-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="be9ac-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be9ac-131">-Confirm</span></span>
<span data-ttu-id="be9ac-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be9ac-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be9ac-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be9ac-133">-WhatIf</span></span>
<span data-ttu-id="be9ac-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be9ac-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be9ac-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="be9ac-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be9ac-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be9ac-136">CommonParameters</span></span>
<span data-ttu-id="be9ac-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be9ac-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be9ac-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be9ac-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be9ac-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be9ac-139">INPUTS</span></span>

### <span data-ttu-id="be9ac-140">System. String</span><span class="sxs-lookup"><span data-stu-id="be9ac-140">System.String</span></span>

### <span data-ttu-id="be9ac-141">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="be9ac-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="be9ac-142">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="be9ac-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="be9ac-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be9ac-143">OUTPUTS</span></span>

### <span data-ttu-id="be9ac-144">Microsoft. Azure. Commands. DataFactoryV2. models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="be9ac-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="be9ac-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be9ac-145">NOTES</span></span>
<span data-ttu-id="be9ac-146">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="be9ac-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="be9ac-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be9ac-147">RELATED LINKS</span></span>

<span data-ttu-id="be9ac-148">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="be9ac-148">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

