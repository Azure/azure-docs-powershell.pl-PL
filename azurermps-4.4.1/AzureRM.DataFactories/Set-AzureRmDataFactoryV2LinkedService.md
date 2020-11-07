---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 5e0ee389a5d2d126cfbccc2a91b1644d81a5fedf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719344"
---
# <span data-ttu-id="ac063-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ac063-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="ac063-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac063-102">SYNOPSIS</span></span>
<span data-ttu-id="ac063-103">Łączy magazyn danych lub usługę w chmurze z fabryką danych.</span><span class="sxs-lookup"><span data-stu-id="ac063-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac063-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac063-104">SYNTAX</span></span>

### <span data-ttu-id="ac063-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ac063-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac063-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac063-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac063-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ac063-107">DESCRIPTION</span></span>
<span data-ttu-id="ac063-108">Polecenie cmdlet Set-AzureRmDataFactoryV2LinkedService łączy magazyn danych lub usługę w chmurze z usługą Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ac063-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="ac063-109">Jeśli określisz nazwę połączonej usługi, która już istnieje, to polecenie cmdlet monituje o potwierdzenie przed zastąpieniem połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="ac063-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="ac063-110">Jeśli określisz parametr Force, polecenie cmdlet zastępuje istniejącą połączoną usługę bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="ac063-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="ac063-111">Wykonuj następujące operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="ac063-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="ac063-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac063-112">EXAMPLES</span></span>

### <span data-ttu-id="ac063-113">Przykład 1. Tworzenie połączonej usługi</span><span class="sxs-lookup"><span data-stu-id="ac063-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="ac063-114">To polecenie tworzy połączoną usługę o nazwie LinkedServiceCuratedWikiData w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ac063-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="ac063-115">Ta połączona usługa łączy magazyn obiektów blob platformy Azure określony w pliku z fabryką danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ac063-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="ac063-116">Polecenie przekazuje wynik do polecenia cmdlet Format-List przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="ac063-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ac063-117">To polecenie cmdlet programu Windows PowerShell formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="ac063-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="ac063-118">Aby uzyskać więcej informacji, wpisz Get-Help format-lista.</span><span class="sxs-lookup"><span data-stu-id="ac063-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="ac063-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac063-119">PARAMETERS</span></span>

### <span data-ttu-id="ac063-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac063-120">-Confirm</span></span>
<span data-ttu-id="ac063-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac063-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac063-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ac063-122">-DataFactoryName</span></span>
<span data-ttu-id="ac063-123">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="ac063-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ac063-124">To polecenie cmdlet tworzy połączoną usługę dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ac063-124">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac063-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="ac063-125">-DefinitionFile</span></span>
<span data-ttu-id="ac063-126">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="ac063-126">The JSON file path.</span></span>

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

### <span data-ttu-id="ac063-127">-Force</span><span class="sxs-lookup"><span data-stu-id="ac063-127">-Force</span></span>
<span data-ttu-id="ac063-128">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ac063-128">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ac063-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ac063-129">-Name</span></span>
<span data-ttu-id="ac063-130">Określa nazwę połączonej usługi, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="ac063-130">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac063-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac063-131">-ResourceGroupName</span></span>
<span data-ttu-id="ac063-132">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ac063-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ac063-133">To polecenie cmdlet powoduje utworzenie połączonej usługi dla grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="ac063-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac063-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac063-134">-ResourceId</span></span>
<span data-ttu-id="ac063-135">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ac063-135">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ac063-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac063-136">-WhatIf</span></span>
<span data-ttu-id="ac063-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac063-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ac063-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac063-138">-DefaultProfile</span></span>
<span data-ttu-id="ac063-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac063-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac063-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac063-140">CommonParameters</span></span>
<span data-ttu-id="ac063-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac063-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac063-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac063-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac063-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac063-143">INPUTS</span></span>

### <span data-ttu-id="ac063-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ac063-144">System.String</span></span>

## <span data-ttu-id="ac063-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac063-145">OUTPUTS</span></span>

### <span data-ttu-id="ac063-146">Microsoft. Azure. Commands. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="ac063-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="ac063-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac063-147">NOTES</span></span>
<span data-ttu-id="ac063-148">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="ac063-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ac063-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac063-149">RELATED LINKS</span></span>

[<span data-ttu-id="ac063-150">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ac063-150">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="ac063-151">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ac063-151">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
