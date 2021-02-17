---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: d6fd12e96a98d0771a984aa5234013dbe4a548af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198162"
---
# <span data-ttu-id="1b297-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="1b297-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="1b297-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b297-102">SYNOPSIS</span></span>
<span data-ttu-id="1b297-103">Łączy magazyn danych lub usługę w chmurze z usługą Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1b297-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="1b297-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1b297-104">SYNTAX</span></span>

### <span data-ttu-id="1b297-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="1b297-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b297-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b297-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b297-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1b297-107">DESCRIPTION</span></span>
<span data-ttu-id="1b297-108">Polecenie Set-AzDataFactoryV2LinkedService łączy magazyn danych lub usługę w chmurze z usługą Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1b297-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="1b297-109">Jeśli określisz nazwę usługi połączonej, która już istnieje, to polecenie cmdlet wyświetli monit o potwierdzenie, zanim zastąpi usługę połączona.</span><span class="sxs-lookup"><span data-stu-id="1b297-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="1b297-110">Jeśli określisz parametr Force, polecenie cmdlet zastąpi istniejącą usługę połączona bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="1b297-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="1b297-111">Wykonaj następujące operacje w następującej kolejności: — Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1b297-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="1b297-112">— Tworzenie usług połączonych.</span><span class="sxs-lookup"><span data-stu-id="1b297-112">-- Create linked services.</span></span>
<span data-ttu-id="1b297-113">— Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="1b297-113">-- Create datasets.</span></span>
<span data-ttu-id="1b297-114">— Tworzenie potoku.</span><span class="sxs-lookup"><span data-stu-id="1b297-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="1b297-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1b297-115">EXAMPLES</span></span>

### <span data-ttu-id="1b297-116">Przykład 1. Tworzenie usługi połączonej</span><span class="sxs-lookup"><span data-stu-id="1b297-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="1b297-117">To polecenie tworzy usługę połączona o nazwie LinkedServiceCuratedWikiData w fabrycznej bazie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1b297-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="1b297-118">Ta połączona usługa łączy magazyn obiektów blob platformy Azure określony w pliku z fabryczną danymi o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1b297-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="1b297-119">Polecenie przekazuje wynik do polecenia cmdlet Format-List za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="1b297-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1b297-120">Polecenie cmdlet programu Windows PowerShell formatuje wyniki.</span><span class="sxs-lookup"><span data-stu-id="1b297-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="1b297-121">Aby uzyskać więcej informacji, wpisz Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="1b297-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="1b297-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b297-122">PARAMETERS</span></span>

### <span data-ttu-id="1b297-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1b297-123">-DataFactoryName</span></span>
<span data-ttu-id="1b297-124">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1b297-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1b297-125">To polecenie cmdlet tworzy usługę połączona dla fabrycznych danych określanych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1b297-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b297-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b297-126">-DefaultProfile</span></span>
<span data-ttu-id="1b297-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b297-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b297-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="1b297-128">-DefinitionFile</span></span>
<span data-ttu-id="1b297-129">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="1b297-129">The JSON file path.</span></span>

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

### <span data-ttu-id="1b297-130">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1b297-130">-Force</span></span>
<span data-ttu-id="1b297-131">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1b297-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1b297-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1b297-132">-Name</span></span>
<span data-ttu-id="1b297-133">Określa nazwę usługi połączonej do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="1b297-133">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="1b297-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b297-134">-ResourceGroupName</span></span>
<span data-ttu-id="1b297-135">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1b297-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1b297-136">To polecenie cmdlet tworzy usługę połączona dla grupy, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1b297-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b297-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b297-137">-ResourceId</span></span>
<span data-ttu-id="1b297-138">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="1b297-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1b297-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b297-139">-Confirm</span></span>
<span data-ttu-id="1b297-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1b297-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b297-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b297-141">-WhatIf</span></span>
<span data-ttu-id="1b297-142">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b297-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1b297-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b297-143">CommonParameters</span></span>
<span data-ttu-id="1b297-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b297-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b297-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b297-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b297-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b297-146">INPUTS</span></span>

### <span data-ttu-id="1b297-147">System.String</span><span class="sxs-lookup"><span data-stu-id="1b297-147">System.String</span></span>

## <span data-ttu-id="1b297-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b297-148">OUTPUTS</span></span>

### <span data-ttu-id="1b297-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="1b297-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="1b297-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1b297-150">NOTES</span></span>
<span data-ttu-id="1b297-151">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="1b297-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1b297-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b297-152">RELATED LINKS</span></span>

[<span data-ttu-id="1b297-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="1b297-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="1b297-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="1b297-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
