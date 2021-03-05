---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 5997ca072ae11407500ceb254dbd16be13382ac8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975265"
---
# <span data-ttu-id="586c4-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="586c4-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="586c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="586c4-102">SYNOPSIS</span></span>
<span data-ttu-id="586c4-103">Pobiera informacje o zasobach środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="586c4-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="586c4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="586c4-104">SYNTAX</span></span>

### <span data-ttu-id="586c4-105">ByIntegrationRuntimeName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="586c4-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="586c4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="586c4-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="586c4-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="586c4-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="586c4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="586c4-108">DESCRIPTION</span></span>
<span data-ttu-id="586c4-109">Polecenie cmdlet Get-AzDataFactoryV2IntegrationRuntime uzyskać informacje o środowiskach uruchomieniowych integracji w factory danych.</span><span class="sxs-lookup"><span data-stu-id="586c4-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="586c4-110">Jeśli określisz nazwę środowiska uruchomieniowego integracji, to polecenie cmdlet pobiera informacje o tym środowisku uruchomieniowym integracji.</span><span class="sxs-lookup"><span data-stu-id="586c4-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="586c4-111">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich środowiskach uruchomieniowych integracji w factory danych.</span><span class="sxs-lookup"><span data-stu-id="586c4-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="586c4-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="586c4-112">EXAMPLES</span></span>

### <span data-ttu-id="586c4-113">Przykład 1. Lista wszystkich środowisk uruchomieniowych integracji w factory danych</span><span class="sxs-lookup"><span data-stu-id="586c4-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="586c4-114">Lista wszystkich środowisk uruchomieniowych integracji w factory danych o nazwie "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="586c4-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="586c4-115">Przykład 2. Uzyskiwanie zarządzanego dedykowanego środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="586c4-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    PublicIPs                    : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="586c4-116">To polecenie wyświetla informacje o środowisku uruchomieniowym integracji o nazwie "test-dedicated-ir" w subskrypcji dla grupy zasobów o nazwach "rg-test-dfv2" i data factory o nazwie "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="586c4-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="586c4-117">Przykład 3. Uzyskiwanie dedykowanego środowiska uruchomieniowego integracji zarządzanej ze stanem szczegółów</span><span class="sxs-lookup"><span data-stu-id="586c4-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

    CreateTime                   : 
    Nodes                        : 
    OtherErrors                  : 
    LastOperation                : 
    State                        : Initial
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    PublicIPs                    : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="586c4-118">To polecenie wyświetla informacje o środowisku uruchomieniowym integracji o nazwie "test-dedicated-ir" w subskrypcji dla grupy zasobów o nazwach "rg-test-dfv2" i data factory o nazwie "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="586c4-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="586c4-119">Przykład 4. Uzyskiwanie środowiska uruchomieniowego integracji z własnym hostem</span><span class="sxs-lookup"><span data-stu-id="586c4-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="586c4-120">To polecenie wyświetla informacje o środowisku uruchomieniowym integracji o nazwie "test-dedicated-ir" w subskrypcji dla grupy zasobów o nazwach "rg-test-dfv2" i data factory o nazwie "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="586c4-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="586c4-121">Przykład 5. Uzyskiwanie środowiska integracji we własnym środowisku uruchomieniowym ze stanem szczegółów</span><span class="sxs-lookup"><span data-stu-id="586c4-121">Example 5: Get self-hosted integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir -Status

    State                     : Online
    Version                   : 4.2.7233.1
    CreateTime                : 9/26/2019 6:00:08 AM
    AutoUpdate                : Off
    ScheduledUpdateDate       :
    UpdateDelayOffset         : 03:00:00
    LocalTimeZoneOffset       : 08:00:00
    InternalChannelEncryption :
    Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
    ServiceUrls               : {}
    Nodes                     : {}
    Links                     : {}
    AutoUpdateETA             :
    LatestVersion             : 4.3.7265.1
    PushedVersion             : 4.3.7265.1
    TaskQueueId               : fe2d60b5-86f5-58bf-bdae-7ef698284088
    VersionStatus             : UpdateAvailable
    Name                      : test-selfhost-ir
    Type                      : SelfHosted
    ResourceGroupName         : rg-test-dfv2
    DataFactoryName           : test-df-eu2
    Description               :
    Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
```

## <span data-ttu-id="586c4-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="586c4-122">PARAMETERS</span></span>

### <span data-ttu-id="586c4-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="586c4-123">-DataFactoryName</span></span>
<span data-ttu-id="586c4-124">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="586c4-124">The data factory name.</span></span>

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

### <span data-ttu-id="586c4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="586c4-125">-DefaultProfile</span></span>
<span data-ttu-id="586c4-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="586c4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="586c4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="586c4-127">-InputObject</span></span>
<span data-ttu-id="586c4-128">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="586c4-128">The integration runtime object.</span></span>

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

### <span data-ttu-id="586c4-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="586c4-129">-Name</span></span>
<span data-ttu-id="586c4-130">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="586c4-130">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="586c4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="586c4-131">-ResourceGroupName</span></span>
<span data-ttu-id="586c4-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="586c4-132">The resource group name.</span></span>

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

### <span data-ttu-id="586c4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="586c4-133">-ResourceId</span></span>
<span data-ttu-id="586c4-134">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="586c4-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="586c4-135">— Status</span><span class="sxs-lookup"><span data-stu-id="586c4-135">-Status</span></span>
<span data-ttu-id="586c4-136">Stan szczegółów środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="586c4-136">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="586c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="586c4-137">CommonParameters</span></span>
<span data-ttu-id="586c4-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="586c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="586c4-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="586c4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="586c4-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="586c4-140">INPUTS</span></span>

### <span data-ttu-id="586c4-141">System.String</span><span class="sxs-lookup"><span data-stu-id="586c4-141">System.String</span></span>

### <span data-ttu-id="586c4-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="586c4-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="586c4-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="586c4-143">OUTPUTS</span></span>

### <span data-ttu-id="586c4-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="586c4-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="586c4-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="586c4-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="586c4-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="586c4-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="586c4-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="586c4-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="586c4-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="586c4-148">NOTES</span></span>
<span data-ttu-id="586c4-149">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="586c4-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="586c4-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="586c4-150">RELATED LINKS</span></span>

[<span data-ttu-id="586c4-151">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="586c4-151">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="586c4-152">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="586c4-152">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
