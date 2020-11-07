---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 67ce6dab34f907babd11bf180b499d25cfe9a053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705906"
---
# <span data-ttu-id="5e7d8-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="5e7d8-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="5e7d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e7d8-102">SYNOPSIS</span></span>
<span data-ttu-id="5e7d8-103">Umożliwia zaktualizowanie węzła środowiska uruchomieniowego integracji na samym własnym poziomie.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="5e7d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e7d8-104">SYNTAX</span></span>

### <span data-ttu-id="5e7d8-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5e7d8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e7d8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e7d8-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e7d8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5e7d8-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e7d8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5e7d8-108">DESCRIPTION</span></span>
<span data-ttu-id="5e7d8-109">Polecenie cmdlet **Update-AzDataFactoryV2IntegrationRuntimeNode** umożliwia aktualizowanie właściwości węzła środowiska uruchomieniowego integracji samodzielnej w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="5e7d8-110">Obecnie obsługuje tylko aktualizowanie "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="5e7d8-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="5e7d8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e7d8-111">EXAMPLES</span></span>

### <span data-ttu-id="5e7d8-112">Przykład 1: aktualizowanie węzła środowiska uruchomieniowego integracji z obsługą własna</span><span class="sxs-lookup"><span data-stu-id="5e7d8-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="5e7d8-113">Polecenie cmdlet aktualizuje "ConcurrentJobsLimit" to 3 dla węzła "Node_1" w środowisku wykonawczym "test-SelfHost-IR" w ramach samodzielnej integracji.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="5e7d8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e7d8-114">PARAMETERS</span></span>

### <span data-ttu-id="5e7d8-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="5e7d8-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="5e7d8-116">Liczba współbieżnych zadań, które mogą działać w węźle środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="5e7d8-117">Dozwolone są wartości z zakresu od 1 do maxConcurrentJobs.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="5e7d8-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5e7d8-118">-DataFactoryName</span></span>
<span data-ttu-id="5e7d8-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-119">The data factory name.</span></span>

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

### <span data-ttu-id="5e7d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e7d8-120">-DefaultProfile</span></span>
<span data-ttu-id="5e7d8-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e7d8-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e7d8-122">-InputObject</span></span>
<span data-ttu-id="5e7d8-123">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="5e7d8-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="5e7d8-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="5e7d8-125">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="5e7d8-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e7d8-126">-Name</span></span>
<span data-ttu-id="5e7d8-127">Nazwa węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="5e7d8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e7d8-128">-ResourceGroupName</span></span>
<span data-ttu-id="5e7d8-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-129">The resource group name.</span></span>

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

### <span data-ttu-id="5e7d8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e7d8-130">-ResourceId</span></span>
<span data-ttu-id="5e7d8-131">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5e7d8-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e7d8-132">-Confirm</span></span>
<span data-ttu-id="5e7d8-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e7d8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e7d8-134">-WhatIf</span></span>
<span data-ttu-id="5e7d8-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e7d8-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e7d8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e7d8-137">CommonParameters</span></span>
<span data-ttu-id="5e7d8-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e7d8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e7d8-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e7d8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e7d8-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e7d8-140">INPUTS</span></span>

### <span data-ttu-id="5e7d8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5e7d8-141">System.String</span></span>

### <span data-ttu-id="5e7d8-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5e7d8-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5e7d8-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e7d8-143">OUTPUTS</span></span>

### <span data-ttu-id="5e7d8-144">Microsoft. Azure. Commands. DataFactoryV2. models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="5e7d8-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="5e7d8-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e7d8-145">NOTES</span></span>
<span data-ttu-id="5e7d8-146">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="5e7d8-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="5e7d8-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e7d8-147">RELATED LINKS</span></span>

<span data-ttu-id="5e7d8-148">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="5e7d8-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

