---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 7db88488ccf60865654169233bb19025eae080d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180994"
---
# <span data-ttu-id="6a030-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="6a030-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="6a030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a030-102">SYNOPSIS</span></span>
<span data-ttu-id="6a030-103">Usuwa zestaw danych z aplikacji Data Factory.</span><span class="sxs-lookup"><span data-stu-id="6a030-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="6a030-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6a030-104">SYNTAX</span></span>

### <span data-ttu-id="6a030-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="6a030-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a030-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6a030-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a030-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a030-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a030-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6a030-108">DESCRIPTION</span></span>
<span data-ttu-id="6a030-109">Polecenie Remove-AzDataFactoryV2Dataset usuwa zestaw danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="6a030-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="6a030-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6a030-110">EXAMPLES</span></span>

### <span data-ttu-id="6a030-111">Przykład 1. Usuwanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="6a030-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="6a030-112">To polecenie usuwa zestaw danych o nazwie DAWikiAggregatedData z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="6a030-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="6a030-113">Polecenie zwróci wartość $True.</span><span class="sxs-lookup"><span data-stu-id="6a030-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="6a030-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a030-114">PARAMETERS</span></span>

### <span data-ttu-id="6a030-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6a030-115">-DataFactoryName</span></span>
<span data-ttu-id="6a030-116">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6a030-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6a030-117">To polecenie cmdlet usuwa zestaw danych z fabrycznej bazy danych, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="6a030-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6a030-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a030-118">-DefaultProfile</span></span>
<span data-ttu-id="6a030-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a030-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a030-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6a030-120">-Force</span></span>
<span data-ttu-id="6a030-121">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6a030-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6a030-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a030-122">-InputObject</span></span>
<span data-ttu-id="6a030-123">Określa obiekt Dataset do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="6a030-123">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a030-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6a030-124">-Name</span></span>
<span data-ttu-id="6a030-125">Określa nazwę zestawu danych do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="6a030-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a030-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a030-126">-ResourceGroupName</span></span>
<span data-ttu-id="6a030-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6a030-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6a030-128">To polecenie cmdlet usuwa zestaw danych z grupy, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6a030-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6a030-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a030-129">-ResourceId</span></span>
<span data-ttu-id="6a030-130">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="6a030-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6a030-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a030-131">-Confirm</span></span>
<span data-ttu-id="6a030-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6a030-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a030-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a030-133">-WhatIf</span></span>
<span data-ttu-id="6a030-134">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a030-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6a030-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a030-135">CommonParameters</span></span>
<span data-ttu-id="6a030-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a030-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a030-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a030-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a030-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a030-138">INPUTS</span></span>

### <span data-ttu-id="6a030-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="6a030-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="6a030-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6a030-140">System.String</span></span>

## <span data-ttu-id="6a030-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a030-141">OUTPUTS</span></span>

### <span data-ttu-id="6a030-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="6a030-142">System.Void</span></span>

## <span data-ttu-id="6a030-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6a030-143">NOTES</span></span>
<span data-ttu-id="6a030-144">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="6a030-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6a030-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a030-145">RELATED LINKS</span></span>

[<span data-ttu-id="6a030-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="6a030-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="6a030-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="6a030-147">Set-AzDataFactoryV2Dataset</span></span>]()
