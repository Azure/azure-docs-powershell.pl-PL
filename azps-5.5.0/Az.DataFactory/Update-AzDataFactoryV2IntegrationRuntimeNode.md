---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 0487794381e40db486df17cb9611191ac5d924d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238249"
---
# <span data-ttu-id="b8acf-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b8acf-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="b8acf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8acf-102">SYNOPSIS</span></span>
<span data-ttu-id="b8acf-103">Aktualizuje węzeł środowiska uruchomieniowego integracji samoobsługowej.</span><span class="sxs-lookup"><span data-stu-id="b8acf-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="b8acf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b8acf-104">SYNTAX</span></span>

### <span data-ttu-id="b8acf-105">ByIntegrationRuntimeName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b8acf-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8acf-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8acf-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8acf-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b8acf-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8acf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b8acf-108">DESCRIPTION</span></span>
<span data-ttu-id="b8acf-109">Polecenie **cmdlet Update-AzDataFactoryV2IntegrationRuntimeNode** aktualizuje właściwości węzła środowiska uruchomieniowego integracji samoobsługowej w fabrycznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="b8acf-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="b8acf-110">Obecnie obsługuje tylko aktualizowanie "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="b8acf-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="b8acf-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b8acf-111">EXAMPLES</span></span>

### <span data-ttu-id="b8acf-112">Przykład 1. Aktualizuje węzeł środowiska uruchomieniowego integracji z własnym środowiskiem uruchomieniowym</span><span class="sxs-lookup"><span data-stu-id="b8acf-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="b8acf-113">Polecenie cmdlet aktualizuje "ConcurrentJobsLimit" na 3 dla węzła "Node_1" w środowisku integracji samoobsługowej "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="b8acf-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="b8acf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8acf-114">PARAMETERS</span></span>

### <span data-ttu-id="b8acf-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="b8acf-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="b8acf-116">Liczba jednoczesnych zadań, które mogą być uruchamiane w węźle środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="b8acf-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="b8acf-117">Dozwolone są wartości od 1 do maxConcurrentJobs.</span><span class="sxs-lookup"><span data-stu-id="b8acf-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="b8acf-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b8acf-118">-DataFactoryName</span></span>
<span data-ttu-id="b8acf-119">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="b8acf-119">The data factory name.</span></span>

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

### <span data-ttu-id="b8acf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8acf-120">-DefaultProfile</span></span>
<span data-ttu-id="b8acf-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8acf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8acf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8acf-122">-InputObject</span></span>
<span data-ttu-id="b8acf-123">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="b8acf-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="b8acf-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b8acf-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b8acf-125">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="b8acf-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="b8acf-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b8acf-126">-Name</span></span>
<span data-ttu-id="b8acf-127">Nazwa węzła integracji środowiska uruchomieniowego.</span><span class="sxs-lookup"><span data-stu-id="b8acf-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="b8acf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8acf-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8acf-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8acf-129">The resource group name.</span></span>

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

### <span data-ttu-id="b8acf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8acf-130">-ResourceId</span></span>
<span data-ttu-id="b8acf-131">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="b8acf-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b8acf-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8acf-132">-Confirm</span></span>
<span data-ttu-id="b8acf-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b8acf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8acf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8acf-134">-WhatIf</span></span>
<span data-ttu-id="b8acf-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8acf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8acf-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b8acf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8acf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8acf-137">CommonParameters</span></span>
<span data-ttu-id="b8acf-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8acf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8acf-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8acf-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8acf-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8acf-140">INPUTS</span></span>

### <span data-ttu-id="b8acf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b8acf-141">System.String</span></span>

### <span data-ttu-id="b8acf-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b8acf-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b8acf-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8acf-143">OUTPUTS</span></span>

### <span data-ttu-id="b8acf-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b8acf-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="b8acf-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b8acf-145">NOTES</span></span>
<span data-ttu-id="b8acf-146">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="b8acf-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="b8acf-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8acf-147">RELATED LINKS</span></span>

<span data-ttu-id="b8acf-148">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="b8acf-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

