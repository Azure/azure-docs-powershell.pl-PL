---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: dec686838bd7826b57e7b158f4ed741608eaf782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526890"
---
# <span data-ttu-id="e454f-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e454f-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="e454f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e454f-102">SYNOPSIS</span></span>
<span data-ttu-id="e454f-103">Usuwa potok z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e454f-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e454f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e454f-104">SYNTAX</span></span>

### <span data-ttu-id="e454f-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e454f-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e454f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e454f-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e454f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e454f-107">DESCRIPTION</span></span>
<span data-ttu-id="e454f-108">Polecenie cmdlet **Remove-AzureRmDataFactoryPipeline** usuwa potok z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e454f-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="e454f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e454f-109">EXAMPLES</span></span>

### <span data-ttu-id="e454f-110">Przykład 1. Usuń rurociąg</span><span class="sxs-lookup"><span data-stu-id="e454f-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="e454f-111">To polecenie cmdlet usuwa potok o nazwie DPWikisample z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e454f-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="e454f-112">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="e454f-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="e454f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e454f-113">PARAMETERS</span></span>

### <span data-ttu-id="e454f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e454f-114">-DataFactory</span></span>
<span data-ttu-id="e454f-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="e454f-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e454f-116">To polecenie cmdlet usuwa potok z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e454f-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e454f-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e454f-117">-DataFactoryName</span></span>
<span data-ttu-id="e454f-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e454f-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e454f-119">To polecenie cmdlet usuwa potok z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e454f-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e454f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e454f-120">-DefaultProfile</span></span>
<span data-ttu-id="e454f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e454f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e454f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e454f-122">-Force</span></span>
<span data-ttu-id="e454f-123">Wskazuje, że to polecenie cmdlet usunie potok bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e454f-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e454f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e454f-124">-Name</span></span>
<span data-ttu-id="e454f-125">Określa nazwę potoku, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e454f-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="e454f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e454f-126">-ResourceGroupName</span></span>
<span data-ttu-id="e454f-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e454f-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e454f-128">To polecenie cmdlet usuwa potok z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="e454f-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e454f-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e454f-129">-Confirm</span></span>
<span data-ttu-id="e454f-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e454f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e454f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e454f-131">-WhatIf</span></span>
<span data-ttu-id="e454f-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e454f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e454f-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e454f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e454f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e454f-134">CommonParameters</span></span>
<span data-ttu-id="e454f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e454f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e454f-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e454f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e454f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e454f-137">INPUTS</span></span>

### <span data-ttu-id="e454f-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e454f-138">None</span></span>
<span data-ttu-id="e454f-139">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e454f-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e454f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e454f-140">OUTPUTS</span></span>

### <span data-ttu-id="e454f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e454f-141">System.Boolean</span></span>

## <span data-ttu-id="e454f-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e454f-142">NOTES</span></span>
* <span data-ttu-id="e454f-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="e454f-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e454f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e454f-144">RELATED LINKS</span></span>

[<span data-ttu-id="e454f-145">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e454f-145">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="e454f-146">Nowe — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e454f-146">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="e454f-147">Życiorys — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e454f-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="e454f-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="e454f-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="e454f-149">Suspend — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e454f-149">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


