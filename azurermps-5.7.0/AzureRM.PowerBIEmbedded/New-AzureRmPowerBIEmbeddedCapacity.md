---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6badeec8b2425a5ca8e10dc88039a1d28e055cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527957"
---
# <span data-ttu-id="3d6cc-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3d6cc-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3d6cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d6cc-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6cc-103">Tworzy nową, zawbudowaną pojemność usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="3d6cc-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d6cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d6cc-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity 
    [-ResourceGroupName] <String> 
    [-Name] <String> 
    [-Location] <String>
    [-Sku] <String> 
    [-Administrator] <String>
    [[-Tag] <Hashtable>] 
    [-WhatIf] 
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="3d6cc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3d6cc-105">DESCRIPTION</span></span>
<span data-ttu-id="3d6cc-106">Polecenie cmdlet New-AzureRmPowerBIEmbeddedCapacity tworzy nową, zawbudowaną pojemność usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="3d6cc-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="3d6cc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d6cc-107">EXAMPLES</span></span>

### <span data-ttu-id="3d6cc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3d6cc-108">Example 1</span></span>
```
PS C:\> New-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="3d6cc-109">Tworzy wydajność o nazwie testcapacity w regionie Azure Region Zachodni (Stanów Zjednoczonych) i w grupie zasób testRG.</span><span class="sxs-lookup"><span data-stu-id="3d6cc-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="3d6cc-110">Poziom wersji SKU dla wydajności to a1.</span><span class="sxs-lookup"><span data-stu-id="3d6cc-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="3d6cc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d6cc-111">PARAMETERS</span></span>

### <span data-ttu-id="3d6cc-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d6cc-112">-ResourceGroupName</span></span>
<span data-ttu-id="3d6cc-113">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="3d6cc-113">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cc-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d6cc-114">-Name</span></span>
<span data-ttu-id="3d6cc-115">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="3d6cc-115">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cc-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3d6cc-116">-Location</span></span>
<span data-ttu-id="3d6cc-117">Obszar platformy Azure, w którym jest hostowana pojemność osadzona w usłudze PowerBI</span><span class="sxs-lookup"><span data-stu-id="3d6cc-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cc-118">-SKU</span><span class="sxs-lookup"><span data-stu-id="3d6cc-118">-Sku</span></span>
<span data-ttu-id="3d6cc-119">Nazwa jednostki SKU dla pojemności.</span><span class="sxs-lookup"><span data-stu-id="3d6cc-119">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cc-120">-Administrator</span><span class="sxs-lookup"><span data-stu-id="3d6cc-120">-Administrator</span></span>
<span data-ttu-id="3d6cc-121">Nazwy pojemności rozdzielone przecinkami, które są ustawiane jako administrator na stanowisku</span><span class="sxs-lookup"><span data-stu-id="3d6cc-121">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cc-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="3d6cc-122">-Tag</span></span>
<span data-ttu-id="3d6cc-123">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na pojemności.</span><span class="sxs-lookup"><span data-stu-id="3d6cc-123">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cc-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d6cc-124">-Confirm</span></span>
<span data-ttu-id="3d6cc-125">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="3d6cc-125">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="3d6cc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d6cc-126">-WhatIf</span></span>
<span data-ttu-id="3d6cc-127">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="3d6cc-127">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="3d6cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6cc-128">CommonParameters</span></span>
<span data-ttu-id="3d6cc-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d6cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6cc-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d6cc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6cc-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d6cc-131">INPUTS</span></span>

### <span data-ttu-id="3d6cc-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3d6cc-132">None</span></span>
<span data-ttu-id="3d6cc-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3d6cc-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d6cc-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d6cc-134">OUTPUTS</span></span>

### <span data-ttu-id="3d6cc-135">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3d6cc-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3d6cc-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d6cc-136">NOTES</span></span>

## <span data-ttu-id="3d6cc-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d6cc-137">RELATED LINKS</span></span>

[<span data-ttu-id="3d6cc-138">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3d6cc-138">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="3d6cc-139">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3d6cc-139">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
