---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/resume-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
ms.openlocfilehash: 221fb414464c062a2f1798223bfe68a09543d7c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705950"
---
# <span data-ttu-id="10746-101">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="10746-101">Resume-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="10746-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10746-102">SYNOPSIS</span></span>
<span data-ttu-id="10746-103">Wznawia zawieszoną rurociąg w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="10746-103">Resumes a suspended pipeline in Data Factory.</span></span>

## <span data-ttu-id="10746-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10746-104">SYNTAX</span></span>

### <span data-ttu-id="10746-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="10746-105">ByFactoryName (Default)</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10746-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="10746-106">ByFactoryObject</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10746-107">Opis</span><span class="sxs-lookup"><span data-stu-id="10746-107">DESCRIPTION</span></span>
<span data-ttu-id="10746-108">Polecenie cmdlet **Resume-AzDataFactoryPipeline** Wznawia zawieszone potoku w fabryce danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="10746-108">The **Resume-AzDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="10746-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10746-109">EXAMPLES</span></span>

### <span data-ttu-id="10746-110">Przykład 1: wznowienie procesu</span><span class="sxs-lookup"><span data-stu-id="10746-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="10746-111">To polecenie wznawia potok o nazwie DPWikisample w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="10746-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="10746-112">Aby zawiesić rurociąg, użyj polecenia cmdlet **Suspend-AzDataFactoryPipeline** .</span><span class="sxs-lookup"><span data-stu-id="10746-112">Use the **Suspend-AzDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="10746-113">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="10746-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="10746-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10746-114">PARAMETERS</span></span>

### <span data-ttu-id="10746-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="10746-115">-DataFactory</span></span>
<span data-ttu-id="10746-116">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="10746-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="10746-117">To polecenie cmdlet powoduje wznowienie pracy rurociągu należącego do fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="10746-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="10746-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="10746-118">-DataFactoryName</span></span>
<span data-ttu-id="10746-119">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="10746-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="10746-120">To polecenie cmdlet powoduje wznowienie pracy rurociągu należącego do fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="10746-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="10746-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10746-121">-DefaultProfile</span></span>
<span data-ttu-id="10746-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="10746-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10746-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10746-123">-Name</span></span>
<span data-ttu-id="10746-124">Określa nazwę potoku, który ma zostać wznowiony.</span><span class="sxs-lookup"><span data-stu-id="10746-124">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="10746-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10746-125">-ResourceGroupName</span></span>
<span data-ttu-id="10746-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="10746-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="10746-127">To polecenie cmdlet powoduje wznowienie pracy rurociągu należącego do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="10746-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="10746-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10746-128">-Confirm</span></span>
<span data-ttu-id="10746-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10746-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10746-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10746-130">-WhatIf</span></span>
<span data-ttu-id="10746-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10746-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10746-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="10746-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10746-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10746-133">CommonParameters</span></span>
<span data-ttu-id="10746-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10746-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10746-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10746-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10746-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10746-136">INPUTS</span></span>

### <span data-ttu-id="10746-137">System. String</span><span class="sxs-lookup"><span data-stu-id="10746-137">System.String</span></span>

### <span data-ttu-id="10746-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="10746-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="10746-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10746-139">OUTPUTS</span></span>

### <span data-ttu-id="10746-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="10746-140">System.Boolean</span></span>

## <span data-ttu-id="10746-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10746-141">NOTES</span></span>
* <span data-ttu-id="10746-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="10746-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="10746-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10746-143">RELATED LINKS</span></span>

[<span data-ttu-id="10746-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="10746-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="10746-145">Nowe — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="10746-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="10746-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="10746-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="10746-147">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="10746-147">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="10746-148">Suspend — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="10746-148">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


