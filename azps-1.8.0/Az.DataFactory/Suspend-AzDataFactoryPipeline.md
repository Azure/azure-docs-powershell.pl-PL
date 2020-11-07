---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: 2f3d48044b06292b18b1254adf1e2bc6d0698d4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710074"
---
# <span data-ttu-id="8538c-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="8538c-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="8538c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8538c-102">SYNOPSIS</span></span>
<span data-ttu-id="8538c-103">Wstrzymuje rurociąg w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8538c-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="8538c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8538c-104">SYNTAX</span></span>

### <span data-ttu-id="8538c-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8538c-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8538c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8538c-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8538c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8538c-107">DESCRIPTION</span></span>
<span data-ttu-id="8538c-108">Polecenie cmdlet **Suspend-AzDataFactoryPipeline** zawiesza rurociąg w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8538c-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="8538c-109">Możesz wznowić rurociąg, korzystając z polecenia cmdlet Resume-AzDataFactoryPipeline.</span><span class="sxs-lookup"><span data-stu-id="8538c-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="8538c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8538c-110">EXAMPLES</span></span>

### <span data-ttu-id="8538c-111">Przykład 1: Wstrzymywanie rurociągu</span><span class="sxs-lookup"><span data-stu-id="8538c-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="8538c-112">To polecenie zawiesza potok o nazwie DPWikiSample w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8538c-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="8538c-113">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="8538c-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="8538c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8538c-114">PARAMETERS</span></span>

### <span data-ttu-id="8538c-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8538c-115">-DataFactory</span></span>
<span data-ttu-id="8538c-116">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="8538c-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8538c-117">To polecenie cmdlet zawiesza potok należący do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="8538c-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8538c-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8538c-118">-DataFactoryName</span></span>
<span data-ttu-id="8538c-119">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="8538c-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8538c-120">To polecenie cmdlet zawiesza potok należący do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="8538c-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8538c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8538c-121">-DefaultProfile</span></span>
<span data-ttu-id="8538c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8538c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8538c-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8538c-123">-Name</span></span>
<span data-ttu-id="8538c-124">Określa nazwę potoku, który ma zostać zawieszony.</span><span class="sxs-lookup"><span data-stu-id="8538c-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="8538c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8538c-125">-ResourceGroupName</span></span>
<span data-ttu-id="8538c-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8538c-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8538c-127">To polecenie cmdlet zawiesza potok należący do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="8538c-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8538c-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8538c-128">-Confirm</span></span>
<span data-ttu-id="8538c-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8538c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8538c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8538c-130">-WhatIf</span></span>
<span data-ttu-id="8538c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8538c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8538c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8538c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8538c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8538c-133">CommonParameters</span></span>
<span data-ttu-id="8538c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8538c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8538c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8538c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8538c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8538c-136">INPUTS</span></span>

### <span data-ttu-id="8538c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8538c-137">System.String</span></span>

### <span data-ttu-id="8538c-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8538c-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="8538c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8538c-139">OUTPUTS</span></span>

### <span data-ttu-id="8538c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8538c-140">System.Boolean</span></span>

## <span data-ttu-id="8538c-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8538c-141">NOTES</span></span>
* <span data-ttu-id="8538c-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="8538c-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8538c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8538c-143">RELATED LINKS</span></span>

[<span data-ttu-id="8538c-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="8538c-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="8538c-145">Nowe — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="8538c-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="8538c-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="8538c-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="8538c-147">Życiorys — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="8538c-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="8538c-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="8538c-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


