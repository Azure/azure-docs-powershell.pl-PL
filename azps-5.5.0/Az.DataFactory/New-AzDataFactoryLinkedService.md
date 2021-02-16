---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 09b766ec77b9f915a03bf6f5b20bd53941b66fc9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188603"
---
# <span data-ttu-id="29437-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="29437-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="29437-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29437-102">SYNOPSIS</span></span>
<span data-ttu-id="29437-103">Łączy magazyn danych lub usługę w chmurze z usługą Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="29437-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="29437-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="29437-104">SYNTAX</span></span>

### <span data-ttu-id="29437-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="29437-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29437-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="29437-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29437-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="29437-107">DESCRIPTION</span></span>
<span data-ttu-id="29437-108">Polecenie **cmdlet New-AzDataFactoryLinkedService** łączy magazyn danych lub usługę w chmurze z usługą Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="29437-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="29437-109">Jeśli określisz nazwę usługi połączonej, która już istnieje, to polecenie cmdlet wyświetli monit o potwierdzenie, zanim zastąpi usługę połączona.</span><span class="sxs-lookup"><span data-stu-id="29437-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="29437-110">Jeśli określisz parametr *Force,* polecenie cmdlet zastąpi istniejącą usługę połączona bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="29437-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="29437-111">Wykonaj te operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="29437-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="29437-112">Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="29437-112">Create a data factory.</span></span> 
- <span data-ttu-id="29437-113">Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="29437-113">Create linked services.</span></span> 
- <span data-ttu-id="29437-114">Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="29437-114">Create datasets.</span></span> 
- <span data-ttu-id="29437-115">Tworzenie potoku.</span><span class="sxs-lookup"><span data-stu-id="29437-115">Create a pipeline.</span></span>

## <span data-ttu-id="29437-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="29437-116">EXAMPLES</span></span>

### <span data-ttu-id="29437-117">Przykład 1. Tworzenie usługi połączonej</span><span class="sxs-lookup"><span data-stu-id="29437-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="29437-118">To polecenie tworzy usługę połączona o nazwie LinkedServiceCuratedWikiData w zakładzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="29437-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="29437-119">Ta połączona usługa łączy magazyn obiektów blob platformy Azure określony w pliku z fabryczną danymi o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="29437-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="29437-120">Polecenie przekazuje wynik do Format-List cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="29437-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="29437-121">Polecenie cmdlet programu Windows PowerShell formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="29437-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="29437-122">Aby uzyskać więcej informacji, wpisz `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="29437-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="29437-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29437-123">PARAMETERS</span></span>

### <span data-ttu-id="29437-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="29437-124">-DataFactory</span></span>
<span data-ttu-id="29437-125">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="29437-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="29437-126">To polecenie cmdlet tworzy usługę połączona dla fabrycznych danych określanych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="29437-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="29437-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="29437-127">-DataFactoryName</span></span>
<span data-ttu-id="29437-128">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="29437-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="29437-129">To polecenie cmdlet tworzy usługę połączona dla fabrycznych danych określanych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="29437-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="29437-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29437-130">-DefaultProfile</span></span>
<span data-ttu-id="29437-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="29437-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29437-132">— Plik</span><span class="sxs-lookup"><span data-stu-id="29437-132">-File</span></span>
<span data-ttu-id="29437-133">Określa pełną ścieżkę pliku JavaScript Object Notation (JSON) zawierającego opis usługi połączonej.</span><span class="sxs-lookup"><span data-stu-id="29437-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="29437-134">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="29437-134">-Force</span></span>
<span data-ttu-id="29437-135">Wskazuje, że to polecenie cmdlet zastępuje istniejącą usługę połączona bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="29437-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="29437-136">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="29437-136">-Name</span></span>
<span data-ttu-id="29437-137">Określa nazwę usługi połączonej do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="29437-137">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="29437-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29437-138">-ResourceGroupName</span></span>
<span data-ttu-id="29437-139">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="29437-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="29437-140">To polecenie cmdlet tworzy usługę połączona dla grupy, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="29437-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="29437-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29437-141">-Confirm</span></span>
<span data-ttu-id="29437-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="29437-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29437-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29437-143">-WhatIf</span></span>
<span data-ttu-id="29437-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29437-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29437-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="29437-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29437-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29437-146">CommonParameters</span></span>
<span data-ttu-id="29437-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29437-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29437-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29437-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29437-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29437-149">INPUTS</span></span>

### <span data-ttu-id="29437-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="29437-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="29437-151">System.String</span><span class="sxs-lookup"><span data-stu-id="29437-151">System.String</span></span>

## <span data-ttu-id="29437-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29437-152">OUTPUTS</span></span>

### <span data-ttu-id="29437-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="29437-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="29437-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="29437-154">NOTES</span></span>
* <span data-ttu-id="29437-155">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="29437-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="29437-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29437-156">RELATED LINKS</span></span>

[<span data-ttu-id="29437-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="29437-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="29437-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="29437-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


