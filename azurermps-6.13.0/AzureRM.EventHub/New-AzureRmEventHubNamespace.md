---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 0fb90529f4157bf627e43477e3db41764040e5c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717410"
---
# <span data-ttu-id="86d2e-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="86d2e-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="86d2e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="86d2e-103">Tworzy obszar nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="86d2e-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86d2e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86d2e-104">SYNTAX</span></span>

### <span data-ttu-id="86d2e-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="86d2e-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86d2e-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="86d2e-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86d2e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="86d2e-107">DESCRIPTION</span></span>
<span data-ttu-id="86d2e-108">Polecenie cmdlet New-AzureRmEventHubNamespace tworzy nowy obszar nazw dla koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="86d2e-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="86d2e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86d2e-109">EXAMPLES</span></span>

### <span data-ttu-id="86d2e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="86d2e-110">Example 1</span></span>                                              
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="86d2e-111">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` w obszarze MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="86d2e-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="86d2e-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="86d2e-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="86d2e-113">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` , w grupie zasoby \` MyResourceGroupName \` i funkcja autorozdęcie jest włączona z MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="86d2e-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="86d2e-114">Przykład 3-Kafka z włączoną przestrzenią nazw</span><span class="sxs-lookup"><span data-stu-id="86d2e-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka
```

<span data-ttu-id="86d2e-115">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` , w grupie zasób \` MyResourceGroupName \` z Kafka i funkcja autorozdęcie włączona.</span><span class="sxs-lookup"><span data-stu-id="86d2e-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="86d2e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86d2e-116">PARAMETERS</span></span>

### <span data-ttu-id="86d2e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d2e-117">-DefaultProfile</span></span>
<span data-ttu-id="86d2e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86d2e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86d2e-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="86d2e-119">-EnableAutoInflate</span></span>
<span data-ttu-id="86d2e-120">Wskazuje, czy funkcja autorozdęcie jest włączona</span><span class="sxs-lookup"><span data-stu-id="86d2e-120">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="86d2e-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="86d2e-121">-EnableKafka</span></span>
<span data-ttu-id="86d2e-122">Włączanie lub wyłączanie Kafka dla obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="86d2e-122">enabling or disabling Kafka for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```         

### <span data-ttu-id="86d2e-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="86d2e-123">-Location</span></span>
<span data-ttu-id="86d2e-124">Lokalizacja obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="86d2e-124">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="86d2e-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="86d2e-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="86d2e-126">Górny limit jednostek przepływności, gdy funkcja podwyższanie jest włączona, wartość powinna należeć do zakresu od 0 do 20 jednostek przepływności.</span><span class="sxs-lookup"><span data-stu-id="86d2e-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86d2e-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86d2e-127">-Name</span></span>
<span data-ttu-id="86d2e-128">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="86d2e-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="86d2e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d2e-129">-ResourceGroupName</span></span>
<span data-ttu-id="86d2e-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="86d2e-130">Resource Group Name</span></span>

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

### <span data-ttu-id="86d2e-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="86d2e-131">-SkuCapacity</span></span>
<span data-ttu-id="86d2e-132">Jednostki przepływności eventhub.</span><span class="sxs-lookup"><span data-stu-id="86d2e-132">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="86d2e-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="86d2e-133">-SkuName</span></span>
<span data-ttu-id="86d2e-134">Nazwa SKU obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="86d2e-134">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="86d2e-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="86d2e-135">-Tag</span></span>
<span data-ttu-id="86d2e-136">Hashtable, które reprezentują znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="86d2e-136">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86d2e-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86d2e-137">-Confirm</span></span>
<span data-ttu-id="86d2e-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86d2e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86d2e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86d2e-139">-WhatIf</span></span>
<span data-ttu-id="86d2e-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86d2e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86d2e-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="86d2e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86d2e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d2e-142">CommonParameters</span></span>
<span data-ttu-id="86d2e-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d2e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="86d2e-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d2e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d2e-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86d2e-145">INPUTS</span></span>


## <span data-ttu-id="86d2e-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86d2e-146">OUTPUTS</span></span>

### <span data-ttu-id="86d2e-147">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="86d2e-147">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="86d2e-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86d2e-148">NOTES</span></span>

## <span data-ttu-id="86d2e-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86d2e-149">RELATED LINKS</span></span>
