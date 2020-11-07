---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 07b5de12e042c81bb5f27c844d1fc8962453310a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719324"
---
# <span data-ttu-id="c440f-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="c440f-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="c440f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c440f-102">SYNOPSIS</span></span>
<span data-ttu-id="c440f-103">Tworzy obszar nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c440f-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c440f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c440f-104">SYNTAX</span></span>

### <span data-ttu-id="c440f-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c440f-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c440f-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c440f-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-EnableAutoInflate]
 [-MaximumThroughputUnits] <Int32> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="c440f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c440f-107">DESCRIPTION</span></span>
<span data-ttu-id="c440f-108">Polecenie cmdlet New-AzureRmEventHubNamespace tworzy nowy obszar nazw dla koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c440f-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="c440f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c440f-109">EXAMPLES</span></span>

### <span data-ttu-id="c440f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c440f-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation 
```

<span data-ttu-id="c440f-111">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` w obszarze MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="c440f-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c440f-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c440f-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="c440f-113">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` , w grupie zasoby \` MyResourceGroupName \` i funkcja autorozdęcie jest włączona z MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="c440f-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="c440f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c440f-114">PARAMETERS</span></span>

### <span data-ttu-id="c440f-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c440f-115">-Location</span></span>
<span data-ttu-id="c440f-116">Lokalizacja obszaru geograficznego dla koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c440f-116">Event Hubs namespace geo-location.</span></span>

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

### <span data-ttu-id="c440f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c440f-117">-ResourceGroupName</span></span>
<span data-ttu-id="c440f-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c440f-118">Resource group name.</span></span>

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

### <span data-ttu-id="c440f-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c440f-119">-SkuCapacity</span></span>
<span data-ttu-id="c440f-120">Jednostki przepływności centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c440f-120">The Event Hub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c440f-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c440f-121">-SkuName</span></span>
<span data-ttu-id="c440f-122">Nazwa SKU obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="c440f-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c440f-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="c440f-123">-Tag</span></span>
<span data-ttu-id="c440f-124">Hashtable, które reprezentują znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="c440f-124">Hashtables that represent resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c440f-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c440f-125">-Confirm</span></span>
<span data-ttu-id="c440f-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c440f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c440f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c440f-127">-WhatIf</span></span>
<span data-ttu-id="c440f-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c440f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c440f-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c440f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c440f-130">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="c440f-130">-EnableAutoInflate</span></span>
<span data-ttu-id="c440f-131">Wskazuje, czy funkcja autorozdęcie jest włączona</span><span class="sxs-lookup"><span data-stu-id="c440f-131">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c440f-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="c440f-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="c440f-133">Górny limit jednostek przepływności, gdy funkcja podwyższanie jest włączona, vaule powinna należeć do zakresu od 0 do 20 jednostek przepływności.</span><span class="sxs-lookup"><span data-stu-id="c440f-133">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c440f-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c440f-134">-Name</span></span>
<span data-ttu-id="c440f-135">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="c440f-135">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="c440f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c440f-136">INPUTS</span></span>

### <span data-ttu-id="c440f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c440f-137">System.String</span></span>
<span data-ttu-id="c440f-138">System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral; PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089 \] \] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c440f-138">System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Collections.Hashtable</span></span>

## <span data-ttu-id="c440f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c440f-139">OUTPUTS</span></span>

### <span data-ttu-id="c440f-140">Microsoft. Azure. Commands. EventHub. modele. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c440f-140">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="c440f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c440f-141">NOTES</span></span>

## <span data-ttu-id="c440f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c440f-142">RELATED LINKS</span></span>

