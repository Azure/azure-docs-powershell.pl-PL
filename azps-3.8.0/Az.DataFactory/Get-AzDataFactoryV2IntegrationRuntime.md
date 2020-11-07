---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 5525dc4613fc1d6bccc56e27de065151b1890f7d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896457"
---
# <span data-ttu-id="34ca9-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="34ca9-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="34ca9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="34ca9-103">Pobiera informacje o zasobach w czasie wykonywania integracji.</span><span class="sxs-lookup"><span data-stu-id="34ca9-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="34ca9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34ca9-104">SYNTAX</span></span>

### <span data-ttu-id="34ca9-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="34ca9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34ca9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="34ca9-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34ca9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="34ca9-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34ca9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="34ca9-108">DESCRIPTION</span></span>
<span data-ttu-id="34ca9-109">Polecenie cmdlet Get-AzDataFactoryV2IntegrationRuntime pobiera informacje o środowiskach integracji w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="34ca9-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="34ca9-110">Jeśli określisz nazwę środowiska wykonawczego integracji, to polecenie cmdlet spowoduje wyświetlenie informacji o tym czasie wykonywania integracji.</span><span class="sxs-lookup"><span data-stu-id="34ca9-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="34ca9-111">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich środowiskach uruchomieniowych integracji w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="34ca9-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="34ca9-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34ca9-112">EXAMPLES</span></span>

### <span data-ttu-id="34ca9-113">Przykład 1. Wyświetl wszystkie środowiska integracji w fabryce danych</span><span class="sxs-lookup"><span data-stu-id="34ca9-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="34ca9-114">Lista wszystkich środowisk uruchomieniowych integracji w fabryce danych o nazwie test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="34ca9-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="34ca9-115">Przykład 2: uzyskiwanie zarządzanego dedykowanego środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="34ca9-115">Example 2: Get managed dedicated integration runtime</span></span>
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

<span data-ttu-id="34ca9-116">To polecenie wyświetla informacje o środowisku wykonawczym integracji o nazwie "Tested-IR" w subskrypcji grupy zasobów o nazwie "RG-test-dfv2" i fabryki danych o nazwie "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="34ca9-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="34ca9-117">Przykład 3: uzyskiwanie zarządzanego dedykowanego środowiska uruchomieniowego integracji ze szczegółowym stanem</span><span class="sxs-lookup"><span data-stu-id="34ca9-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
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

<span data-ttu-id="34ca9-118">To polecenie wyświetla informacje o środowisku wykonawczym integracji o nazwie "Tested-IR" w subskrypcji grupy zasobów o nazwie "RG-test-dfv2" i fabryki danych o nazwie "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="34ca9-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="34ca9-119">Przykład 4: uzyskiwanie środowiska uruchomieniowego integracji z obsługą własna</span><span class="sxs-lookup"><span data-stu-id="34ca9-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="34ca9-120">To polecenie wyświetla informacje o środowisku wykonawczym integracji o nazwie "Tested-IR" w subskrypcji grupy zasobów o nazwie "RG-test-dfv2" i fabryki danych o nazwie "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="34ca9-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="34ca9-121">Przykład 5: pobieranie danych środowiska uruchomieniowego integracji z obsługą danych z informacjami o stanie szczegółowym</span><span class="sxs-lookup"><span data-stu-id="34ca9-121">Example 5: Get self-hosted integration runtime with detail status</span></span>
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

## <span data-ttu-id="34ca9-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34ca9-122">PARAMETERS</span></span>

### <span data-ttu-id="34ca9-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="34ca9-123">-DataFactoryName</span></span>
<span data-ttu-id="34ca9-124">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="34ca9-124">The data factory name.</span></span>

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

### <span data-ttu-id="34ca9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ca9-125">-DefaultProfile</span></span>
<span data-ttu-id="34ca9-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34ca9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34ca9-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="34ca9-127">-InputObject</span></span>
<span data-ttu-id="34ca9-128">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="34ca9-128">The integration runtime object.</span></span>

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

### <span data-ttu-id="34ca9-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34ca9-129">-Name</span></span>
<span data-ttu-id="34ca9-130">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="34ca9-130">The integration runtime name.</span></span>

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

### <span data-ttu-id="34ca9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34ca9-131">-ResourceGroupName</span></span>
<span data-ttu-id="34ca9-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34ca9-132">The resource group name.</span></span>

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

### <span data-ttu-id="34ca9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34ca9-133">-ResourceId</span></span>
<span data-ttu-id="34ca9-134">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="34ca9-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="34ca9-135">-Status</span><span class="sxs-lookup"><span data-stu-id="34ca9-135">-Status</span></span>
<span data-ttu-id="34ca9-136">Stan szczegółów środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="34ca9-136">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="34ca9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ca9-137">CommonParameters</span></span>
<span data-ttu-id="34ca9-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34ca9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ca9-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34ca9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ca9-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34ca9-140">INPUTS</span></span>

### <span data-ttu-id="34ca9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="34ca9-141">System.String</span></span>

### <span data-ttu-id="34ca9-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="34ca9-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="34ca9-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34ca9-143">OUTPUTS</span></span>

### <span data-ttu-id="34ca9-144">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="34ca9-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="34ca9-145">Microsoft. Azure. Commands. DataFactoryV2. models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="34ca9-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="34ca9-146">Microsoft. Azure. Commands. DataFactoryV2. models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="34ca9-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="34ca9-147">Microsoft. Azure. Commands. DataFactoryV2. models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="34ca9-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="34ca9-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34ca9-148">NOTES</span></span>
<span data-ttu-id="34ca9-149">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="34ca9-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="34ca9-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34ca9-150">RELATED LINKS</span></span>

[<span data-ttu-id="34ca9-151">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="34ca9-151">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="34ca9-152">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="34ca9-152">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
