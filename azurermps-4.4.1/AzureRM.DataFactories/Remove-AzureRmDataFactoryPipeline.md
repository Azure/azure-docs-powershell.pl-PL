---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 48638f53f58fd420e9a7b3dfe2e50a3e61d2314f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527661"
---
# <span data-ttu-id="b35f3-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b35f3-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="b35f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b35f3-102">SYNOPSIS</span></span>
<span data-ttu-id="b35f3-103">Usuwa potok z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b35f3-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b35f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b35f3-104">SYNTAX</span></span>

### <span data-ttu-id="b35f3-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b35f3-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b35f3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b35f3-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b35f3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b35f3-107">DESCRIPTION</span></span>
<span data-ttu-id="b35f3-108">Polecenie cmdlet **Remove-AzureRmDataFactoryPipeline** usuwa potok z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b35f3-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="b35f3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b35f3-109">EXAMPLES</span></span>

### <span data-ttu-id="b35f3-110">Przykład 1. Usuń rurociąg</span><span class="sxs-lookup"><span data-stu-id="b35f3-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="b35f3-111">To polecenie cmdlet usuwa potok o nazwie DPWikisample z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b35f3-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="b35f3-112">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="b35f3-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="b35f3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b35f3-113">PARAMETERS</span></span>

### <span data-ttu-id="b35f3-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b35f3-114">-DataFactory</span></span>
<span data-ttu-id="b35f3-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="b35f3-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b35f3-116">To polecenie cmdlet usuwa potok z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b35f3-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b35f3-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b35f3-117">-DataFactoryName</span></span>
<span data-ttu-id="b35f3-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="b35f3-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b35f3-119">To polecenie cmdlet usuwa potok z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b35f3-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b35f3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b35f3-120">-Force</span></span>
<span data-ttu-id="b35f3-121">Wskazuje, że to polecenie cmdlet usunie potok bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b35f3-121">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b35f3-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b35f3-122">-Name</span></span>
<span data-ttu-id="b35f3-123">Określa nazwę potoku, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="b35f3-123">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="b35f3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b35f3-124">-ResourceGroupName</span></span>
<span data-ttu-id="b35f3-125">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b35f3-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b35f3-126">To polecenie cmdlet usuwa potok z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="b35f3-126">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b35f3-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b35f3-127">-Confirm</span></span>
<span data-ttu-id="b35f3-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b35f3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b35f3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b35f3-129">-WhatIf</span></span>
<span data-ttu-id="b35f3-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b35f3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b35f3-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b35f3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b35f3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35f3-132">-DefaultProfile</span></span>
<span data-ttu-id="b35f3-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b35f3-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b35f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35f3-134">CommonParameters</span></span>
<span data-ttu-id="b35f3-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b35f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35f3-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b35f3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35f3-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b35f3-137">INPUTS</span></span>

## <span data-ttu-id="b35f3-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b35f3-138">OUTPUTS</span></span>

### <span data-ttu-id="b35f3-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b35f3-139">System.Boolean</span></span>

## <span data-ttu-id="b35f3-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b35f3-140">NOTES</span></span>
* <span data-ttu-id="b35f3-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="b35f3-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b35f3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b35f3-142">RELATED LINKS</span></span>

[<span data-ttu-id="b35f3-143">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b35f3-143">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="b35f3-144">Nowe — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b35f3-144">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="b35f3-145">Życiorys — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b35f3-145">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="b35f3-146">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="b35f3-146">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="b35f3-147">Suspend — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b35f3-147">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


