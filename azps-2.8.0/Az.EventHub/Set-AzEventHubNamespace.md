---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: 99993a92179da1adaba068ae7bb525b5b2cca5df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705411"
---
# <span data-ttu-id="7e7cf-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="7e7cf-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="7e7cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="7e7cf-103">Umożliwia zaktualizowanie określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="7e7cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e7cf-104">SYNTAX</span></span>

### <span data-ttu-id="7e7cf-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7e7cf-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e7cf-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e7cf-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e7cf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7e7cf-107">DESCRIPTION</span></span>
<span data-ttu-id="7e7cf-108">Polecenie cmdlet Set-AzEventHubNamespace aktualizuje właściwości określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="7e7cf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e7cf-109">EXAMPLES</span></span>

### <span data-ttu-id="7e7cf-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7e7cf-110">Example 1</span></span>
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

<span data-ttu-id="7e7cf-111">Aktualizuje znaczniki obszaru nazw NamespaceName \` \` na utworzony.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-111">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="7e7cf-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7e7cf-112">Example 2</span></span>
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

<span data-ttu-id="7e7cf-113">Umożliwia zaktualizowanie stanu przestrzeni nazw obszar_nazwname \` \` za pomocą funkcji autorozdęcie = włączone i MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="7e7cf-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="7e7cf-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e7cf-114">PARAMETERS</span></span>

### <span data-ttu-id="7e7cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e7cf-115">-DefaultProfile</span></span>
<span data-ttu-id="7e7cf-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e7cf-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="7e7cf-117">-EnableAutoInflate</span></span>
<span data-ttu-id="7e7cf-118">Wskazuje, czy funkcja autorozdęcie jest włączona</span><span class="sxs-lookup"><span data-stu-id="7e7cf-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="7e7cf-119">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="7e7cf-119">-EnableKafka</span></span>
<span data-ttu-id="7e7cf-120">Włączanie lub wyłączanie Kafka dla obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="7e7cf-120">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="7e7cf-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7e7cf-121">-Location</span></span>
<span data-ttu-id="7e7cf-122">Lokalizacja obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-122">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="7e7cf-123">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="7e7cf-123">-MaximumThroughputUnits</span></span>
<span data-ttu-id="7e7cf-124">Górny limit jednostek przepływności, gdy funkcja podwyższanie jest włączona, wartość powinna należeć do zakresu od 0 do 20 jednostek przepływności.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-124">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="7e7cf-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e7cf-125">-Name</span></span>
<span data-ttu-id="7e7cf-126">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-126">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="7e7cf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e7cf-127">-ResourceGroupName</span></span>
<span data-ttu-id="7e7cf-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="7e7cf-129">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7e7cf-129">-SkuCapacity</span></span>
<span data-ttu-id="7e7cf-130">Jednostki przepływności eventhub.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-130">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="7e7cf-131">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7e7cf-131">-SkuName</span></span>
<span data-ttu-id="7e7cf-132">Nazwa SKU obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-132">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="7e7cf-133">-State</span><span class="sxs-lookup"><span data-stu-id="7e7cf-133">-State</span></span>
<span data-ttu-id="7e7cf-134">Wyłącz/Włącz obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-134">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="7e7cf-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e7cf-135">-Tag</span></span>
<span data-ttu-id="7e7cf-136">Hashtable, które reprezentują znacznik zasobu.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-136">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="7e7cf-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e7cf-137">-Confirm</span></span>
<span data-ttu-id="7e7cf-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e7cf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e7cf-139">-WhatIf</span></span>
<span data-ttu-id="7e7cf-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e7cf-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e7cf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e7cf-142">CommonParameters</span></span>
<span data-ttu-id="7e7cf-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e7cf-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e7cf-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e7cf-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e7cf-145">INPUTS</span></span>

### <span data-ttu-id="7e7cf-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7e7cf-146">System.String</span></span>

### <span data-ttu-id="7e7cf-147">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7e7cf-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7e7cf-148">System. Nullable "1 [[Microsoft. Azure. Commands. EventHub. MODELES. NamespaceState; Microsoft. Azure. PowerShell. PowerShell. w usłudze EventHub, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7e7cf-148">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7e7cf-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e7cf-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7e7cf-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e7cf-150">OUTPUTS</span></span>

### <span data-ttu-id="7e7cf-151">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7e7cf-151">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="7e7cf-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e7cf-152">NOTES</span></span>

## <span data-ttu-id="7e7cf-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e7cf-153">RELATED LINKS</span></span>
