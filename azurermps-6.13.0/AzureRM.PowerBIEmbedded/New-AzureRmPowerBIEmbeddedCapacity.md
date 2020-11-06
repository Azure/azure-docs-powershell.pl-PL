---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8546dbfbe8da12cd61c8b03d8aca64772d032b60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544952"
---
# <span data-ttu-id="8b923-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8b923-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8b923-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b923-102">SYNOPSIS</span></span>
<span data-ttu-id="8b923-103">Tworzy nową, zawbudowaną pojemność usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="8b923-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b923-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b923-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b923-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8b923-105">DESCRIPTION</span></span>
<span data-ttu-id="8b923-106">Polecenie cmdlet New-AzureRmPowerBIEmbeddedCapacity tworzy nową, zawbudowaną pojemność usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="8b923-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="8b923-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b923-107">EXAMPLES</span></span>

### <span data-ttu-id="8b923-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b923-108">Example 1</span></span>
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

<span data-ttu-id="8b923-109">Tworzy wydajność o nazwie testcapacity w regionie Azure Region Zachodni (Stanów Zjednoczonych) i w grupie zasób testRG.</span><span class="sxs-lookup"><span data-stu-id="8b923-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="8b923-110">Poziom wersji SKU dla wydajności to a1.</span><span class="sxs-lookup"><span data-stu-id="8b923-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="8b923-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b923-111">PARAMETERS</span></span>

### <span data-ttu-id="8b923-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="8b923-112">-Administrator</span></span>
<span data-ttu-id="8b923-113">Nazwy pojemności rozdzielone przecinkami, które są ustawiane jako administrator na stanowisku</span><span class="sxs-lookup"><span data-stu-id="8b923-113">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b923-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b923-114">-DefaultProfile</span></span>
<span data-ttu-id="8b923-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b923-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b923-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8b923-116">-Location</span></span>
<span data-ttu-id="8b923-117">Obszar platformy Azure, w którym jest hostowana pojemność osadzona w usłudze PowerBI</span><span class="sxs-lookup"><span data-stu-id="8b923-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="8b923-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8b923-118">-Name</span></span>
<span data-ttu-id="8b923-119">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="8b923-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="8b923-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b923-120">-ResourceGroupName</span></span>
<span data-ttu-id="8b923-121">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="8b923-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="8b923-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="8b923-122">-Sku</span></span>
<span data-ttu-id="8b923-123">Nazwa jednostki SKU dla pojemności.</span><span class="sxs-lookup"><span data-stu-id="8b923-123">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b923-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="8b923-124">-Tag</span></span>
<span data-ttu-id="8b923-125">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na pojemności.</span><span class="sxs-lookup"><span data-stu-id="8b923-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b923-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b923-126">-Confirm</span></span>
<span data-ttu-id="8b923-127">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="8b923-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="8b923-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b923-128">-WhatIf</span></span>
<span data-ttu-id="8b923-129">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="8b923-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="8b923-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b923-130">CommonParameters</span></span>
<span data-ttu-id="8b923-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b923-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b923-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b923-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b923-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b923-133">INPUTS</span></span>

### <span data-ttu-id="8b923-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8b923-134">System.String</span></span>

### <span data-ttu-id="8b923-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="8b923-135">System.String[]</span></span>

### <span data-ttu-id="8b923-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8b923-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8b923-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b923-137">OUTPUTS</span></span>

### <span data-ttu-id="8b923-138">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8b923-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8b923-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b923-139">NOTES</span></span>

## <span data-ttu-id="8b923-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b923-140">RELATED LINKS</span></span>

[<span data-ttu-id="8b923-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8b923-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="8b923-142">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8b923-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
