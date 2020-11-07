---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b1d39c3d60d043485cc4ec4dc0c4ba986a97e800
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896341"
---
# <span data-ttu-id="987a7-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="987a7-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="987a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="987a7-102">SYNOPSIS</span></span>
<span data-ttu-id="987a7-103">Usuwa potok z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="987a7-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="987a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="987a7-104">SYNTAX</span></span>

### <span data-ttu-id="987a7-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="987a7-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="987a7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="987a7-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="987a7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="987a7-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="987a7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="987a7-108">DESCRIPTION</span></span>
<span data-ttu-id="987a7-109">Polecenie cmdlet Remove-AzDataFactoryV2Pipeline usuwa potok z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="987a7-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="987a7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="987a7-110">EXAMPLES</span></span>

### <span data-ttu-id="987a7-111">Przykład 1. Usuń rurociąg</span><span class="sxs-lookup"><span data-stu-id="987a7-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="987a7-112">To polecenie cmdlet usuwa potok o nazwie DPWikisample z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="987a7-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="987a7-113">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="987a7-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="987a7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="987a7-114">PARAMETERS</span></span>

### <span data-ttu-id="987a7-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="987a7-115">-DataFactoryName</span></span>
<span data-ttu-id="987a7-116">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="987a7-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="987a7-117">To polecenie cmdlet usuwa potok z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="987a7-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="987a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987a7-118">-DefaultProfile</span></span>
<span data-ttu-id="987a7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="987a7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="987a7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="987a7-120">-Force</span></span>
<span data-ttu-id="987a7-121">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="987a7-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="987a7-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="987a7-122">-InputObject</span></span>
<span data-ttu-id="987a7-123">Określa obiekt potoku.</span><span class="sxs-lookup"><span data-stu-id="987a7-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="987a7-124">To polecenie cmdlet usuwa potok, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="987a7-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="987a7-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="987a7-125">-Name</span></span>
<span data-ttu-id="987a7-126">Określa nazwę potoku, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="987a7-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="987a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="987a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="987a7-128">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="987a7-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="987a7-129">To polecenie cmdlet usuwa potok z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="987a7-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="987a7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="987a7-130">-ResourceId</span></span>
<span data-ttu-id="987a7-131">Identyfikator zasobu platformy Azure potoku, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="987a7-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="987a7-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="987a7-132">-Confirm</span></span>
<span data-ttu-id="987a7-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="987a7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="987a7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="987a7-134">-WhatIf</span></span>
<span data-ttu-id="987a7-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="987a7-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="987a7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987a7-136">CommonParameters</span></span>
<span data-ttu-id="987a7-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="987a7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987a7-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="987a7-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987a7-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="987a7-139">INPUTS</span></span>

### <span data-ttu-id="987a7-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="987a7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="987a7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="987a7-141">System.String</span></span>

## <span data-ttu-id="987a7-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="987a7-142">OUTPUTS</span></span>

### <span data-ttu-id="987a7-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="987a7-143">System.Boolean</span></span>

## <span data-ttu-id="987a7-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="987a7-144">NOTES</span></span>
<span data-ttu-id="987a7-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="987a7-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="987a7-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="987a7-146">RELATED LINKS</span></span>

[<span data-ttu-id="987a7-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="987a7-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="987a7-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="987a7-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="987a7-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="987a7-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

