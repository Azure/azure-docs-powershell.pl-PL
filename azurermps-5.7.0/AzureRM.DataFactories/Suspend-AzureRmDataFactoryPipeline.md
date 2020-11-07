---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/suspend-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 98c8d5778e827b251c5d0c9b919bde9f86e2c41e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716625"
---
# <span data-ttu-id="83aee-101">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="83aee-101">Suspend-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="83aee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83aee-102">SYNOPSIS</span></span>
<span data-ttu-id="83aee-103">Wstrzymuje rurociąg w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="83aee-103">Suspends a pipeline in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83aee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83aee-104">SYNTAX</span></span>

### <span data-ttu-id="83aee-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="83aee-105">ByFactoryName (Default)</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83aee-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="83aee-106">ByFactoryObject</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83aee-107">Opis</span><span class="sxs-lookup"><span data-stu-id="83aee-107">DESCRIPTION</span></span>
<span data-ttu-id="83aee-108">Polecenie cmdlet **Suspend-AzureRmDataFactoryPipeline** zawiesza rurociąg w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="83aee-108">The **Suspend-AzureRmDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="83aee-109">Możesz wznowić rurociąg, korzystając z polecenia cmdlet Resume-AzureRmDataFactoryPipeline.</span><span class="sxs-lookup"><span data-stu-id="83aee-109">You can resume the pipeline by using the Resume-AzureRmDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="83aee-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83aee-110">EXAMPLES</span></span>

### <span data-ttu-id="83aee-111">Przykład 1: Wstrzymywanie rurociągu</span><span class="sxs-lookup"><span data-stu-id="83aee-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="83aee-112">To polecenie zawiesza potok o nazwie DPWikiSample w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="83aee-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="83aee-113">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="83aee-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="83aee-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83aee-114">PARAMETERS</span></span>

### <span data-ttu-id="83aee-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="83aee-115">-DataFactory</span></span>
<span data-ttu-id="83aee-116">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="83aee-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="83aee-117">To polecenie cmdlet zawiesza potok należący do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="83aee-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83aee-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="83aee-118">-DataFactoryName</span></span>
<span data-ttu-id="83aee-119">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="83aee-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="83aee-120">To polecenie cmdlet zawiesza potok należący do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="83aee-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83aee-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83aee-121">-DefaultProfile</span></span>
<span data-ttu-id="83aee-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="83aee-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83aee-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="83aee-123">-Name</span></span>
<span data-ttu-id="83aee-124">Określa nazwę potoku, który ma zostać zawieszony.</span><span class="sxs-lookup"><span data-stu-id="83aee-124">Specifies the name of the pipeline to suspend.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83aee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83aee-125">-ResourceGroupName</span></span>
<span data-ttu-id="83aee-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="83aee-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="83aee-127">To polecenie cmdlet zawiesza potok należący do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="83aee-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83aee-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83aee-128">-Confirm</span></span>
<span data-ttu-id="83aee-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83aee-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83aee-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83aee-130">-WhatIf</span></span>
<span data-ttu-id="83aee-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83aee-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83aee-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83aee-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83aee-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83aee-133">CommonParameters</span></span>
<span data-ttu-id="83aee-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83aee-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83aee-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83aee-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83aee-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83aee-136">INPUTS</span></span>

### <span data-ttu-id="83aee-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="83aee-137">None</span></span>
<span data-ttu-id="83aee-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="83aee-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83aee-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83aee-139">OUTPUTS</span></span>

### <span data-ttu-id="83aee-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83aee-140">System.Boolean</span></span>

## <span data-ttu-id="83aee-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83aee-141">NOTES</span></span>
* <span data-ttu-id="83aee-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="83aee-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="83aee-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83aee-143">RELATED LINKS</span></span>

[<span data-ttu-id="83aee-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="83aee-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="83aee-145">Nowe — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="83aee-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="83aee-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="83aee-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="83aee-147">Życiorys — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="83aee-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="83aee-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="83aee-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


