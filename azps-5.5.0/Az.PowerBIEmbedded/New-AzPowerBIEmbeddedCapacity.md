---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3b0f64101972e7803961a08565af33ee08b34696
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202155"
---
# <span data-ttu-id="4e135-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4e135-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4e135-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e135-102">SYNOPSIS</span></span>
<span data-ttu-id="4e135-103">Tworzy nową pojemność osadzoną w u programie PowerBI.</span><span class="sxs-lookup"><span data-stu-id="4e135-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="4e135-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4e135-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e135-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4e135-105">DESCRIPTION</span></span>
<span data-ttu-id="4e135-106">Polecenie New-AzPowerBIEmbeddedCapacity cmdlet tworzy nową osadzoną pojemność usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="4e135-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4e135-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4e135-107">EXAMPLES</span></span>

### <span data-ttu-id="4e135-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4e135-108">Example 1</span></span>
```
PS C:\> New-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
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

<span data-ttu-id="4e135-109">Tworzy wydajność o nazwie testcapacity w regionie Azure West Central US i w testRG grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4e135-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="4e135-110">Poziom SKU dla wydajności będzie mieć 1.</span><span class="sxs-lookup"><span data-stu-id="4e135-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="4e135-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e135-111">PARAMETERS</span></span>

### <span data-ttu-id="4e135-112">— Administrator</span><span class="sxs-lookup"><span data-stu-id="4e135-112">-Administrator</span></span>
<span data-ttu-id="4e135-113">Nazwy rozdzielone przecinkami, które należy ustawić jako administrator w zakresie pojemności</span><span class="sxs-lookup"><span data-stu-id="4e135-113">A comma separated names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="4e135-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e135-114">-DefaultProfile</span></span>
<span data-ttu-id="4e135-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e135-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e135-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4e135-116">-Location</span></span>
<span data-ttu-id="4e135-117">Region platformy Azure, w którym jest hostowana osadzona pojemność usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="4e135-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="4e135-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4e135-118">-Name</span></span>
<span data-ttu-id="4e135-119">Nazwa osadzonej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="4e135-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="4e135-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e135-120">-ResourceGroupName</span></span>
<span data-ttu-id="4e135-121">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="4e135-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="4e135-122">- SKU</span><span class="sxs-lookup"><span data-stu-id="4e135-122">-Sku</span></span>
<span data-ttu-id="4e135-123">Nazwa sku dla pojemności.</span><span class="sxs-lookup"><span data-stu-id="4e135-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="4e135-124">— Tag</span><span class="sxs-lookup"><span data-stu-id="4e135-124">-Tag</span></span>
<span data-ttu-id="4e135-125">Pary klucz-wartość w postaci tabeli skrótów ustawionej jako tagi dotyczące pojemności.</span><span class="sxs-lookup"><span data-stu-id="4e135-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="4e135-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4e135-126">-Confirm</span></span>
<span data-ttu-id="4e135-127">Monituje użytkownika o potwierdzenie, czy wykonać operację</span><span class="sxs-lookup"><span data-stu-id="4e135-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4e135-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e135-128">-WhatIf</span></span>
<span data-ttu-id="4e135-129">W tym artykule opisano akcje, które bieżąca operacja zostanie wykonać bez ich wykonania.</span><span class="sxs-lookup"><span data-stu-id="4e135-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4e135-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e135-130">CommonParameters</span></span>
<span data-ttu-id="4e135-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e135-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e135-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e135-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e135-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e135-133">INPUTS</span></span>

### <span data-ttu-id="4e135-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4e135-134">System.String</span></span>

### <span data-ttu-id="4e135-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4e135-135">System.String[]</span></span>

### <span data-ttu-id="4e135-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4e135-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4e135-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e135-137">OUTPUTS</span></span>

### <span data-ttu-id="4e135-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4e135-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4e135-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4e135-139">NOTES</span></span>

## <span data-ttu-id="4e135-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e135-140">RELATED LINKS</span></span>

[<span data-ttu-id="4e135-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4e135-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4e135-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4e135-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
