---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: eb832037080550a1a22c3cacce2386eba7c4e6f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971137"
---
# <span data-ttu-id="adeeb-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="adeeb-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="adeeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adeeb-102">SYNOPSIS</span></span>
<span data-ttu-id="adeeb-103">Usuwa potok z aplikacji Data Factory.</span><span class="sxs-lookup"><span data-stu-id="adeeb-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="adeeb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="adeeb-104">SYNTAX</span></span>

### <span data-ttu-id="adeeb-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="adeeb-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adeeb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="adeeb-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adeeb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="adeeb-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adeeb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="adeeb-108">DESCRIPTION</span></span>
<span data-ttu-id="adeeb-109">Polecenie Remove-AzDataFactoryV2Pipeline usuwa potok z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="adeeb-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="adeeb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="adeeb-110">EXAMPLES</span></span>

### <span data-ttu-id="adeeb-111">Przykład 1. Usuwanie potoku</span><span class="sxs-lookup"><span data-stu-id="adeeb-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="adeeb-112">To polecenie cmdlet usuwa potok o nazwie DPWikisample z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="adeeb-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="adeeb-113">Polecenie zwróci wartość $True.</span><span class="sxs-lookup"><span data-stu-id="adeeb-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="adeeb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adeeb-114">PARAMETERS</span></span>

### <span data-ttu-id="adeeb-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="adeeb-115">-DataFactoryName</span></span>
<span data-ttu-id="adeeb-116">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="adeeb-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="adeeb-117">To polecenie cmdlet usuwa potok z fabryki danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="adeeb-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="adeeb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adeeb-118">-DefaultProfile</span></span>
<span data-ttu-id="adeeb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="adeeb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adeeb-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="adeeb-120">-Force</span></span>
<span data-ttu-id="adeeb-121">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="adeeb-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="adeeb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adeeb-122">-InputObject</span></span>
<span data-ttu-id="adeeb-123">Określa obiekt Pipeline.</span><span class="sxs-lookup"><span data-stu-id="adeeb-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="adeeb-124">To polecenie cmdlet usuwa potok, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="adeeb-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adeeb-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="adeeb-125">-Name</span></span>
<span data-ttu-id="adeeb-126">Określa nazwę potoku do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="adeeb-126">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adeeb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adeeb-127">-ResourceGroupName</span></span>
<span data-ttu-id="adeeb-128">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="adeeb-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="adeeb-129">To polecenie cmdlet usuwa potok z grupy, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="adeeb-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="adeeb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adeeb-130">-ResourceId</span></span>
<span data-ttu-id="adeeb-131">Identyfikator zasobu Azure w potoku do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="adeeb-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="adeeb-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="adeeb-132">-Confirm</span></span>
<span data-ttu-id="adeeb-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="adeeb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adeeb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adeeb-134">-WhatIf</span></span>
<span data-ttu-id="adeeb-135">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adeeb-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="adeeb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adeeb-136">CommonParameters</span></span>
<span data-ttu-id="adeeb-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adeeb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adeeb-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adeeb-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adeeb-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adeeb-139">INPUTS</span></span>

### <span data-ttu-id="adeeb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="adeeb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="adeeb-141">System.String</span><span class="sxs-lookup"><span data-stu-id="adeeb-141">System.String</span></span>

## <span data-ttu-id="adeeb-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adeeb-142">OUTPUTS</span></span>

### <span data-ttu-id="adeeb-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="adeeb-143">System.Boolean</span></span>

## <span data-ttu-id="adeeb-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="adeeb-144">NOTES</span></span>
<span data-ttu-id="adeeb-145">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="adeeb-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="adeeb-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="adeeb-146">RELATED LINKS</span></span>

[<span data-ttu-id="adeeb-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="adeeb-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="adeeb-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="adeeb-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="adeeb-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="adeeb-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

