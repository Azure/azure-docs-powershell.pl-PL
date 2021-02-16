---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b441c354214775f3f6aad425513a953fbefe7810
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414887"
---
# <span data-ttu-id="e0ea2-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="e0ea2-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="e0ea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ea2-103">Usuwa przepływ danych z aplikacji Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="e0ea2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0ea2-104">SYNTAX</span></span>

### <span data-ttu-id="e0ea2-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="e0ea2-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0ea2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e0ea2-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0ea2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0ea2-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0ea2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0ea2-108">DESCRIPTION</span></span>
<span data-ttu-id="e0ea2-109">Polecenie Remove-AzDataFactoryV2DataFlow usuwa przepływ danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="e0ea2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0ea2-110">EXAMPLES</span></span>

### <span data-ttu-id="e0ea2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0ea2-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="e0ea2-112">To polecenie usuwa przepływ danych o nazwie dataflow5 z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="e0ea2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0ea2-113">PARAMETERS</span></span>

### <span data-ttu-id="e0ea2-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e0ea2-114">-DataFactoryName</span></span>
<span data-ttu-id="e0ea2-115">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ea2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ea2-116">-DefaultProfile</span></span>
<span data-ttu-id="e0ea2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0ea2-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e0ea2-118">-Force</span></span>
<span data-ttu-id="e0ea2-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e0ea2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0ea2-120">-InputObject</span></span>
<span data-ttu-id="e0ea2-121">Obiekt przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ea2-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0ea2-122">-Name</span></span>
<span data-ttu-id="e0ea2-123">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ea2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ea2-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0ea2-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ea2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0ea2-126">-ResourceId</span></span>
<span data-ttu-id="e0ea2-127">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ea2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0ea2-128">-PassThru</span></span>
<span data-ttu-id="e0ea2-129">Jeśli zostanie określona, w przypadku gdy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="e0ea2-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="e0ea2-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0ea2-131">-Confirm</span></span>
<span data-ttu-id="e0ea2-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0ea2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0ea2-133">-WhatIf</span></span>
<span data-ttu-id="e0ea2-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0ea2-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0ea2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ea2-136">CommonParameters</span></span>
<span data-ttu-id="e0ea2-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ea2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ea2-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0ea2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ea2-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0ea2-139">INPUTS</span></span>

### <span data-ttu-id="e0ea2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="e0ea2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="e0ea2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e0ea2-141">System.String</span></span>

## <span data-ttu-id="e0ea2-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0ea2-142">OUTPUTS</span></span>

### <span data-ttu-id="e0ea2-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="e0ea2-143">System.Void</span></span>

### <span data-ttu-id="e0ea2-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e0ea2-144">System.Boolean</span></span>

## <span data-ttu-id="e0ea2-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0ea2-145">NOTES</span></span>
<span data-ttu-id="e0ea2-146">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="e0ea2-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e0ea2-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0ea2-147">RELATED LINKS</span></span>



