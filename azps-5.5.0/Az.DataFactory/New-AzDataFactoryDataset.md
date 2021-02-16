---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 38af817205f8d80615fa94799eee5a7a54f05e78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242810"
---
# <span data-ttu-id="7ee1c-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="7ee1c-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="7ee1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ee1c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee1c-103">Tworzy zestaw danych w układzie Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="7ee1c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7ee1c-104">SYNTAX</span></span>

### <span data-ttu-id="7ee1c-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="7ee1c-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ee1c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7ee1c-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ee1c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7ee1c-107">DESCRIPTION</span></span>
<span data-ttu-id="7ee1c-108">Polecenie **cmdlet New-AzDataFactoryDataset** tworzy zestaw danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="7ee1c-109">Jeśli określisz nazwę dla zestawu danych, który już istnieje, to polecenie cmdlet wyświetli monit o potwierdzenie przed zastąpieniem zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="7ee1c-110">Jeśli określisz parametr *Force,* polecenie cmdlet zastąpi istniejący zestaw danych bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="7ee1c-111">Wykonaj te operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="7ee1c-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="7ee1c-112">Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-112">Create a data factory.</span></span> 
- <span data-ttu-id="7ee1c-113">Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-113">Create linked services.</span></span> 
- <span data-ttu-id="7ee1c-114">Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-114">Create datasets.</span></span> 
- <span data-ttu-id="7ee1c-115">Tworzenie potoku.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-115">Create a pipeline.</span></span>
<span data-ttu-id="7ee1c-116">Jeśli w fabrycznej układzie danych istnieje już zestaw danych o tej samej nazwie, to polecenie cmdlet wyświetli monit o potwierdzenie, czy chcesz zastąpić istniejący zestaw danych nowym zestawem danych.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="7ee1c-117">Jeśli potwierdzisz zastąpienie istniejącego zestawu danych, definicja zestawu danych również zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="7ee1c-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7ee1c-118">EXAMPLES</span></span>

### <span data-ttu-id="7ee1c-119">Przykład 1. Tworzenie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="7ee1c-119">Example 1: Create a dataset</span></span>
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="7ee1c-120">To polecenie tworzy zestaw danych o nazwie DA_WikipediaClickEvents w zakładzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="7ee1c-121">Polecenie bazuje na danych w pliku danych DAWikipediaClickEvents.jspliku.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="7ee1c-122">Przykład 2. Wyświetlanie dostępności nowego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="7ee1c-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="7ee1c-123">Pierwsze polecenie tworzy zestaw danych o nazwie DA_WikipediaClickEvents, tak jak w poprzednim przykładzie, a następnie przypisuje go do zmiennej $Dataset danych.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="7ee1c-124">Drugie polecenie używa standardowej notacji kropki w celu wyświetlenia szczegółów właściwości Dostępność zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="7ee1c-125">Przykład 3. Wyświetlanie lokalizacji nowego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="7ee1c-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="7ee1c-126">Pierwsze polecenie tworzy zestaw danych o nazwie DA_WikipediaClickEvents, tak jak w poprzednim przykładzie, a następnie przypisuje go do zmiennej $Dataset danych.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="7ee1c-127">Drugie polecenie wyświetla szczegółowe informacje o właściwości Lokalizacja zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="7ee1c-128">Przykład 4. Wyświetlanie reguł poprawności dla nowego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="7ee1c-128">Example 4: View validation rules for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

<span data-ttu-id="7ee1c-129">Pierwsze polecenie tworzy zestaw danych o nazwie DA_WikipediaClickEvents, tak jak w poprzednim przykładzie, a następnie przypisuje go do zmiennej $Dataset danych.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="7ee1c-130">Drugie polecenie pobiera szczegółowe informacje o regułach poprawności dla zestawu danych, a następnie przekazuje je do polecenia cmdlet Format-List za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7ee1c-131">Polecenie cmdlet programu Windows PowerShell formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="7ee1c-132">Aby uzyskać więcej informacji, wpisz `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="7ee1c-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="7ee1c-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ee1c-133">PARAMETERS</span></span>

### <span data-ttu-id="7ee1c-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ee1c-134">-DataFactory</span></span>
<span data-ttu-id="7ee1c-135">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="7ee1c-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7ee1c-136">To polecenie cmdlet tworzy w zakładzie danych zestaw danych, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7ee1c-137">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7ee1c-137">-DataFactoryName</span></span>
<span data-ttu-id="7ee1c-138">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7ee1c-139">To polecenie cmdlet tworzy w zakładzie danych zestaw danych, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7ee1c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ee1c-140">-DefaultProfile</span></span>
<span data-ttu-id="7ee1c-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7ee1c-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ee1c-142">— Plik</span><span class="sxs-lookup"><span data-stu-id="7ee1c-142">-File</span></span>
<span data-ttu-id="7ee1c-143">Określa pełną ścieżkę pliku JavaScript Object Notation (JSON) zawierającego opis zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee1c-144">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7ee1c-144">-Force</span></span>
<span data-ttu-id="7ee1c-145">Wskazuje, że to polecenie cmdlet zastępuje istniejący zestaw danych bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7ee1c-146">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7ee1c-146">-Name</span></span>
<span data-ttu-id="7ee1c-147">Określa nazwę zestawu danych do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-147">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee1c-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee1c-148">-ResourceGroupName</span></span>
<span data-ttu-id="7ee1c-149">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7ee1c-150">To polecenie cmdlet tworzy zestaw danych w grupie, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7ee1c-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ee1c-151">-Confirm</span></span>
<span data-ttu-id="7ee1c-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ee1c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ee1c-153">-WhatIf</span></span>
<span data-ttu-id="7ee1c-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ee1c-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ee1c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee1c-156">CommonParameters</span></span>
<span data-ttu-id="7ee1c-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ee1c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee1c-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ee1c-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee1c-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ee1c-159">INPUTS</span></span>

### <span data-ttu-id="7ee1c-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7ee1c-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="7ee1c-161">System.String</span><span class="sxs-lookup"><span data-stu-id="7ee1c-161">System.String</span></span>

## <span data-ttu-id="7ee1c-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ee1c-162">OUTPUTS</span></span>

### <span data-ttu-id="7ee1c-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="7ee1c-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="7ee1c-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7ee1c-164">NOTES</span></span>
* <span data-ttu-id="7ee1c-165">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="7ee1c-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7ee1c-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ee1c-166">RELATED LINKS</span></span>

[<span data-ttu-id="7ee1c-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="7ee1c-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="7ee1c-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="7ee1c-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


