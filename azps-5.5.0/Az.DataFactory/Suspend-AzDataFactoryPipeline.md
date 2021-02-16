---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242754"
---
# <span data-ttu-id="1f57a-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f57a-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="1f57a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f57a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f57a-103">Zawiesza potok w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1f57a-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="1f57a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1f57a-104">SYNTAX</span></span>

### <span data-ttu-id="1f57a-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="1f57a-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f57a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1f57a-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f57a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1f57a-107">DESCRIPTION</span></span>
<span data-ttu-id="1f57a-108">Polecenie cmdlet **Suspend-AzDataFactoryPipeline** zawiesza potok w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1f57a-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="1f57a-109">Potok można wznowić za pomocą polecenia cmdlet Resume-AzDataFactoryPipeline cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f57a-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="1f57a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1f57a-110">EXAMPLES</span></span>

### <span data-ttu-id="1f57a-111">Przykład 1. Zawieszanie potoku</span><span class="sxs-lookup"><span data-stu-id="1f57a-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="1f57a-112">To polecenie zawiesza potok o nazwie DPWikiSample w zakładzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1f57a-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="1f57a-113">Polecenie zwróci wartość $True.</span><span class="sxs-lookup"><span data-stu-id="1f57a-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="1f57a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f57a-114">PARAMETERS</span></span>

### <span data-ttu-id="1f57a-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1f57a-115">-DataFactory</span></span>
<span data-ttu-id="1f57a-116">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="1f57a-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1f57a-117">To polecenie cmdlet zawiesza potok należący do fabrycznych danych określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1f57a-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f57a-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1f57a-118">-DataFactoryName</span></span>
<span data-ttu-id="1f57a-119">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1f57a-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1f57a-120">To polecenie cmdlet zawiesza potok należący do fabrycznych danych określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1f57a-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1f57a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f57a-121">-DefaultProfile</span></span>
<span data-ttu-id="1f57a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1f57a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f57a-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1f57a-123">-Name</span></span>
<span data-ttu-id="1f57a-124">Określa nazwę potoku do zawieszenia.</span><span class="sxs-lookup"><span data-stu-id="1f57a-124">Specifies the name of the pipeline to suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f57a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f57a-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f57a-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f57a-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1f57a-127">To polecenie cmdlet zawiesza potok należący do grupy, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1f57a-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1f57a-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f57a-128">-Confirm</span></span>
<span data-ttu-id="1f57a-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f57a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f57a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f57a-130">-WhatIf</span></span>
<span data-ttu-id="1f57a-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f57a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f57a-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1f57a-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f57a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f57a-133">CommonParameters</span></span>
<span data-ttu-id="1f57a-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f57a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f57a-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f57a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f57a-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f57a-136">INPUTS</span></span>

### <span data-ttu-id="1f57a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1f57a-137">System.String</span></span>

### <span data-ttu-id="1f57a-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1f57a-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="1f57a-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f57a-139">OUTPUTS</span></span>

### <span data-ttu-id="1f57a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f57a-140">System.Boolean</span></span>

## <span data-ttu-id="1f57a-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1f57a-141">NOTES</span></span>
* <span data-ttu-id="1f57a-142">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="1f57a-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1f57a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f57a-143">RELATED LINKS</span></span>

[<span data-ttu-id="1f57a-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f57a-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="1f57a-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f57a-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="1f57a-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f57a-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="1f57a-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f57a-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="1f57a-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="1f57a-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


