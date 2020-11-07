---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 2b5f01047bf0b86fc885a01f0c58a9ab094f7698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719655"
---
# <span data-ttu-id="966fb-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="966fb-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="966fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="966fb-102">SYNOPSIS</span></span>
<span data-ttu-id="966fb-103">Rozpoczyna zarządzany dedykowany środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="966fb-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="966fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="966fb-104">SYNTAX</span></span>

### <span data-ttu-id="966fb-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="966fb-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="966fb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="966fb-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="966fb-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="966fb-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="966fb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="966fb-108">DESCRIPTION</span></span>
<span data-ttu-id="966fb-109">Polecenie cmdlet **Start-AzureRmDataFactoryV2IntegrationRuntime** rozpoczyna zarządzane dedykowane środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="966fb-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="966fb-110">Zasób jest inicjowany i po wykonaniu operacji jest to stan uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="966fb-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="966fb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="966fb-111">EXAMPLES</span></span>

### <span data-ttu-id="966fb-112">Przykład 1. Rozpocznij środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="966fb-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

    CreateTime                   : 9/11/2017 2:16:12 PM
    Nodes                        : {tvm-1650185656_1-20170911t141751z}
    OtherErrors                  : {}
    LastOperation                : 
    State                        : Started
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : testsvr.database.windows.net
    CatalogAdminUserName         : admin
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="966fb-113">To polecenie cmdlet rozpoczyna zarządzane dedykowane środowisko uruchomieniowe integracji o nazwie "Tested-IR".</span><span class="sxs-lookup"><span data-stu-id="966fb-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="966fb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="966fb-114">PARAMETERS</span></span>

### <span data-ttu-id="966fb-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="966fb-115">-Confirm</span></span>
<span data-ttu-id="966fb-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="966fb-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="966fb-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="966fb-117">-DataFactoryName</span></span>
<span data-ttu-id="966fb-118">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="966fb-118">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="966fb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="966fb-119">-Force</span></span>
<span data-ttu-id="966fb-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="966fb-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="966fb-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="966fb-121">-InputObject</span></span>
<span data-ttu-id="966fb-122">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="966fb-122">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="966fb-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="966fb-123">-Name</span></span>
<span data-ttu-id="966fb-124">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="966fb-124">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="966fb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="966fb-125">-ResourceGroupName</span></span>
<span data-ttu-id="966fb-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="966fb-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="966fb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="966fb-127">-ResourceId</span></span>
<span data-ttu-id="966fb-128">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="966fb-128">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="966fb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="966fb-129">-WhatIf</span></span>
<span data-ttu-id="966fb-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="966fb-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="966fb-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="966fb-131">INPUTS</span></span>

### <span data-ttu-id="966fb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="966fb-132">System.String</span></span>
<span data-ttu-id="966fb-133">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="966fb-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="966fb-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="966fb-134">OUTPUTS</span></span>

### <span data-ttu-id="966fb-135">Microsoft. Azure. Commands. DataFactoryV2. models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="966fb-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="966fb-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="966fb-136">NOTES</span></span>

## <span data-ttu-id="966fb-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="966fb-137">RELATED LINKS</span></span>
[<span data-ttu-id="966fb-138">Zatrzymaj — AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="966fb-138">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
