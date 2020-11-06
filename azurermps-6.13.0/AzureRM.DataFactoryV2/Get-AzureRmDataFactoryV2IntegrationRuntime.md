---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 83e6de07f7796e49732a35cfea4573002e6208df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548787"
---
# <span data-ttu-id="f767c-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f767c-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="f767c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f767c-102">SYNOPSIS</span></span>
<span data-ttu-id="f767c-103">Pobiera informacje o zasobach w czasie wykonywania integracji.</span><span class="sxs-lookup"><span data-stu-id="f767c-103">Gets information about integration runtime resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f767c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f767c-104">SYNTAX</span></span>

### <span data-ttu-id="f767c-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f767c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f767c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f767c-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f767c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f767c-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f767c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f767c-108">DESCRIPTION</span></span>
<span data-ttu-id="f767c-109">Polecenie cmdlet Get-AzureRmDataFactoryV2IntegrationRuntime pobiera informacje o środowiskach integracji w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="f767c-109">The Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="f767c-110">Jeśli określisz nazwę środowiska wykonawczego integracji, to polecenie cmdlet spowoduje wyświetlenie informacji o tym czasie wykonywania integracji.</span><span class="sxs-lookup"><span data-stu-id="f767c-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="f767c-111">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich środowiskach uruchomieniowych integracji w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="f767c-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="f767c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f767c-112">EXAMPLES</span></span>

### <span data-ttu-id="f767c-113">Przykład 1. Wyświetl wszystkie środowiska integracji w fabryce danych</span><span class="sxs-lookup"><span data-stu-id="f767c-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="f767c-114">Lista wszystkich środowisk uruchomieniowych integracji w fabryce danych o nazwie test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="f767c-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="f767c-115">Przykład 2: uzyskiwanie zarządzanego dedykowanego środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="f767c-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

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
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="f767c-116">To polecenie wyświetla informacje o środowisku wykonawczym integracji o nazwie "Tested-IR" w subskrypcji grupy zasobów o nazwie "RG-test-dfv2" i fabryki danych o nazwie "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="f767c-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="f767c-117">Przykład 3: uzyskiwanie zarządzanego dedykowanego środowiska uruchomieniowego integracji ze szczegółowym stanem</span><span class="sxs-lookup"><span data-stu-id="f767c-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

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
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="f767c-118">To polecenie wyświetla informacje o środowisku wykonawczym integracji o nazwie "Tested-IR" w subskrypcji grupy zasobów o nazwie "RG-test-dfv2" i fabryki danych o nazwie "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="f767c-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="f767c-119">Przykład 4: uzyskiwanie środowiska uruchomieniowego integracji z obsługą własna</span><span class="sxs-lookup"><span data-stu-id="f767c-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="f767c-120">To polecenie wyświetla informacje o środowisku wykonawczym integracji o nazwie "Tested-IR" w subskrypcji grupy zasobów o nazwie "RG-test-dfv2" i fabryki danych o nazwie "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="f767c-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="f767c-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f767c-121">PARAMETERS</span></span>

### <span data-ttu-id="f767c-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f767c-122">-DataFactoryName</span></span>
<span data-ttu-id="f767c-123">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="f767c-123">The data factory name.</span></span>

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

### <span data-ttu-id="f767c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f767c-124">-DefaultProfile</span></span>
<span data-ttu-id="f767c-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f767c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f767c-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f767c-126">-InputObject</span></span>
<span data-ttu-id="f767c-127">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="f767c-127">The integration runtime object.</span></span>

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

### <span data-ttu-id="f767c-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f767c-128">-Name</span></span>
<span data-ttu-id="f767c-129">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="f767c-129">The integration runtime name.</span></span>

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

### <span data-ttu-id="f767c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f767c-130">-ResourceGroupName</span></span>
<span data-ttu-id="f767c-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f767c-131">The resource group name.</span></span>

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

### <span data-ttu-id="f767c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f767c-132">-ResourceId</span></span>
<span data-ttu-id="f767c-133">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f767c-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f767c-134">-Status</span><span class="sxs-lookup"><span data-stu-id="f767c-134">-Status</span></span>
<span data-ttu-id="f767c-135">Stan szczegółów środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="f767c-135">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="f767c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f767c-136">CommonParameters</span></span>
<span data-ttu-id="f767c-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f767c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f767c-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f767c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f767c-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f767c-139">INPUTS</span></span>

### <span data-ttu-id="f767c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f767c-140">System.String</span></span>

### <span data-ttu-id="f767c-141">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f767c-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="f767c-142">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f767c-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f767c-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f767c-143">OUTPUTS</span></span>

### <span data-ttu-id="f767c-144">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f767c-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="f767c-145">Microsoft. Azure. Commands. DataFactoryV2. models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f767c-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="f767c-146">Microsoft. Azure. Commands. DataFactoryV2. models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f767c-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="f767c-147">Microsoft. Azure. Commands. DataFactoryV2. models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f767c-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="f767c-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f767c-148">NOTES</span></span>
<span data-ttu-id="f767c-149">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="f767c-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="f767c-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f767c-150">RELATED LINKS</span></span>

[<span data-ttu-id="f767c-151">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f767c-151">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="f767c-152">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f767c-152">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
