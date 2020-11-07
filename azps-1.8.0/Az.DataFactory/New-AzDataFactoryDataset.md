---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 1d03ba1e4b025be933fd9cd409270d8deb93d1d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710110"
---
# <span data-ttu-id="6c902-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="6c902-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="6c902-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c902-102">SYNOPSIS</span></span>
<span data-ttu-id="6c902-103">Tworzy zestaw danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="6c902-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="6c902-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c902-104">SYNTAX</span></span>

### <span data-ttu-id="6c902-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6c902-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c902-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6c902-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c902-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6c902-107">DESCRIPTION</span></span>
<span data-ttu-id="6c902-108">Polecenie cmdlet **New-AzDataFactoryDataset** tworzy zestaw danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="6c902-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="6c902-109">Jeśli określisz nazwę dla zestawu danych, który już istnieje, to polecenie cmdlet monituje o potwierdzenie przed zastąpieniem zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="6c902-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="6c902-110">Jeśli określisz parametr *Force* , polecenie cmdlet zastępuje istniejący zestaw danych bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="6c902-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="6c902-111">Wykonuj następujące operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="6c902-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="6c902-112">Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6c902-112">Create a data factory.</span></span> 
- <span data-ttu-id="6c902-113">Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="6c902-113">Create linked services.</span></span> 
- <span data-ttu-id="6c902-114">Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="6c902-114">Create datasets.</span></span> 
- <span data-ttu-id="6c902-115">Utwórz rurociąg.</span><span class="sxs-lookup"><span data-stu-id="6c902-115">Create a pipeline.</span></span>
<span data-ttu-id="6c902-116">Jeśli zestaw danych o takiej samej nazwie już istnieje w fabryce danych, to polecenie cmdlet wyświetli monit o potwierdzenie zamiaru zastąpienia istniejącego zestawu danych nowym zestawem danych.</span><span class="sxs-lookup"><span data-stu-id="6c902-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="6c902-117">Jeśli potwierdzisz zastąpienie istniejącego zestawu danych, definicja zestawu danych również zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="6c902-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="6c902-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c902-118">EXAMPLES</span></span>

### <span data-ttu-id="6c902-119">Przykład 1. Tworzenie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="6c902-119">Example 1: Create a dataset</span></span>
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

<span data-ttu-id="6c902-120">To polecenie tworzy zestaw danych o nazwie DA_WikipediaClickEvents w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="6c902-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="6c902-121">Polecenie opiera się na zestawie danych na temat informacji zawartych w DAWikipediaClickEvents.jspliku.</span><span class="sxs-lookup"><span data-stu-id="6c902-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="6c902-122">Przykład 2: Wyświetlanie dostępności nowego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="6c902-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="6c902-123">Pierwsze polecenie powoduje utworzenie zestawu danych o nazwie DA_WikipediaClickEvents, tak jak w poprzednim przykładzie, a następnie przypisanie tego zestawu danych do zmiennej $Dataset.</span><span class="sxs-lookup"><span data-stu-id="6c902-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="6c902-124">Drugie polecenie używa standardowego zapisu kropkowego, aby wyświetlić szczegółowe informacje o właściwości dostępności zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="6c902-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="6c902-125">Przykład 3: Wyświetlanie lokalizacji nowego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="6c902-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="6c902-126">Pierwsze polecenie powoduje utworzenie zestawu danych o nazwie DA_WikipediaClickEvents, tak jak w poprzednim przykładzie, a następnie przypisanie tego zestawu danych do zmiennej $Dataset.</span><span class="sxs-lookup"><span data-stu-id="6c902-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="6c902-127">Drugie polecenie wyświetla szczegółowe informacje dotyczące właściwości lokalizacja zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="6c902-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="6c902-128">Przykład 4: Wyświetlanie reguł sprawdzania poprawności dla nowego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="6c902-128">Example 4: View validation rules for a new dataset</span></span>
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

<span data-ttu-id="6c902-129">Pierwsze polecenie powoduje utworzenie zestawu danych o nazwie DA_WikipediaClickEvents, tak jak w poprzednim przykładzie, a następnie przypisanie tego zestawu danych do zmiennej $Dataset.</span><span class="sxs-lookup"><span data-stu-id="6c902-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="6c902-130">Drugie polecenie pobiera szczegóły dotyczące reguł poprawności dla zestawu danych, a następnie przekazuje je do polecenia cmdlet Format-List przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="6c902-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6c902-131">To polecenie cmdlet programu Windows PowerShell formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="6c902-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="6c902-132">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="6c902-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="6c902-133">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c902-133">PARAMETERS</span></span>

### <span data-ttu-id="6c902-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6c902-134">-DataFactory</span></span>
<span data-ttu-id="6c902-135">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="6c902-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6c902-136">To polecenie cmdlet powoduje utworzenie zestawu danych w fabryce danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6c902-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6c902-137">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6c902-137">-DataFactoryName</span></span>
<span data-ttu-id="6c902-138">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6c902-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6c902-139">To polecenie cmdlet powoduje utworzenie zestawu danych w fabryce danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6c902-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6c902-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c902-140">-DefaultProfile</span></span>
<span data-ttu-id="6c902-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6c902-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c902-142">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="6c902-142">-File</span></span>
<span data-ttu-id="6c902-143">Określa pełną ścieżkę do pliku notacji JavaScript (kod JSON) zawierającego opis zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="6c902-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

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

### <span data-ttu-id="6c902-144">-Force</span><span class="sxs-lookup"><span data-stu-id="6c902-144">-Force</span></span>
<span data-ttu-id="6c902-145">Wskazuje, że to polecenie cmdlet Zamienia istniejący zestaw danych bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6c902-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="6c902-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c902-146">-Name</span></span>
<span data-ttu-id="6c902-147">Określa nazwę zestawu danych, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="6c902-147">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="6c902-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c902-148">-ResourceGroupName</span></span>
<span data-ttu-id="6c902-149">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6c902-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6c902-150">To polecenie cmdlet powoduje utworzenie zestawu danych w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="6c902-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6c902-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c902-151">-Confirm</span></span>
<span data-ttu-id="6c902-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c902-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c902-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c902-153">-WhatIf</span></span>
<span data-ttu-id="6c902-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c902-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c902-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6c902-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c902-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c902-156">CommonParameters</span></span>
<span data-ttu-id="6c902-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c902-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c902-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c902-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c902-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c902-159">INPUTS</span></span>

### <span data-ttu-id="6c902-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6c902-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="6c902-161">System. String</span><span class="sxs-lookup"><span data-stu-id="6c902-161">System.String</span></span>

## <span data-ttu-id="6c902-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c902-162">OUTPUTS</span></span>

### <span data-ttu-id="6c902-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="6c902-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="6c902-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c902-164">NOTES</span></span>
* <span data-ttu-id="6c902-165">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="6c902-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6c902-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c902-166">RELATED LINKS</span></span>

[<span data-ttu-id="6c902-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="6c902-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="6c902-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="6c902-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)

