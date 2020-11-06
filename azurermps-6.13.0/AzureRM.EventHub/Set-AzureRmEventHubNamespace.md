---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6fd3f000f7c91f0475cd18802dd6a9d096d35f5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548667"
---
# <span data-ttu-id="b593b-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b593b-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="b593b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b593b-102">SYNOPSIS</span></span>
<span data-ttu-id="b593b-103">Umożliwia zaktualizowanie określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b593b-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b593b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b593b-104">SYNTAX</span></span>

### <span data-ttu-id="b593b-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b593b-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b593b-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="b593b-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b593b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b593b-107">DESCRIPTION</span></span>
<span data-ttu-id="b593b-108">Polecenie cmdlet Set-AzureRmEventHubNamespace aktualizuje właściwości określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b593b-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="b593b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b593b-109">EXAMPLES</span></span>

### <span data-ttu-id="b593b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b593b-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="b593b-111">Umożliwia zaktualizowanie stanu obszaru nazw NamespaceName \` \` .</span><span class="sxs-lookup"><span data-stu-id="b593b-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="b593b-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b593b-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="b593b-113">Umożliwia zaktualizowanie stanu przestrzeni nazw obszar_nazwname \` \` za pomocą funkcji autorozdęcie = włączone i MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="b593b-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="b593b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b593b-114">PARAMETERS</span></span>

### <span data-ttu-id="b593b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b593b-115">-DefaultProfile</span></span>
<span data-ttu-id="b593b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b593b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b593b-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="b593b-117">-EnableAutoInflate</span></span>
<span data-ttu-id="b593b-118">Wskazuje, czy funkcja autorozdęcie jest włączona</span><span class="sxs-lookup"><span data-stu-id="b593b-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b593b-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b593b-119">-Location</span></span>
<span data-ttu-id="b593b-120">Lokalizacja obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="b593b-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="b593b-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="b593b-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="b593b-122">Górny limit jednostek przepływności, gdy funkcja podwyższanie jest włączona, wartość powinna należeć do zakresu od 0 do 20 jednostek przepływności.</span><span class="sxs-lookup"><span data-stu-id="b593b-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b593b-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b593b-123">-Name</span></span>
<span data-ttu-id="b593b-124">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="b593b-124">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b593b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b593b-125">-ResourceGroupName</span></span>
<span data-ttu-id="b593b-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b593b-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="b593b-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b593b-127">-SkuCapacity</span></span>
<span data-ttu-id="b593b-128">Jednostki przepływności eventhub.</span><span class="sxs-lookup"><span data-stu-id="b593b-128">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b593b-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b593b-129">-SkuName</span></span>
<span data-ttu-id="b593b-130">Nazwa SKU obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="b593b-130">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b593b-131">-State</span><span class="sxs-lookup"><span data-stu-id="b593b-131">-State</span></span>
<span data-ttu-id="b593b-132">Wyłącz/Włącz obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="b593b-132">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b593b-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="b593b-133">-Tag</span></span>
<span data-ttu-id="b593b-134">Hashtable, które reprezentują znacznik zasobu.</span><span class="sxs-lookup"><span data-stu-id="b593b-134">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b593b-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b593b-135">-Confirm</span></span>
<span data-ttu-id="b593b-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b593b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b593b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b593b-137">-WhatIf</span></span>
<span data-ttu-id="b593b-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b593b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b593b-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b593b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b593b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b593b-140">CommonParameters</span></span>
<span data-ttu-id="b593b-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b593b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b593b-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b593b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b593b-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b593b-143">INPUTS</span></span>

### <span data-ttu-id="b593b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b593b-144">System.String</span></span>

### <span data-ttu-id="b593b-145">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b593b-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b593b-146">System. Nullable "1 [[Microsoft. Azure. Commands. EventHub. MODELES. NamespaceState, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="b593b-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.Commands.EventHub, Version=0.6.7.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b593b-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b593b-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b593b-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b593b-148">OUTPUTS</span></span>

### <span data-ttu-id="b593b-149">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b593b-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="b593b-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b593b-150">NOTES</span></span>

## <span data-ttu-id="b593b-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b593b-151">RELATED LINKS</span></span>
