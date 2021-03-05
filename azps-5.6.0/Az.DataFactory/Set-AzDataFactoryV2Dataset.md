---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5ea766b4c35e23a62a0764320a2f0491ea151586
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006954"
---
# <span data-ttu-id="39449-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="39449-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="39449-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39449-102">SYNOPSIS</span></span>
<span data-ttu-id="39449-103">Tworzy zestaw danych w układzie Data Factory.</span><span class="sxs-lookup"><span data-stu-id="39449-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="39449-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="39449-104">SYNTAX</span></span>

### <span data-ttu-id="39449-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="39449-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39449-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="39449-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39449-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="39449-107">DESCRIPTION</span></span>
<span data-ttu-id="39449-108">Polecenie Set-AzDataFactoryV2Dataset umożliwia utworzenie zestawu danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="39449-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="39449-109">Jeśli określisz nazwę dla zestawu danych, który już istnieje, to polecenie cmdlet wyświetli monit o potwierdzenie przed zastąpieniem zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="39449-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="39449-110">Jeśli określisz parametr Force, polecenie cmdlet zastąpi istniejący zestaw danych bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="39449-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="39449-111">Wykonaj następujące operacje w następującej kolejności: — Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="39449-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="39449-112">— Tworzenie usług połączonych.</span><span class="sxs-lookup"><span data-stu-id="39449-112">-- Create linked services.</span></span>
<span data-ttu-id="39449-113">— Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="39449-113">-- Create datasets.</span></span>
<span data-ttu-id="39449-114">— Tworzenie potoku.</span><span class="sxs-lookup"><span data-stu-id="39449-114">-- Create a pipeline.</span></span>
<span data-ttu-id="39449-115">Jeśli w fabrycznej układzie danych istnieje już zestaw danych o tej samej nazwie, to polecenie cmdlet wyświetli monit o potwierdzenie, czy chcesz zastąpić istniejący zestaw danych nowym zestawem danych.</span><span class="sxs-lookup"><span data-stu-id="39449-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="39449-116">Jeśli potwierdzisz zastąpienie istniejącego zestawu danych, definicja zestawu danych również zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="39449-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="39449-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="39449-117">EXAMPLES</span></span>

### <span data-ttu-id="39449-118">Przykład 1. Tworzenie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="39449-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="39449-119">To polecenie tworzy zestaw danych o nazwie DA_WikipediaClickEvents w zakładzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="39449-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="39449-120">Polecenie bazuje na danych w pliku danych DAWikipediaClickEvents.jspliku.</span><span class="sxs-lookup"><span data-stu-id="39449-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="39449-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39449-121">PARAMETERS</span></span>

### <span data-ttu-id="39449-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="39449-122">-DataFactoryName</span></span>
<span data-ttu-id="39449-123">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="39449-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="39449-124">To polecenie cmdlet tworzy w zakładzie danych zestaw danych, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="39449-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="39449-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39449-125">-DefaultProfile</span></span>
<span data-ttu-id="39449-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="39449-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39449-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="39449-127">-DefinitionFile</span></span>
<span data-ttu-id="39449-128">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="39449-128">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39449-129">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="39449-129">-Force</span></span>
<span data-ttu-id="39449-130">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="39449-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="39449-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="39449-131">-Name</span></span>
<span data-ttu-id="39449-132">Określa nazwę zestawu danych do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="39449-132">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39449-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39449-133">-ResourceGroupName</span></span>
<span data-ttu-id="39449-134">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="39449-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="39449-135">To polecenie cmdlet tworzy zestaw danych w grupie, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="39449-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="39449-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39449-136">-ResourceId</span></span>
<span data-ttu-id="39449-137">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="39449-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="39449-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39449-138">-Confirm</span></span>
<span data-ttu-id="39449-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="39449-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39449-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39449-140">-WhatIf</span></span>
<span data-ttu-id="39449-141">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39449-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="39449-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39449-142">CommonParameters</span></span>
<span data-ttu-id="39449-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39449-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39449-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39449-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39449-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39449-145">INPUTS</span></span>

### <span data-ttu-id="39449-146">System.String</span><span class="sxs-lookup"><span data-stu-id="39449-146">System.String</span></span>

## <span data-ttu-id="39449-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39449-147">OUTPUTS</span></span>

### <span data-ttu-id="39449-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="39449-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="39449-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="39449-149">NOTES</span></span>
<span data-ttu-id="39449-150">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="39449-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="39449-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39449-151">RELATED LINKS</span></span>

[<span data-ttu-id="39449-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="39449-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="39449-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="39449-153">Remove-AzDataFactoryV2Dataset</span></span>]()
