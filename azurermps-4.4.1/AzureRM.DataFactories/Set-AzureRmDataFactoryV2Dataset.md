---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 4254a243894893e58c1c59ea19a8953ddcc8f101
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527654"
---
# <span data-ttu-id="5b90b-101">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="5b90b-101">Set-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="5b90b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b90b-102">SYNOPSIS</span></span>
<span data-ttu-id="5b90b-103">Tworzy zestaw danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="5b90b-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b90b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b90b-104">SYNTAX</span></span>

### <span data-ttu-id="5b90b-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5b90b-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b90b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b90b-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b90b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5b90b-107">DESCRIPTION</span></span>
<span data-ttu-id="5b90b-108">Polecenie cmdlet Set-AzureRmDataFactoryV2Dataset powoduje utworzenie zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5b90b-108">The Set-AzureRmDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="5b90b-109">Jeśli określisz nazwę dla zestawu danych, który już istnieje, to polecenie cmdlet monituje o potwierdzenie przed zastąpieniem zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="5b90b-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="5b90b-110">Jeśli określisz parametr Force, polecenie cmdlet zastępuje istniejący zestaw danych bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="5b90b-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>

<span data-ttu-id="5b90b-111">Wykonuj następujące operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="5b90b-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="5b90b-112">Jeśli zestaw danych o takiej samej nazwie już istnieje w fabryce danych, to polecenie cmdlet wyświetli monit o potwierdzenie zamiaru zastąpienia istniejącego zestawu danych nowym zestawem danych.</span><span class="sxs-lookup"><span data-stu-id="5b90b-112">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="5b90b-113">Jeśli potwierdzisz zastąpienie istniejącego zestawu danych, definicja zestawu danych również zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="5b90b-113">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="5b90b-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b90b-114">EXAMPLES</span></span>

### <span data-ttu-id="5b90b-115">Przykład 1. Tworzenie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="5b90b-115">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="5b90b-116">To polecenie tworzy zestaw danych o nazwie DA_WikipediaClickEvents w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5b90b-116">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="5b90b-117">Polecenie opiera się na zestawie danych na temat informacji zawartych w DAWikipediaClickEvents.jspliku.</span><span class="sxs-lookup"><span data-stu-id="5b90b-117">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="5b90b-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b90b-118">PARAMETERS</span></span>

### <span data-ttu-id="5b90b-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5b90b-119">-Confirm</span></span>
<span data-ttu-id="5b90b-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b90b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b90b-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5b90b-121">-DataFactoryName</span></span>
<span data-ttu-id="5b90b-122">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5b90b-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5b90b-123">To polecenie cmdlet powoduje utworzenie zestawu danych w fabryce danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5b90b-123">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5b90b-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="5b90b-124">-DefinitionFile</span></span>
<span data-ttu-id="5b90b-125">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="5b90b-125">The JSON file path.</span></span>

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

### <span data-ttu-id="5b90b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="5b90b-126">-Force</span></span>
<span data-ttu-id="5b90b-127">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5b90b-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5b90b-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5b90b-128">-Name</span></span>
<span data-ttu-id="5b90b-129">Określa nazwę zestawu danych, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="5b90b-129">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="5b90b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b90b-130">-ResourceGroupName</span></span>
<span data-ttu-id="5b90b-131">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5b90b-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5b90b-132">To polecenie cmdlet powoduje utworzenie zestawu danych w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="5b90b-132">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5b90b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b90b-133">-ResourceId</span></span>
<span data-ttu-id="5b90b-134">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5b90b-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5b90b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b90b-135">-WhatIf</span></span>
<span data-ttu-id="5b90b-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b90b-136">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5b90b-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b90b-137">-DefaultProfile</span></span>
<span data-ttu-id="5b90b-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b90b-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b90b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b90b-139">CommonParameters</span></span>
<span data-ttu-id="5b90b-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b90b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b90b-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b90b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b90b-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b90b-142">INPUTS</span></span>

### <span data-ttu-id="5b90b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5b90b-143">System.String</span></span>

## <span data-ttu-id="5b90b-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b90b-144">OUTPUTS</span></span>

### <span data-ttu-id="5b90b-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="5b90b-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="5b90b-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b90b-146">NOTES</span></span>
<span data-ttu-id="5b90b-147">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="5b90b-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5b90b-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b90b-148">RELATED LINKS</span></span>

[<span data-ttu-id="5b90b-149">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="5b90b-149">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="5b90b-150">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="5b90b-150">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
