---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 8b5b9e8cfd1909b0d91627a2c0600620f264da78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501561"
---
# <span data-ttu-id="5e8a3-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="5e8a3-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="5e8a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e8a3-102">SYNOPSIS</span></span>
<span data-ttu-id="5e8a3-103">Usuwa przepływ danych z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="5e8a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e8a3-104">SYNTAX</span></span>

### <span data-ttu-id="5e8a3-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5e8a3-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e8a3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5e8a3-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e8a3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e8a3-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e8a3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5e8a3-108">DESCRIPTION</span></span>
<span data-ttu-id="5e8a3-109">Polecenie cmdlet Remove-AzDataFactoryV2DataFlow usuwa przepływ danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="5e8a3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e8a3-110">EXAMPLES</span></span>

### <span data-ttu-id="5e8a3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5e8a3-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="5e8a3-112">To polecenie usuwa przepływ danych o nazwie dataflow5 z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="5e8a3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e8a3-113">PARAMETERS</span></span>

### <span data-ttu-id="5e8a3-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5e8a3-114">-DataFactoryName</span></span>
<span data-ttu-id="5e8a3-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-115">The data factory name.</span></span>

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

### <span data-ttu-id="5e8a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e8a3-116">-DefaultProfile</span></span>
<span data-ttu-id="5e8a3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e8a3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5e8a3-118">-Force</span></span>
<span data-ttu-id="5e8a3-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5e8a3-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e8a3-120">-InputObject</span></span>
<span data-ttu-id="5e8a3-121">Obiekt przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-121">The data flow object.</span></span>

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

### <span data-ttu-id="5e8a3-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e8a3-122">-Name</span></span>
<span data-ttu-id="5e8a3-123">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-123">The data flow name.</span></span>

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

### <span data-ttu-id="5e8a3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e8a3-124">-ResourceGroupName</span></span>
<span data-ttu-id="5e8a3-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-125">The resource group name.</span></span>

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

### <span data-ttu-id="5e8a3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e8a3-126">-ResourceId</span></span>
<span data-ttu-id="5e8a3-127">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5e8a3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e8a3-128">-PassThru</span></span>
<span data-ttu-id="5e8a3-129">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="5e8a3-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="5e8a3-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e8a3-131">-Confirm</span></span>
<span data-ttu-id="5e8a3-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e8a3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e8a3-133">-WhatIf</span></span>
<span data-ttu-id="5e8a3-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e8a3-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e8a3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e8a3-136">CommonParameters</span></span>
<span data-ttu-id="5e8a3-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e8a3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e8a3-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e8a3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e8a3-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e8a3-139">INPUTS</span></span>

### <span data-ttu-id="5e8a3-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="5e8a3-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="5e8a3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5e8a3-141">System.String</span></span>

## <span data-ttu-id="5e8a3-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e8a3-142">OUTPUTS</span></span>

### <span data-ttu-id="5e8a3-143">System. void</span><span class="sxs-lookup"><span data-stu-id="5e8a3-143">System.Void</span></span>

### <span data-ttu-id="5e8a3-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e8a3-144">System.Boolean</span></span>

## <span data-ttu-id="5e8a3-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e8a3-145">NOTES</span></span>
<span data-ttu-id="5e8a3-146">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="5e8a3-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5e8a3-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e8a3-147">RELATED LINKS</span></span>

[<span data-ttu-id="5e8a3-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="5e8a3-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="5e8a3-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="5e8a3-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

