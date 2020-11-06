---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: a69e051fb8f2cba30fba8419a818346e044f8462
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545384"
---
# <span data-ttu-id="54ce8-101">Update-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="54ce8-101">Update-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="54ce8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="54ce8-103">Umożliwia zaktualizowanie węzła środowiska uruchomieniowego integracji na samym własnym poziomie.</span><span class="sxs-lookup"><span data-stu-id="54ce8-103">Updates self-hosted integration runtime node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54ce8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54ce8-104">SYNTAX</span></span>

### <span data-ttu-id="54ce8-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="54ce8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54ce8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="54ce8-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54ce8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="54ce8-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54ce8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="54ce8-108">DESCRIPTION</span></span>
<span data-ttu-id="54ce8-109">Polecenie cmdlet **Update-AzureRmDataFactoryV2IntegrationRuntimeNode** umożliwia aktualizowanie właściwości węzła środowiska uruchomieniowego integracji samodzielnej w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="54ce8-109">The **Update-AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="54ce8-110">Obecnie obsługuje tylko aktualizowanie "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="54ce8-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="54ce8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54ce8-111">EXAMPLES</span></span>

### <span data-ttu-id="54ce8-112">Przykład 1: aktualizowanie węzła środowiska uruchomieniowego integracji z obsługą własna</span><span class="sxs-lookup"><span data-stu-id="54ce8-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="54ce8-113">Polecenie cmdlet aktualizuje "ConcurrentJobsLimit" to 3 dla węzła "Node_1" w środowisku wykonawczym "test-SelfHost-IR" w ramach samodzielnej integracji.</span><span class="sxs-lookup"><span data-stu-id="54ce8-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="54ce8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54ce8-114">PARAMETERS</span></span>

### <span data-ttu-id="54ce8-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="54ce8-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="54ce8-116">Liczba współbieżnych zadań, które mogą działać w węźle środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="54ce8-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="54ce8-117">Dozwolone są wartości z zakresu od 1 do maxConcurrentJobs.</span><span class="sxs-lookup"><span data-stu-id="54ce8-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ce8-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="54ce8-118">-DataFactoryName</span></span>
<span data-ttu-id="54ce8-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="54ce8-119">The data factory name.</span></span>

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

### <span data-ttu-id="54ce8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ce8-120">-DefaultProfile</span></span>
<span data-ttu-id="54ce8-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="54ce8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54ce8-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="54ce8-122">-InputObject</span></span>
<span data-ttu-id="54ce8-123">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="54ce8-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="54ce8-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="54ce8-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="54ce8-125">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="54ce8-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54ce8-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="54ce8-126">-Name</span></span>
<span data-ttu-id="54ce8-127">Nazwa węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="54ce8-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ce8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54ce8-128">-ResourceGroupName</span></span>
<span data-ttu-id="54ce8-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="54ce8-129">The resource group name.</span></span>

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

### <span data-ttu-id="54ce8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54ce8-130">-ResourceId</span></span>
<span data-ttu-id="54ce8-131">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="54ce8-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="54ce8-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="54ce8-132">-Confirm</span></span>
<span data-ttu-id="54ce8-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54ce8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54ce8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54ce8-134">-WhatIf</span></span>
<span data-ttu-id="54ce8-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54ce8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54ce8-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="54ce8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54ce8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ce8-137">CommonParameters</span></span>
<span data-ttu-id="54ce8-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54ce8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ce8-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54ce8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ce8-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54ce8-140">INPUTS</span></span>

### <span data-ttu-id="54ce8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="54ce8-141">System.String</span></span>

### <span data-ttu-id="54ce8-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="54ce8-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="54ce8-143">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="54ce8-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="54ce8-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54ce8-144">OUTPUTS</span></span>

### <span data-ttu-id="54ce8-145">Microsoft. Azure. Commands. DataFactoryV2. models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="54ce8-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="54ce8-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54ce8-146">NOTES</span></span>
<span data-ttu-id="54ce8-147">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="54ce8-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="54ce8-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54ce8-148">RELATED LINKS</span></span>

<span data-ttu-id="54ce8-149">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="54ce8-149">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

