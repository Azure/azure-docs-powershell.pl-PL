---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: 450a833656f6508f70ebd97f5387075c1711c5f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194842"
---
# <span data-ttu-id="c89cb-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="c89cb-101">New-AzDataFactory</span></span>

## <span data-ttu-id="c89cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c89cb-102">SYNOPSIS</span></span>
<span data-ttu-id="c89cb-103">Tworzy fabryczne dane.</span><span class="sxs-lookup"><span data-stu-id="c89cb-103">Creates a data factory.</span></span>

## <span data-ttu-id="c89cb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c89cb-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c89cb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c89cb-105">DESCRIPTION</span></span>
<span data-ttu-id="c89cb-106">Polecenie **cmdlet New-AzDataFactory** tworzy grupę danych z określoną nazwą i lokalizacją grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c89cb-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="c89cb-107">Wykonaj te operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="c89cb-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="c89cb-108">Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="c89cb-108">Create a data factory.</span></span> 
- <span data-ttu-id="c89cb-109">Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="c89cb-109">Create linked services.</span></span> 
- <span data-ttu-id="c89cb-110">Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="c89cb-110">Create datasets.</span></span> 
- <span data-ttu-id="c89cb-111">Tworzenie potoku.</span><span class="sxs-lookup"><span data-stu-id="c89cb-111">Create a pipeline.</span></span>

## <span data-ttu-id="c89cb-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c89cb-112">EXAMPLES</span></span>

### <span data-ttu-id="c89cb-113">Przykład 1. Tworzenie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="c89cb-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="c89cb-114">To polecenie umożliwia utworzenie w grupie zasobów O nazwie ADF w lokalizacji WestUS fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c89cb-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="c89cb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c89cb-115">PARAMETERS</span></span>

### <span data-ttu-id="c89cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c89cb-116">-DefaultProfile</span></span>
<span data-ttu-id="c89cb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c89cb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c89cb-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c89cb-118">-Force</span></span>
<span data-ttu-id="c89cb-119">Wskazuje, że to polecenie cmdlet zastępuje istniejącą fabryczną dane bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c89cb-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c89cb-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c89cb-120">-Location</span></span>
<span data-ttu-id="c89cb-121">Określa lokalizację dla fabryki danych, na przykład WestUS lub EastUS.</span><span class="sxs-lookup"><span data-stu-id="c89cb-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="c89cb-122">Obecnie obsługiwany jest tylko program WestUS.</span><span class="sxs-lookup"><span data-stu-id="c89cb-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="c89cb-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c89cb-123">-Name</span></span>
<span data-ttu-id="c89cb-124">Określa nazwę fabrycznej transmisji danych, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="c89cb-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="c89cb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c89cb-125">-ResourceGroupName</span></span>
<span data-ttu-id="c89cb-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c89cb-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c89cb-127">To polecenie cmdlet tworzy grupę należącą do grupy, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c89cb-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c89cb-128">— Tag</span><span class="sxs-lookup"><span data-stu-id="c89cb-128">-Tag</span></span>
<span data-ttu-id="c89cb-129">Tagi fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="c89cb-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="c89cb-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c89cb-130">-Confirm</span></span>
<span data-ttu-id="c89cb-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c89cb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c89cb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c89cb-132">-WhatIf</span></span>
<span data-ttu-id="c89cb-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c89cb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c89cb-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c89cb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c89cb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c89cb-135">CommonParameters</span></span>
<span data-ttu-id="c89cb-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c89cb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c89cb-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c89cb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c89cb-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c89cb-138">INPUTS</span></span>

### <span data-ttu-id="c89cb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c89cb-139">System.String</span></span>

### <span data-ttu-id="c89cb-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c89cb-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c89cb-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c89cb-141">OUTPUTS</span></span>

### <span data-ttu-id="c89cb-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c89cb-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="c89cb-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c89cb-143">NOTES</span></span>
* <span data-ttu-id="c89cb-144">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="c89cb-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c89cb-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c89cb-145">RELATED LINKS</span></span>

[<span data-ttu-id="c89cb-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="c89cb-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="c89cb-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="c89cb-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


