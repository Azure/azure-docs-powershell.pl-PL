---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/6911f050bfba3248a3fd992fbc2645e3a1a8641d
ms.openlocfilehash: 05f0c3cd3947a1955689a7359b40d59052863ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527582"
---
# <span data-ttu-id="e569d-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="e569d-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="e569d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e569d-102">SYNOPSIS</span></span>
<span data-ttu-id="e569d-103">Umożliwia zaktualizowanie określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="e569d-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e569d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e569d-104">SYNTAX</span></span>

### <span data-ttu-id="e569d-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e569d-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e569d-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e569d-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e569d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e569d-107">DESCRIPTION</span></span>
<span data-ttu-id="e569d-108">Polecenie cmdlet Set-AzureRmEventHubNamespace aktualizuje właściwości określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="e569d-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="e569d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e569d-109">EXAMPLES</span></span>

### <span data-ttu-id="e569d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e569d-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="e569d-111">Umożliwia zaktualizowanie stanu obszaru nazw NamespaceName \` \` .</span><span class="sxs-lookup"><span data-stu-id="e569d-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="e569d-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e569d-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="e569d-113">Umożliwia zaktualizowanie stanu przestrzeni nazw obszar_nazwname \` \` za pomocą funkcji autorozdęcie = włączone i MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="e569d-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="e569d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e569d-114">PARAMETERS</span></span>

### <span data-ttu-id="e569d-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e569d-115">-Location</span></span>
<span data-ttu-id="e569d-116">Lokalizacja obszaru geograficznego dla koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="e569d-116">Event Hubs namespace geo-location.</span></span>

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

### <span data-ttu-id="e569d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e569d-117">-ResourceGroupName</span></span>
<span data-ttu-id="e569d-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e569d-118">Resource group name.</span></span>

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

### <span data-ttu-id="e569d-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e569d-119">-SkuCapacity</span></span>
<span data-ttu-id="e569d-120">Jednostki przepływności centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="e569d-120">The Event Hub throughput units.</span></span>

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

### <span data-ttu-id="e569d-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e569d-121">-SkuName</span></span>
<span data-ttu-id="e569d-122">Nazwa SKU obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="e569d-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e569d-123">-State</span><span class="sxs-lookup"><span data-stu-id="e569d-123">-State</span></span>
<span data-ttu-id="e569d-124">Określa stan (wyłączony lub włączony) obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="e569d-124">Specifies the state (disabled or enabled) of the namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, Creating, Created, Activating, Enabling, Active, Disabling, Disabled, SoftDeleting, SoftDeleted, Removing, Removed, Failed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e569d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="e569d-125">-Tag</span></span>
<span data-ttu-id="e569d-126">Hashtable, które reprezentują znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="e569d-126">Hashtables that represent resource tags.</span></span>

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

### <span data-ttu-id="e569d-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e569d-127">-Confirm</span></span>
<span data-ttu-id="e569d-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e569d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e569d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e569d-129">-WhatIf</span></span>
<span data-ttu-id="e569d-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e569d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e569d-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e569d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e569d-132">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="e569d-132">-EnableAutoInflate</span></span>
<span data-ttu-id="e569d-133">Wskazuje, czy funkcja autorozdęcie jest włączona</span><span class="sxs-lookup"><span data-stu-id="e569d-133">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="e569d-134">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="e569d-134">-MaximumThroughputUnits</span></span>
<span data-ttu-id="e569d-135">Górny limit jednostek przepływności, gdy funkcja podwyższanie jest włączona, vaule powinna należeć do zakresu od 0 do 20 jednostek przepływności.</span><span class="sxs-lookup"><span data-stu-id="e569d-135">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="e569d-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e569d-136">-Name</span></span>
<span data-ttu-id="e569d-137">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="e569d-137">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="e569d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e569d-138">INPUTS</span></span>

### <span data-ttu-id="e569d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e569d-139">System.String</span></span>

### <span data-ttu-id="e569d-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e569d-140">System.Int32</span></span>

### <span data-ttu-id="e569d-141">Microsoft. Azure. Management. EventHub. MODELES. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="e569d-141">Microsoft.Azure.Management.EventHub.Models.NamespaceState</span></span>

### <span data-ttu-id="e569d-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e569d-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e569d-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e569d-143">OUTPUTS</span></span>

### <span data-ttu-id="e569d-144">Microsoft. Azure. Commands. EventHub. modele. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e569d-144">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="e569d-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e569d-145">NOTES</span></span>

## <span data-ttu-id="e569d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e569d-146">RELATED LINKS</span></span>

