---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3b0f64101972e7803961a08565af33ee08b34696
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355765"
---
# <span data-ttu-id="89688-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="89688-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="89688-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89688-102">SYNOPSIS</span></span>
<span data-ttu-id="89688-103">Tworzy nową, zawbudowaną pojemność usługi PowerBI.</span><span class="sxs-lookup"><span data-stu-id="89688-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="89688-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89688-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89688-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89688-105">DESCRIPTION</span></span>
<span data-ttu-id="89688-106">Polecenie cmdlet New-AzPowerBIEmbeddedCapacity tworzy nową, zawbudowaną pojemność usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="89688-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="89688-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89688-107">EXAMPLES</span></span>

### <span data-ttu-id="89688-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="89688-108">Example 1</span></span>
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

<span data-ttu-id="89688-109">Tworzy wydajność o nazwie testcapacity w regionie Azure Region Zachodni (Stanów Zjednoczonych) i w grupie zasób testRG.</span><span class="sxs-lookup"><span data-stu-id="89688-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="89688-110">Poziom wersji SKU dla wydajności to a1.</span><span class="sxs-lookup"><span data-stu-id="89688-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="89688-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89688-111">PARAMETERS</span></span>

### <span data-ttu-id="89688-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="89688-112">-Administrator</span></span>
<span data-ttu-id="89688-113">Nazwy rozdzielone przecinkami w celu ustawienia ich jako administrator na karcie wydajność</span><span class="sxs-lookup"><span data-stu-id="89688-113">A comma separated names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="89688-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89688-114">-DefaultProfile</span></span>
<span data-ttu-id="89688-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89688-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89688-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="89688-116">-Location</span></span>
<span data-ttu-id="89688-117">Obszar platformy Azure, w którym jest hostowana pojemność osadzona w usłudze PowerBI</span><span class="sxs-lookup"><span data-stu-id="89688-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="89688-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="89688-118">-Name</span></span>
<span data-ttu-id="89688-119">Nazwa wbudowanej pojemności usługi PowerBI</span><span class="sxs-lookup"><span data-stu-id="89688-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="89688-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89688-120">-ResourceGroupName</span></span>
<span data-ttu-id="89688-121">Nazwa grupy zasobów platformy Azure, do której należy pojemność</span><span class="sxs-lookup"><span data-stu-id="89688-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="89688-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="89688-122">-Sku</span></span>
<span data-ttu-id="89688-123">Nazwa jednostki SKU dla pojemności.</span><span class="sxs-lookup"><span data-stu-id="89688-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="89688-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="89688-124">-Tag</span></span>
<span data-ttu-id="89688-125">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na pojemności.</span><span class="sxs-lookup"><span data-stu-id="89688-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="89688-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89688-126">-Confirm</span></span>
<span data-ttu-id="89688-127">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="89688-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="89688-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89688-128">-WhatIf</span></span>
<span data-ttu-id="89688-129">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="89688-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="89688-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89688-130">CommonParameters</span></span>
<span data-ttu-id="89688-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89688-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89688-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89688-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89688-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89688-133">INPUTS</span></span>

### <span data-ttu-id="89688-134">System. String</span><span class="sxs-lookup"><span data-stu-id="89688-134">System.String</span></span>

### <span data-ttu-id="89688-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="89688-135">System.String[]</span></span>

### <span data-ttu-id="89688-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="89688-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="89688-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89688-137">OUTPUTS</span></span>

### <span data-ttu-id="89688-138">Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="89688-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="89688-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89688-139">NOTES</span></span>

## <span data-ttu-id="89688-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89688-140">RELATED LINKS</span></span>

[<span data-ttu-id="89688-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="89688-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="89688-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="89688-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
