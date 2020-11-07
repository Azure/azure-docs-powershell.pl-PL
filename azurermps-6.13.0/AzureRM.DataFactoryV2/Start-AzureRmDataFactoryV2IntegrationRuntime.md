---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a9254fbac7e0c98413f4367d9b5e62581f6cb64c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717088"
---
# <span data-ttu-id="0b09f-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0b09f-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="0b09f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b09f-102">SYNOPSIS</span></span>
<span data-ttu-id="0b09f-103">Rozpoczyna zarządzany dedykowany środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="0b09f-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b09f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b09f-104">SYNTAX</span></span>

### <span data-ttu-id="0b09f-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0b09f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b09f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b09f-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b09f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0b09f-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b09f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0b09f-108">DESCRIPTION</span></span>
<span data-ttu-id="0b09f-109">Polecenie cmdlet **Start-AzureRmDataFactoryV2IntegrationRuntime** rozpoczyna zarządzane dedykowane środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="0b09f-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="0b09f-110">Zasób jest inicjowany i po wykonaniu operacji jest to stan uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="0b09f-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="0b09f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b09f-111">EXAMPLES</span></span>

### <span data-ttu-id="0b09f-112">Przykład 1. Rozpocznij środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="0b09f-112">Example 1: Start an integration runtime</span></span>
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

<span data-ttu-id="0b09f-113">To polecenie cmdlet rozpoczyna zarządzane dedykowane środowisko uruchomieniowe integracji o nazwie "Tested-IR".</span><span class="sxs-lookup"><span data-stu-id="0b09f-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="0b09f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b09f-114">PARAMETERS</span></span>

### <span data-ttu-id="0b09f-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0b09f-115">-DataFactoryName</span></span>
<span data-ttu-id="0b09f-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0b09f-116">The data factory name.</span></span>

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

### <span data-ttu-id="0b09f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b09f-117">-DefaultProfile</span></span>
<span data-ttu-id="0b09f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b09f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b09f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0b09f-119">-Force</span></span>
<span data-ttu-id="0b09f-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0b09f-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0b09f-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0b09f-121">-InputObject</span></span>
<span data-ttu-id="0b09f-122">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="0b09f-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="0b09f-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0b09f-123">-Name</span></span>
<span data-ttu-id="0b09f-124">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="0b09f-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="0b09f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b09f-125">-ResourceGroupName</span></span>
<span data-ttu-id="0b09f-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0b09f-126">The resource group name.</span></span>

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

### <span data-ttu-id="0b09f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b09f-127">-ResourceId</span></span>
<span data-ttu-id="0b09f-128">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0b09f-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0b09f-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b09f-129">-Confirm</span></span>
<span data-ttu-id="0b09f-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b09f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b09f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b09f-131">-WhatIf</span></span>
<span data-ttu-id="0b09f-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b09f-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0b09f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b09f-133">CommonParameters</span></span>
<span data-ttu-id="0b09f-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b09f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b09f-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b09f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b09f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b09f-136">INPUTS</span></span>

### <span data-ttu-id="0b09f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0b09f-137">System.String</span></span>

### <span data-ttu-id="0b09f-138">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0b09f-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="0b09f-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0b09f-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0b09f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b09f-140">OUTPUTS</span></span>

### <span data-ttu-id="0b09f-141">Microsoft. Azure. Commands. DataFactoryV2. models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="0b09f-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="0b09f-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b09f-142">NOTES</span></span>

## <span data-ttu-id="0b09f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b09f-143">RELATED LINKS</span></span>

[<span data-ttu-id="0b09f-144">Zatrzymaj — AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0b09f-144">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()