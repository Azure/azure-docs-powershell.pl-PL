---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: cd67307c13e5704da67659ba67f6f609eeff4df8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552135"
---
# <span data-ttu-id="a6e5e-101">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="a6e5e-101">New-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="a6e5e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="a6e5e-103">Łączy magazyn danych lub usługę w chmurze z fabryką danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6e5e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6e5e-104">SYNTAX</span></span>

### <span data-ttu-id="a6e5e-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a6e5e-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6e5e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a6e5e-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6e5e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a6e5e-107">DESCRIPTION</span></span>
<span data-ttu-id="a6e5e-108">Polecenie cmdlet **New-AzureRmDataFactoryLinkedService** łączy magazyn danych lub usługę w chmurze z usługą Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-108">The **New-AzureRmDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="a6e5e-109">Jeśli określisz nazwę połączonej usługi, która już istnieje, to polecenie cmdlet monituje o potwierdzenie przed zastąpieniem połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="a6e5e-110">Jeśli określisz parametr *Force* , polecenie cmdlet zastępuje istniejącą połączoną usługę bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="a6e5e-111">Wykonuj następujące operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="a6e5e-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="a6e5e-112">Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-112">Create a data factory.</span></span> 
- <span data-ttu-id="a6e5e-113">Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-113">Create linked services.</span></span> 
- <span data-ttu-id="a6e5e-114">Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-114">Create datasets.</span></span> 
- <span data-ttu-id="a6e5e-115">Utwórz rurociąg.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-115">Create a pipeline.</span></span>

## <span data-ttu-id="a6e5e-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6e5e-116">EXAMPLES</span></span>

### <span data-ttu-id="a6e5e-117">Przykład 1. Tworzenie połączonej usługi</span><span class="sxs-lookup"><span data-stu-id="a6e5e-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="a6e5e-118">To polecenie tworzy połączoną usługę o nazwie LinkedServiceCuratedWikiData w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="a6e5e-119">Ta połączona usługa łączy magazyn obiektów blob platformy Azure określony w pliku z fabryką danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="a6e5e-120">Polecenie przekazuje wynik do polecenia cmdlet Format-List przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a6e5e-121">To polecenie cmdlet programu Windows PowerShell formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="a6e5e-122">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="a6e5e-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="a6e5e-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6e5e-123">PARAMETERS</span></span>

### <span data-ttu-id="a6e5e-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e5e-124">-DataFactory</span></span>
<span data-ttu-id="a6e5e-125">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="a6e5e-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a6e5e-126">To polecenie cmdlet tworzy połączoną usługę dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6e5e-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a6e5e-127">-DataFactoryName</span></span>
<span data-ttu-id="a6e5e-128">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a6e5e-129">To polecenie cmdlet tworzy połączoną usługę dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6e5e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6e5e-130">-DefaultProfile</span></span>
<span data-ttu-id="a6e5e-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a6e5e-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6e5e-132">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="a6e5e-132">-File</span></span>
<span data-ttu-id="a6e5e-133">Określa pełną ścieżkę do pliku notacji JavaScript (kod JSON) zawierającego opis połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="a6e5e-134">-Force</span><span class="sxs-lookup"><span data-stu-id="a6e5e-134">-Force</span></span>
<span data-ttu-id="a6e5e-135">Wskazuje, że to polecenie cmdlet zamieni istniejącą usługę połączoną bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a6e5e-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a6e5e-136">-Name</span></span>
<span data-ttu-id="a6e5e-137">Określa nazwę połączonej usługi, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-137">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="a6e5e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6e5e-138">-ResourceGroupName</span></span>
<span data-ttu-id="a6e5e-139">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a6e5e-140">To polecenie cmdlet powoduje utworzenie połączonej usługi dla grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6e5e-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6e5e-141">-Confirm</span></span>
<span data-ttu-id="a6e5e-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6e5e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6e5e-143">-WhatIf</span></span>
<span data-ttu-id="a6e5e-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6e5e-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6e5e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6e5e-146">CommonParameters</span></span>
<span data-ttu-id="a6e5e-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6e5e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6e5e-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6e5e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6e5e-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6e5e-149">INPUTS</span></span>

### <span data-ttu-id="a6e5e-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e5e-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a6e5e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a6e5e-151">System.String</span></span>

## <span data-ttu-id="a6e5e-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6e5e-152">OUTPUTS</span></span>

### <span data-ttu-id="a6e5e-153">Microsoft. Azure. Commands. datafactors. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="a6e5e-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="a6e5e-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6e5e-154">NOTES</span></span>
* <span data-ttu-id="a6e5e-155">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="a6e5e-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a6e5e-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6e5e-156">RELATED LINKS</span></span>

[<span data-ttu-id="a6e5e-157">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="a6e5e-157">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="a6e5e-158">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="a6e5e-158">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)


