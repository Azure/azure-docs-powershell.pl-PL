---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: 450a833656f6508f70ebd97f5387075c1711c5f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306193"
---
# <span data-ttu-id="0b918-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="0b918-101">New-AzDataFactory</span></span>

## <span data-ttu-id="0b918-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b918-102">SYNOPSIS</span></span>
<span data-ttu-id="0b918-103">Tworzy fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="0b918-103">Creates a data factory.</span></span>

## <span data-ttu-id="0b918-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b918-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b918-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0b918-105">DESCRIPTION</span></span>
<span data-ttu-id="0b918-106">Polecenie cmdlet **New-AzDataFactory** tworzy fabrykę danych z określoną nazwą i lokalizacją grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0b918-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="0b918-107">Wykonuj następujące operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="0b918-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="0b918-108">Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0b918-108">Create a data factory.</span></span> 
- <span data-ttu-id="0b918-109">Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="0b918-109">Create linked services.</span></span> 
- <span data-ttu-id="0b918-110">Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="0b918-110">Create datasets.</span></span> 
- <span data-ttu-id="0b918-111">Utwórz rurociąg.</span><span class="sxs-lookup"><span data-stu-id="0b918-111">Create a pipeline.</span></span>

## <span data-ttu-id="0b918-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b918-112">EXAMPLES</span></span>

### <span data-ttu-id="0b918-113">Przykład 1. Tworzenie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="0b918-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="0b918-114">To polecenie tworzy fabrykę danych o nazwie WikiADF w grupie zasobów o nazwie ADF w lokalizacji na zachód.</span><span class="sxs-lookup"><span data-stu-id="0b918-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="0b918-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b918-115">PARAMETERS</span></span>

### <span data-ttu-id="0b918-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b918-116">-DefaultProfile</span></span>
<span data-ttu-id="0b918-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0b918-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b918-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0b918-118">-Force</span></span>
<span data-ttu-id="0b918-119">Wskazuje, że to polecenie cmdlet zamienia istniejącą fabrykę danych bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0b918-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="0b918-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0b918-120">-Location</span></span>
<span data-ttu-id="0b918-121">Określa lokalizację fabryki danych, na przykład zachód lub wschód.</span><span class="sxs-lookup"><span data-stu-id="0b918-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="0b918-122">Obecnie jest obsługiwany tylko zachód.</span><span class="sxs-lookup"><span data-stu-id="0b918-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="0b918-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0b918-123">-Name</span></span>
<span data-ttu-id="0b918-124">Określa nazwę fabryki danych, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="0b918-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="0b918-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b918-125">-ResourceGroupName</span></span>
<span data-ttu-id="0b918-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0b918-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0b918-127">To polecenie cmdlet umożliwia utworzenie fabryki danych należącej do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="0b918-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0b918-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b918-128">-Tag</span></span>
<span data-ttu-id="0b918-129">Znaczniki fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0b918-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="0b918-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b918-130">-Confirm</span></span>
<span data-ttu-id="0b918-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b918-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b918-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b918-132">-WhatIf</span></span>
<span data-ttu-id="0b918-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b918-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b918-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0b918-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b918-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b918-135">CommonParameters</span></span>
<span data-ttu-id="0b918-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b918-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b918-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b918-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b918-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b918-138">INPUTS</span></span>

### <span data-ttu-id="0b918-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0b918-139">System.String</span></span>

### <span data-ttu-id="0b918-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b918-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b918-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b918-141">OUTPUTS</span></span>

### <span data-ttu-id="0b918-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0b918-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="0b918-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b918-143">NOTES</span></span>
* <span data-ttu-id="0b918-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="0b918-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0b918-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b918-145">RELATED LINKS</span></span>

[<span data-ttu-id="0b918-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="0b918-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="0b918-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="0b918-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


