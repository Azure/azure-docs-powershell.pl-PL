---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
ms.openlocfilehash: 8adaa00b08615bb687cbd481584875e9c91e7da3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546824"
---
# <span data-ttu-id="3a700-101">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="3a700-101">New-AzureRmDataFactory</span></span>

## <span data-ttu-id="3a700-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a700-102">SYNOPSIS</span></span>
<span data-ttu-id="3a700-103">Tworzy fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="3a700-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a700-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a700-104">SYNTAX</span></span>

```
New-AzureRmDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a700-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a700-105">DESCRIPTION</span></span>
<span data-ttu-id="3a700-106">Polecenie cmdlet **New-AzureRmDataFactory** tworzy fabrykę danych z określoną nazwą i lokalizacją grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a700-106">The **New-AzureRmDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="3a700-107">Wykonuj następujące operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="3a700-107">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="3a700-108">Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="3a700-108">Create a data factory.</span></span> 
- <span data-ttu-id="3a700-109">Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="3a700-109">Create linked services.</span></span> 
- <span data-ttu-id="3a700-110">Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="3a700-110">Create datasets.</span></span> 
- <span data-ttu-id="3a700-111">Utwórz rurociąg.</span><span class="sxs-lookup"><span data-stu-id="3a700-111">Create a pipeline.</span></span>

## <span data-ttu-id="3a700-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a700-112">EXAMPLES</span></span>

### <span data-ttu-id="3a700-113">Przykład 1. Tworzenie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="3a700-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="3a700-114">To polecenie tworzy fabrykę danych o nazwie WikiADF w grupie zasobów o nazwie ADF w lokalizacji na zachód.</span><span class="sxs-lookup"><span data-stu-id="3a700-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="3a700-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a700-115">PARAMETERS</span></span>

### <span data-ttu-id="3a700-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a700-116">-DefaultProfile</span></span>
<span data-ttu-id="3a700-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3a700-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a700-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3a700-118">-Force</span></span>
<span data-ttu-id="3a700-119">Wskazuje, że to polecenie cmdlet zamienia istniejącą fabrykę danych bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3a700-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3a700-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3a700-120">-Location</span></span>
<span data-ttu-id="3a700-121">Określa lokalizację fabryki danych, na przykład zachód lub wschód.</span><span class="sxs-lookup"><span data-stu-id="3a700-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="3a700-122">Obecnie jest obsługiwany tylko zachód.</span><span class="sxs-lookup"><span data-stu-id="3a700-122">Only WestUS is currently supported.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a700-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a700-123">-Name</span></span>
<span data-ttu-id="3a700-124">Określa nazwę fabryki danych, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="3a700-124">Specifies the name of the data factory to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a700-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a700-125">-ResourceGroupName</span></span>
<span data-ttu-id="3a700-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3a700-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3a700-127">To polecenie cmdlet umożliwia utworzenie fabryki danych należącej do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="3a700-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a700-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="3a700-128">-Tag</span></span>
<span data-ttu-id="3a700-129">Znaczniki fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="3a700-129">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a700-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a700-130">-Confirm</span></span>
<span data-ttu-id="3a700-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a700-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a700-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a700-132">-WhatIf</span></span>
<span data-ttu-id="3a700-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a700-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a700-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a700-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a700-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a700-135">CommonParameters</span></span>
<span data-ttu-id="3a700-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a700-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a700-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a700-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a700-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a700-138">INPUTS</span></span>

### <span data-ttu-id="3a700-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3a700-139">None</span></span>
<span data-ttu-id="3a700-140">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3a700-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a700-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a700-141">OUTPUTS</span></span>

### <span data-ttu-id="3a700-142">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3a700-142">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="3a700-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a700-143">NOTES</span></span>
* <span data-ttu-id="3a700-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="3a700-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3a700-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a700-145">RELATED LINKS</span></span>

[<span data-ttu-id="3a700-146">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="3a700-146">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="3a700-147">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="3a700-147">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


