---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 9217dfa2d5465841cb0ed33c2781849ddebff3b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705441"
---
# <span data-ttu-id="acf2d-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="acf2d-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="acf2d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="acf2d-102">SYNOPSIS</span></span>
<span data-ttu-id="acf2d-103">Tworzy obszar nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="acf2d-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="acf2d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="acf2d-104">SYNTAX</span></span>

### <span data-ttu-id="acf2d-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="acf2d-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf2d-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="acf2d-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acf2d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="acf2d-107">DESCRIPTION</span></span>
<span data-ttu-id="acf2d-108">Polecenie cmdlet New-AzEventHubNamespace tworzy nowy obszar nazw dla koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="acf2d-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="acf2d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="acf2d-109">EXAMPLES</span></span>

### <span data-ttu-id="acf2d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="acf2d-110">Example 1</span></span>                                           
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : False
MaximumThroughputUnits : 0
```

<span data-ttu-id="acf2d-111">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` w obszarze MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="acf2d-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="acf2d-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="acf2d-112">Example 2</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="acf2d-113">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` , w grupie zasoby \` MyResourceGroupName \` i funkcja autorozdęcie jest włączona z MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="acf2d-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="acf2d-114">Przykład 3-Kafka z włączoną przestrzenią nazw</span><span class="sxs-lookup"><span data-stu-id="acf2d-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 12
```

<span data-ttu-id="acf2d-115">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` , w grupie zasób \` MyResourceGroupName \` z Kafka i funkcja autorozdęcie włączona.</span><span class="sxs-lookup"><span data-stu-id="acf2d-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="acf2d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="acf2d-116">PARAMETERS</span></span>

### <span data-ttu-id="acf2d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf2d-117">-DefaultProfile</span></span>
<span data-ttu-id="acf2d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="acf2d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf2d-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="acf2d-119">-EnableAutoInflate</span></span>
<span data-ttu-id="acf2d-120">Wskazuje, czy funkcja autorozdęcie jest włączona</span><span class="sxs-lookup"><span data-stu-id="acf2d-120">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="acf2d-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="acf2d-121">-EnableKafka</span></span>
<span data-ttu-id="acf2d-122">Włączanie lub wyłączanie Kafka dla obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="acf2d-122">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="acf2d-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="acf2d-123">-Location</span></span>
<span data-ttu-id="acf2d-124">Lokalizacja obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="acf2d-124">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="acf2d-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="acf2d-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="acf2d-126">Górny limit jednostek przepływności, gdy funkcja podwyższanie jest włączona, wartość powinna należeć do zakresu od 0 do 20 jednostek przepływności.</span><span class="sxs-lookup"><span data-stu-id="acf2d-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="acf2d-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="acf2d-127">-Name</span></span>
<span data-ttu-id="acf2d-128">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="acf2d-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="acf2d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf2d-129">-ResourceGroupName</span></span>
<span data-ttu-id="acf2d-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="acf2d-130">Resource Group Name</span></span>

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

### <span data-ttu-id="acf2d-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="acf2d-131">-SkuCapacity</span></span>
<span data-ttu-id="acf2d-132">Jednostki przepływności eventhub.</span><span class="sxs-lookup"><span data-stu-id="acf2d-132">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="acf2d-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="acf2d-133">-SkuName</span></span>
<span data-ttu-id="acf2d-134">Nazwa SKU obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="acf2d-134">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="acf2d-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="acf2d-135">-Tag</span></span>
<span data-ttu-id="acf2d-136">Hashtable, które reprezentują znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="acf2d-136">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="acf2d-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="acf2d-137">-Confirm</span></span>
<span data-ttu-id="acf2d-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acf2d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acf2d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf2d-139">-WhatIf</span></span>
<span data-ttu-id="acf2d-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acf2d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf2d-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="acf2d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acf2d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf2d-142">CommonParameters</span></span>
<span data-ttu-id="acf2d-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acf2d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf2d-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acf2d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf2d-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="acf2d-145">INPUTS</span></span>

### <span data-ttu-id="acf2d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="acf2d-146">System.String</span></span>

### <span data-ttu-id="acf2d-147">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="acf2d-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="acf2d-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="acf2d-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="acf2d-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="acf2d-149">OUTPUTS</span></span>

### <span data-ttu-id="acf2d-150">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="acf2d-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="acf2d-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="acf2d-151">NOTES</span></span>

## <span data-ttu-id="acf2d-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="acf2d-152">RELATED LINKS</span></span>