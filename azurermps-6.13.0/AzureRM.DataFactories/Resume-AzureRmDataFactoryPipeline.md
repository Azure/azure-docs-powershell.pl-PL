---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/resume-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 298a86c05cc318fbe360cddd2341901070601d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526206"
---
# <span data-ttu-id="6f846-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6f846-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="6f846-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f846-102">SYNOPSIS</span></span>
<span data-ttu-id="6f846-103">Wznawia zawieszoną rurociąg w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="6f846-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f846-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f846-104">SYNTAX</span></span>

### <span data-ttu-id="6f846-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6f846-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f846-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6f846-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f846-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6f846-107">DESCRIPTION</span></span>
<span data-ttu-id="6f846-108">Polecenie cmdlet **Resume-AzureRmDataFactoryPipeline** Wznawia zawieszone potoku w fabryce danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6f846-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="6f846-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f846-109">EXAMPLES</span></span>

### <span data-ttu-id="6f846-110">Przykład 1: wznowienie procesu</span><span class="sxs-lookup"><span data-stu-id="6f846-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="6f846-111">To polecenie wznawia potok o nazwie DPWikisample w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="6f846-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="6f846-112">Aby zawiesić rurociąg, użyj polecenia cmdlet **Suspend-AzureRmDataFactoryPipeline** .</span><span class="sxs-lookup"><span data-stu-id="6f846-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="6f846-113">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="6f846-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="6f846-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f846-114">PARAMETERS</span></span>

### <span data-ttu-id="6f846-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f846-115">-DataFactory</span></span>
<span data-ttu-id="6f846-116">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="6f846-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6f846-117">To polecenie cmdlet powoduje wznowienie pracy rurociągu należącego do fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="6f846-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f846-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6f846-118">-DataFactoryName</span></span>
<span data-ttu-id="6f846-119">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6f846-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6f846-120">To polecenie cmdlet powoduje wznowienie pracy rurociągu należącego do fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="6f846-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f846-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f846-121">-DefaultProfile</span></span>
<span data-ttu-id="6f846-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6f846-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f846-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6f846-123">-Name</span></span>
<span data-ttu-id="6f846-124">Określa nazwę potoku, który ma zostać wznowiony.</span><span class="sxs-lookup"><span data-stu-id="6f846-124">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="6f846-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f846-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f846-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6f846-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6f846-127">To polecenie cmdlet powoduje wznowienie pracy rurociągu należącego do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="6f846-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f846-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6f846-128">-Confirm</span></span>
<span data-ttu-id="6f846-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f846-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f846-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f846-130">-WhatIf</span></span>
<span data-ttu-id="6f846-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f846-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f846-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6f846-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f846-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f846-133">CommonParameters</span></span>
<span data-ttu-id="6f846-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f846-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f846-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f846-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f846-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f846-136">INPUTS</span></span>

### <span data-ttu-id="6f846-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6f846-137">System.String</span></span>

### <span data-ttu-id="6f846-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6f846-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="6f846-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f846-139">OUTPUTS</span></span>

### <span data-ttu-id="6f846-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f846-140">System.Boolean</span></span>

## <span data-ttu-id="6f846-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f846-141">NOTES</span></span>
* <span data-ttu-id="6f846-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="6f846-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6f846-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f846-143">RELATED LINKS</span></span>

[<span data-ttu-id="6f846-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6f846-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="6f846-145">Nowe — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6f846-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="6f846-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6f846-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="6f846-147">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="6f846-147">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="6f846-148">Suspend — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6f846-148">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


