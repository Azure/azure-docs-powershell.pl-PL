---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: f977344f2beabe8352a7417130063c3e9d4d3e1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719658"
---
# <span data-ttu-id="abdfd-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="abdfd-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="abdfd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="abdfd-102">SYNOPSIS</span></span>
<span data-ttu-id="abdfd-103">Łączy magazyn danych lub usługę w chmurze z fabryką danych.</span><span class="sxs-lookup"><span data-stu-id="abdfd-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abdfd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="abdfd-104">SYNTAX</span></span>

### <span data-ttu-id="abdfd-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="abdfd-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="abdfd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="abdfd-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="abdfd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="abdfd-107">DESCRIPTION</span></span>
<span data-ttu-id="abdfd-108">Polecenie cmdlet Set-AzureRmDataFactoryV2LinkedService łączy magazyn danych lub usługę w chmurze z usługą Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="abdfd-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="abdfd-109">Jeśli określisz nazwę połączonej usługi, która już istnieje, to polecenie cmdlet monituje o potwierdzenie przed zastąpieniem połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="abdfd-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="abdfd-110">Jeśli określisz parametr Force, polecenie cmdlet zastępuje istniejącą połączoną usługę bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="abdfd-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="abdfd-111">Wykonuj następujące operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="abdfd-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="abdfd-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="abdfd-112">EXAMPLES</span></span>

### <span data-ttu-id="abdfd-113">Przykład 1. Tworzenie połączonej usługi</span><span class="sxs-lookup"><span data-stu-id="abdfd-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

```

<span data-ttu-id="abdfd-114">To polecenie tworzy połączoną usługę o nazwie LinkedServiceCuratedWikiData w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="abdfd-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="abdfd-115">Ta połączona usługa łączy magazyn obiektów blob platformy Azure określony w pliku z fabryką danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="abdfd-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="abdfd-116">Polecenie przekazuje wynik do polecenia cmdlet Format-List przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="abdfd-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="abdfd-117">To polecenie cmdlet programu Windows PowerShell formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="abdfd-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="abdfd-118">Aby uzyskać więcej informacji, wpisz Get-Help format-lista.</span><span class="sxs-lookup"><span data-stu-id="abdfd-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="abdfd-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="abdfd-119">PARAMETERS</span></span>

### <span data-ttu-id="abdfd-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="abdfd-120">-Confirm</span></span>
<span data-ttu-id="abdfd-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abdfd-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abdfd-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="abdfd-122">-DataFactoryName</span></span>
<span data-ttu-id="abdfd-123">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="abdfd-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="abdfd-124">To polecenie cmdlet tworzy połączoną usługę dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="abdfd-124">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="abdfd-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="abdfd-125">-DefinitionFile</span></span>
<span data-ttu-id="abdfd-126">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="abdfd-126">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abdfd-127">-Force</span><span class="sxs-lookup"><span data-stu-id="abdfd-127">-Force</span></span>
<span data-ttu-id="abdfd-128">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="abdfd-128">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="abdfd-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="abdfd-129">-Name</span></span>
<span data-ttu-id="abdfd-130">Określa nazwę połączonej usługi, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="abdfd-130">Specifies the name of the linked service to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abdfd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abdfd-131">-ResourceGroupName</span></span>
<span data-ttu-id="abdfd-132">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="abdfd-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="abdfd-133">To polecenie cmdlet powoduje utworzenie połączonej usługi dla grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="abdfd-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="abdfd-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abdfd-134">-ResourceId</span></span>
<span data-ttu-id="abdfd-135">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="abdfd-135">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abdfd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abdfd-136">-WhatIf</span></span>
<span data-ttu-id="abdfd-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abdfd-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="abdfd-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abdfd-138">INPUTS</span></span>

### <span data-ttu-id="abdfd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="abdfd-139">System.String</span></span>


## <span data-ttu-id="abdfd-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="abdfd-140">OUTPUTS</span></span>

### <span data-ttu-id="abdfd-141">Microsoft. Azure. Commands. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="abdfd-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>


## <span data-ttu-id="abdfd-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="abdfd-142">NOTES</span></span>
<span data-ttu-id="abdfd-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="abdfd-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="abdfd-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abdfd-144">RELATED LINKS</span></span>
[<span data-ttu-id="abdfd-145">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="abdfd-145">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="abdfd-146">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="abdfd-146">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
