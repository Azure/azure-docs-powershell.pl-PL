---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
ms.openlocfilehash: 13e9a8de97ee19e53c31a76516fef7c9fcfcaedd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525542"
---
# <span data-ttu-id="3b3af-101">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="3b3af-101">New-AzureRmDataFactory</span></span>

## <span data-ttu-id="3b3af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b3af-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3af-103">Tworzy fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="3b3af-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b3af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b3af-104">SYNTAX</span></span>

```
New-AzureRmDataFactory [-Name] <String> [-Location] <String> [[-Tags] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b3af-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3b3af-105">DESCRIPTION</span></span>
<span data-ttu-id="3b3af-106">Polecenie cmdlet **New-AzureRmDataFactory** tworzy fabrykę danych z określoną nazwą i lokalizacją grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b3af-106">The **New-AzureRmDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="3b3af-107">Wykonuj następujące operacje w następującej kolejności:</span><span class="sxs-lookup"><span data-stu-id="3b3af-107">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="3b3af-108">Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="3b3af-108">Create a data factory.</span></span> 
- <span data-ttu-id="3b3af-109">Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="3b3af-109">Create linked services.</span></span> 
- <span data-ttu-id="3b3af-110">Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="3b3af-110">Create datasets.</span></span> 
- <span data-ttu-id="3b3af-111">Utwórz rurociąg.</span><span class="sxs-lookup"><span data-stu-id="3b3af-111">Create a pipeline.</span></span>

## <span data-ttu-id="3b3af-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b3af-112">EXAMPLES</span></span>

### <span data-ttu-id="3b3af-113">Przykład 1. Tworzenie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="3b3af-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="3b3af-114">To polecenie tworzy fabrykę danych o nazwie WikiADF w grupie zasobów o nazwie ADF w lokalizacji na zachód.</span><span class="sxs-lookup"><span data-stu-id="3b3af-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="3b3af-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b3af-115">PARAMETERS</span></span>

### <span data-ttu-id="3b3af-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3b3af-116">-Force</span></span>
<span data-ttu-id="3b3af-117">Wskazuje, że to polecenie cmdlet zamienia istniejącą fabrykę danych bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3b3af-117">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3b3af-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3b3af-118">-Location</span></span>
<span data-ttu-id="3b3af-119">Określa lokalizację fabryki danych, na przykład zachód lub wschód.</span><span class="sxs-lookup"><span data-stu-id="3b3af-119">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="3b3af-120">Obecnie jest obsługiwany tylko zachód.</span><span class="sxs-lookup"><span data-stu-id="3b3af-120">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="3b3af-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b3af-121">-Name</span></span>
<span data-ttu-id="3b3af-122">Określa nazwę fabryki danych, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="3b3af-122">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="3b3af-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b3af-123">-ResourceGroupName</span></span>
<span data-ttu-id="3b3af-124">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3b3af-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3b3af-125">To polecenie cmdlet umożliwia utworzenie fabryki danych należącej do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="3b3af-125">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3b3af-126">-Tagi</span><span class="sxs-lookup"><span data-stu-id="3b3af-126">-Tags</span></span>
<span data-ttu-id="3b3af-127">Określa Tagi dla fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="3b3af-127">Specifies tags for the data factory.</span></span>

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

### <span data-ttu-id="3b3af-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b3af-128">-Confirm</span></span>
<span data-ttu-id="3b3af-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b3af-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b3af-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b3af-130">-WhatIf</span></span>
<span data-ttu-id="3b3af-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b3af-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b3af-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3b3af-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b3af-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3af-133">-DefaultProfile</span></span>
<span data-ttu-id="3b3af-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b3af-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b3af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3af-135">CommonParameters</span></span>
<span data-ttu-id="3b3af-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3af-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3af-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3af-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b3af-138">INPUTS</span></span>

## <span data-ttu-id="3b3af-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b3af-139">OUTPUTS</span></span>

### <span data-ttu-id="3b3af-140">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3b3af-140">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="3b3af-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b3af-141">NOTES</span></span>
* <span data-ttu-id="3b3af-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="3b3af-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3b3af-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b3af-143">RELATED LINKS</span></span>

[<span data-ttu-id="3b3af-144">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="3b3af-144">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="3b3af-145">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="3b3af-145">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


