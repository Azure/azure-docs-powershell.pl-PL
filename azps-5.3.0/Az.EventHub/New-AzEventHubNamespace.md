---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: a51fffe36102b05121e52054103357bd26f56d51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501075"
---
# <span data-ttu-id="15c0c-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="15c0c-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="15c0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="15c0c-103">Tworzy obszar nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="15c0c-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="15c0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15c0c-104">SYNTAX</span></span>

### <span data-ttu-id="15c0c-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="15c0c-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-ZoneRedundant]
 [[-ClusterARMId] <String>] [-Identity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15c0c-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c0c-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-ZoneRedundant] [[-ClusterARMId] <String>] [-Identity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15c0c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="15c0c-107">DESCRIPTION</span></span>
<span data-ttu-id="15c0c-108">Polecenie cmdlet New-AzEventHubNamespace tworzy nowy obszar nazw dla koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="15c0c-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="15c0c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15c0c-109">EXAMPLES</span></span>
### <span data-ttu-id="15c0c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="15c0c-110">Example 1</span></span>                                           
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/14/2020 9:02:16 PM
UpdatedAt                     : 6/14/2020 9:03:04 PM
ServiceBusEndpoint            : https://testingnew2018.servicebus.windows.net:443/
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : False
MaximumThroughputUnits        : 0
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="15c0c-111">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` w obszarze MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="15c0c-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="15c0c-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="15c0c-112">Example 2</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="15c0c-113">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` , w grupie zasoby \` MyResourceGroupName \` i funkcja autorozdęcie jest włączona z MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="15c0c-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="15c0c-114">Przykład 3: obszar nazw z włączoną Kafka</span><span class="sxs-lookup"><span data-stu-id="15c0c-114">Example 3: Kafka enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="15c0c-115">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` , w grupie zasób \` MyResourceGroupName \` z Kafka i funkcja autorozdęcie włączona.</span><span class="sxs-lookup"><span data-stu-id="15c0c-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="15c0c-116">Przykład 4: obszar nazw z włączoną obsługą ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="15c0c-116">Example 4: ZoneRedundant enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -ZoneRedundant

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : True
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="15c0c-117">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` , w grupie zasób \` MyResourceGroupName \` z Kafka i funkcja autorozdęcie włączona.</span><span class="sxs-lookup"><span data-stu-id="15c0c-117">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="15c0c-118">Przykład 5. Tworzenie obszaru nazw za pomocą zarządzania tożsamością w klastrze</span><span class="sxs-lookup"><span data-stu-id="15c0c-118">Example 5: Creating Namespace with Manage Identity in a cluster</span></span> 
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation --EnableAutoInflate -MaximumThroughputUnits 12 -EnableKafka -ZoneRedundant -Identity

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 12
ZoneRedundant                 : True
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity.PrincipalId          : ##########
Identity.TenantId             : ##########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :


# Get created namespace
PS C:\>$getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
PS C:\> $key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperties @(@($key.Name, $keyvault.VaultUri,""))

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
ServiceBusEndpoint            : #########
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          : #########
Identity.TenantId             : #########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          : MicrosoftKeyVault
Encryption.KeyVaultProperties : {testkey, https://myvaultname.vault.azure.net, }
```

## <span data-ttu-id="15c0c-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15c0c-119">PARAMETERS</span></span>

### <span data-ttu-id="15c0c-120">-ClusterARMId</span><span class="sxs-lookup"><span data-stu-id="15c0c-120">-ClusterARMId</span></span>
<span data-ttu-id="15c0c-121">Identyfikator ARM klastra, w którym ma zostać utworzony obszar nazw</span><span class="sxs-lookup"><span data-stu-id="15c0c-121">ARM ID of Cluster where namespace is to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15c0c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c0c-122">-DefaultProfile</span></span>
<span data-ttu-id="15c0c-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15c0c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c0c-124">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="15c0c-124">-EnableAutoInflate</span></span>
<span data-ttu-id="15c0c-125">Wskazuje, czy funkcja autorozdęcie jest włączona</span><span class="sxs-lookup"><span data-stu-id="15c0c-125">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="15c0c-126">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="15c0c-126">-EnableKafka</span></span>
<span data-ttu-id="15c0c-127">Włączanie lub wyłączanie Kafka dla obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="15c0c-127">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="15c0c-128">-Identity (tożsamość)</span><span class="sxs-lookup"><span data-stu-id="15c0c-128">-Identity</span></span>
<span data-ttu-id="15c0c-129">Włączanie lub wyłączanie tożsamości obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="15c0c-129">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="15c0c-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="15c0c-130">-Location</span></span>
<span data-ttu-id="15c0c-131">Lokalizacja obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="15c0c-131">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="15c0c-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="15c0c-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="15c0c-133">Górny limit jednostek przepływności, gdy funkcja podwyższanie jest włączona, wartość powinna należeć do zakresu od 0 do 20 jednostek przepływności.</span><span class="sxs-lookup"><span data-stu-id="15c0c-133">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="15c0c-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="15c0c-134">-Name</span></span>
<span data-ttu-id="15c0c-135">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="15c0c-135">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="15c0c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15c0c-136">-ResourceGroupName</span></span>
<span data-ttu-id="15c0c-137">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="15c0c-137">Resource Group Name</span></span>

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

### <span data-ttu-id="15c0c-138">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="15c0c-138">-SkuCapacity</span></span>
<span data-ttu-id="15c0c-139">Jednostki przepływności eventhub.</span><span class="sxs-lookup"><span data-stu-id="15c0c-139">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="15c0c-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="15c0c-140">-SkuName</span></span>
<span data-ttu-id="15c0c-141">Nazwa SKU obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="15c0c-141">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="15c0c-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="15c0c-142">-Tag</span></span>
<span data-ttu-id="15c0c-143">Hashtable, które reprezentują znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="15c0c-143">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="15c0c-144">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="15c0c-144">-ZoneRedundant</span></span>
<span data-ttu-id="15c0c-145">Włączanie i wyłączanie nadmiarowych stref dla obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="15c0c-145">enabling or disabling Zone Redundant for namespace</span></span>

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

### <span data-ttu-id="15c0c-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15c0c-146">-Confirm</span></span>
<span data-ttu-id="15c0c-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15c0c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15c0c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15c0c-148">-WhatIf</span></span>
<span data-ttu-id="15c0c-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15c0c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15c0c-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="15c0c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15c0c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c0c-151">CommonParameters</span></span>
<span data-ttu-id="15c0c-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15c0c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c0c-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15c0c-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c0c-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15c0c-154">INPUTS</span></span>

### <span data-ttu-id="15c0c-155">System. String</span><span class="sxs-lookup"><span data-stu-id="15c0c-155">System.String</span></span>

### <span data-ttu-id="15c0c-156">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="15c0c-156">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="15c0c-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="15c0c-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="15c0c-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15c0c-158">OUTPUTS</span></span>

### <span data-ttu-id="15c0c-159">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="15c0c-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="15c0c-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15c0c-160">NOTES</span></span>

## <span data-ttu-id="15c0c-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15c0c-161">RELATED LINKS</span></span>
