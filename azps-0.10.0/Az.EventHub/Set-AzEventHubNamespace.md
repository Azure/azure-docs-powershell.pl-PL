---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: af46e09571deba338d67b75659f6915ac0e8e061
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891409"
---
# <span data-ttu-id="ff80a-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ff80a-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="ff80a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff80a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff80a-103">Umożliwia zaktualizowanie określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ff80a-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ff80a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff80a-104">SYNTAX</span></span>

### <span data-ttu-id="ff80a-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ff80a-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff80a-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff80a-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff80a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ff80a-107">DESCRIPTION</span></span>
<span data-ttu-id="ff80a-108">Polecenie cmdlet Set-AzEventHubNamespace aktualizuje właściwości określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ff80a-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ff80a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff80a-109">EXAMPLES</span></span>

### <span data-ttu-id="ff80a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ff80a-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="ff80a-111">Aktualizuje znaczniki obszaru nazw NamespaceName \` \` na utworzony.</span><span class="sxs-lookup"><span data-stu-id="ff80a-111">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="ff80a-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ff80a-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
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
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="ff80a-113">Umożliwia zaktualizowanie stanu przestrzeni nazw obszar_nazwname \` \` za pomocą funkcji autorozdęcie = włączone i MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="ff80a-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="ff80a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff80a-114">PARAMETERS</span></span>

### <span data-ttu-id="ff80a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff80a-115">-DefaultProfile</span></span>
<span data-ttu-id="ff80a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff80a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff80a-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="ff80a-117">-EnableAutoInflate</span></span>
<span data-ttu-id="ff80a-118">Wskazuje, czy funkcja autorozdęcie jest włączona</span><span class="sxs-lookup"><span data-stu-id="ff80a-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="ff80a-119">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="ff80a-119">-EnableKafka</span></span>
<span data-ttu-id="ff80a-120">Włączanie lub wyłączanie Kafka dla obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="ff80a-120">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="ff80a-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ff80a-121">-Location</span></span>
<span data-ttu-id="ff80a-122">Lokalizacja obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="ff80a-122">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="ff80a-123">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="ff80a-123">-MaximumThroughputUnits</span></span>
<span data-ttu-id="ff80a-124">Górny limit jednostek przepływności, gdy funkcja podwyższanie jest włączona, wartość powinna należeć do zakresu od 0 do 20 jednostek przepływności.</span><span class="sxs-lookup"><span data-stu-id="ff80a-124">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="ff80a-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ff80a-125">-Name</span></span>
<span data-ttu-id="ff80a-126">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="ff80a-126">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="ff80a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff80a-127">-ResourceGroupName</span></span>
<span data-ttu-id="ff80a-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff80a-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="ff80a-129">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ff80a-129">-SkuCapacity</span></span>
<span data-ttu-id="ff80a-130">Jednostki przepływności eventhub.</span><span class="sxs-lookup"><span data-stu-id="ff80a-130">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="ff80a-131">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ff80a-131">-SkuName</span></span>
<span data-ttu-id="ff80a-132">Nazwa SKU obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="ff80a-132">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="ff80a-133">-State</span><span class="sxs-lookup"><span data-stu-id="ff80a-133">-State</span></span>
<span data-ttu-id="ff80a-134">Wyłącz/Włącz obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="ff80a-134">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="ff80a-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="ff80a-135">-Tag</span></span>
<span data-ttu-id="ff80a-136">Hashtable, które reprezentują znacznik zasobu.</span><span class="sxs-lookup"><span data-stu-id="ff80a-136">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="ff80a-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff80a-137">-Confirm</span></span>
<span data-ttu-id="ff80a-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff80a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff80a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff80a-139">-WhatIf</span></span>
<span data-ttu-id="ff80a-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff80a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff80a-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ff80a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff80a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff80a-142">CommonParameters</span></span>
<span data-ttu-id="ff80a-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff80a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff80a-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff80a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff80a-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff80a-145">INPUTS</span></span>

### <span data-ttu-id="ff80a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ff80a-146">System.String</span></span>

### <span data-ttu-id="ff80a-147">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ff80a-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ff80a-148">System. Nullable "1 [[Microsoft. Azure. Commands. EventHub. MODELES. NamespaceState; Microsoft. Azure. PowerShell. PowerShell. w usłudze EventHub, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ff80a-148">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ff80a-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ff80a-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ff80a-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff80a-150">OUTPUTS</span></span>

### <span data-ttu-id="ff80a-151">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ff80a-151">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ff80a-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff80a-152">NOTES</span></span>

## <span data-ttu-id="ff80a-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff80a-153">RELATED LINKS</span></span>
