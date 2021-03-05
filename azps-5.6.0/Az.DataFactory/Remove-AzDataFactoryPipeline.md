---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 25653cb7423803f2722a87e218c4ee4b3d73be86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972858"
---
# <span data-ttu-id="0044e-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0044e-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="0044e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0044e-102">SYNOPSIS</span></span>
<span data-ttu-id="0044e-103">Usuwa potok z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0044e-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="0044e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0044e-104">SYNTAX</span></span>

### <span data-ttu-id="0044e-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="0044e-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0044e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0044e-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0044e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0044e-107">DESCRIPTION</span></span>
<span data-ttu-id="0044e-108">Polecenie **cmdlet Remove-AzDataFactoryPipeline** usuwa potok z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0044e-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="0044e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0044e-109">EXAMPLES</span></span>

### <span data-ttu-id="0044e-110">Przykład 1. Usuwanie potoku</span><span class="sxs-lookup"><span data-stu-id="0044e-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="0044e-111">To polecenie cmdlet usuwa potok o nazwie DPWikisample z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0044e-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="0044e-112">Polecenie zwróci wartość $True.</span><span class="sxs-lookup"><span data-stu-id="0044e-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="0044e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0044e-113">PARAMETERS</span></span>

### <span data-ttu-id="0044e-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0044e-114">-DataFactory</span></span>
<span data-ttu-id="0044e-115">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="0044e-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="0044e-116">To polecenie cmdlet usuwa potok z fabryki danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0044e-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0044e-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0044e-117">-DataFactoryName</span></span>
<span data-ttu-id="0044e-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0044e-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0044e-119">To polecenie cmdlet usuwa potok z fabryki danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0044e-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0044e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0044e-120">-DefaultProfile</span></span>
<span data-ttu-id="0044e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0044e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0044e-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0044e-122">-Force</span></span>
<span data-ttu-id="0044e-123">Wskazuje, że to polecenie cmdlet usuwa potok bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0044e-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="0044e-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0044e-124">-Name</span></span>
<span data-ttu-id="0044e-125">Określa nazwę potoku do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="0044e-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="0044e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0044e-126">-ResourceGroupName</span></span>
<span data-ttu-id="0044e-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0044e-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0044e-128">To polecenie cmdlet usuwa potok z grupy, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0044e-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0044e-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0044e-129">-Confirm</span></span>
<span data-ttu-id="0044e-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0044e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0044e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0044e-131">-WhatIf</span></span>
<span data-ttu-id="0044e-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0044e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0044e-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0044e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0044e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0044e-134">CommonParameters</span></span>
<span data-ttu-id="0044e-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0044e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0044e-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0044e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0044e-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0044e-137">INPUTS</span></span>

### <span data-ttu-id="0044e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0044e-138">System.String</span></span>

### <span data-ttu-id="0044e-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0044e-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="0044e-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0044e-140">OUTPUTS</span></span>

### <span data-ttu-id="0044e-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="0044e-141">System.Void</span></span>

## <span data-ttu-id="0044e-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0044e-142">NOTES</span></span>
* <span data-ttu-id="0044e-143">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="0044e-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0044e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0044e-144">RELATED LINKS</span></span>

[<span data-ttu-id="0044e-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0044e-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="0044e-146">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0044e-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="0044e-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0044e-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="0044e-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="0044e-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="0044e-149">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0044e-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


