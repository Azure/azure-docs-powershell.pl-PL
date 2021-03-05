---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: c13fdf46dff4ba0b62a8009bad7c4790507b2561
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975009"
---
# <span data-ttu-id="3a151-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="3a151-101">New-AzDataFactory</span></span>

## <span data-ttu-id="3a151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a151-102">SYNOPSIS</span></span>
<span data-ttu-id="3a151-103">Tworzy fabryczne dane.</span><span class="sxs-lookup"><span data-stu-id="3a151-103">Creates a data factory.</span></span>

## <span data-ttu-id="3a151-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3a151-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a151-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3a151-105">DESCRIPTION</span></span>
<span data-ttu-id="3a151-106">Polecenie **cmdlet New-AzDataFactory** tworzy grupę danych o nazwie i lokalizacji określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a151-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="3a151-107">Wykonaj te operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="3a151-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="3a151-108">Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="3a151-108">Create a data factory.</span></span> 
- <span data-ttu-id="3a151-109">Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="3a151-109">Create linked services.</span></span> 
- <span data-ttu-id="3a151-110">Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="3a151-110">Create datasets.</span></span> 
- <span data-ttu-id="3a151-111">Tworzenie potoku.</span><span class="sxs-lookup"><span data-stu-id="3a151-111">Create a pipeline.</span></span>

## <span data-ttu-id="3a151-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3a151-112">EXAMPLES</span></span>

### <span data-ttu-id="3a151-113">Przykład 1. Tworzenie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="3a151-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="3a151-114">To polecenie umożliwia utworzenie w grupie zasobów O nazwie ADF w lokalizacji WestUS fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3a151-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="3a151-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a151-115">PARAMETERS</span></span>

### <span data-ttu-id="3a151-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a151-116">-DefaultProfile</span></span>
<span data-ttu-id="3a151-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3a151-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a151-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3a151-118">-Force</span></span>
<span data-ttu-id="3a151-119">Wskazuje, że to polecenie cmdlet zastępuje istniejącą fabryczną dane bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3a151-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3a151-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3a151-120">-Location</span></span>
<span data-ttu-id="3a151-121">Określa lokalizację dla fabryki danych, na przykład ZachódUS lub EastUS.</span><span class="sxs-lookup"><span data-stu-id="3a151-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="3a151-122">Obecnie obsługiwany jest tylko program WestUS.</span><span class="sxs-lookup"><span data-stu-id="3a151-122">Only WestUS is currently supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a151-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3a151-123">-Name</span></span>
<span data-ttu-id="3a151-124">Określa nazwę fabrycznej transmisji danych, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="3a151-124">Specifies the name of the data factory to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a151-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a151-125">-ResourceGroupName</span></span>
<span data-ttu-id="3a151-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3a151-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3a151-127">To polecenie cmdlet tworzy grupę danych należącą do grupy, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3a151-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a151-128">— Tag</span><span class="sxs-lookup"><span data-stu-id="3a151-128">-Tag</span></span>
<span data-ttu-id="3a151-129">Tagi fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="3a151-129">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a151-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a151-130">-Confirm</span></span>
<span data-ttu-id="3a151-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3a151-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a151-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a151-132">-WhatIf</span></span>
<span data-ttu-id="3a151-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a151-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a151-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3a151-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a151-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a151-135">CommonParameters</span></span>
<span data-ttu-id="3a151-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a151-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a151-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a151-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a151-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a151-138">INPUTS</span></span>

### <span data-ttu-id="3a151-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3a151-139">System.String</span></span>

### <span data-ttu-id="3a151-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3a151-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3a151-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a151-141">OUTPUTS</span></span>

### <span data-ttu-id="3a151-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3a151-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="3a151-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3a151-143">NOTES</span></span>
* <span data-ttu-id="3a151-144">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="3a151-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3a151-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a151-145">RELATED LINKS</span></span>

[<span data-ttu-id="3a151-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="3a151-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="3a151-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="3a151-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


