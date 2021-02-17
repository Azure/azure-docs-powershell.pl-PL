---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: a51fffe36102b05121e52054103357bd26f56d51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188450"
---
# <span data-ttu-id="26eac-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="26eac-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="26eac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26eac-102">SYNOPSIS</span></span>
<span data-ttu-id="26eac-103">Tworzy przestrzeń nazw centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="26eac-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="26eac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="26eac-104">SYNTAX</span></span>

### <span data-ttu-id="26eac-105">NamespaceParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="26eac-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-ZoneRedundant]
 [[-ClusterARMId] <String>] [-Identity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26eac-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="26eac-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-ZoneRedundant] [[-ClusterARMId] <String>] [-Identity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26eac-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="26eac-107">DESCRIPTION</span></span>
<span data-ttu-id="26eac-108">Polecenie New-AzEventHubNamespace cmdlet tworzy nową przestrzeń nazw typu Centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="26eac-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="26eac-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="26eac-109">EXAMPLES</span></span>
### <span data-ttu-id="26eac-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26eac-110">Example 1</span></span>                                           
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

<span data-ttu-id="26eac-111">Tworzy przestrzeń nazw MyNamespaceName w centrum zdarzeń w określonej lokalizacji geograficznej, w grupie zasobów \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="26eac-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="26eac-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="26eac-112">Example 2</span></span>
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

<span data-ttu-id="26eac-113">Tworzy przestrzeń nazw MyNamespaceName w centrum zdarzeń w określonej lokalizacji geograficznej, w grupie zasobów nazwa_grupy zasobów MyResourceGroupName i funkcja AutoInflate jest włączona z parametrem \` \` \` \` \` \` MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="26eac-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="26eac-114">Przykład 3. Włączono przestrzeń nazw usługi Kafka</span><span class="sxs-lookup"><span data-stu-id="26eac-114">Example 3: Kafka enabled namespace</span></span>
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

<span data-ttu-id="26eac-115">Tworzy przestrzeń nazw MyNamespaceName w centrum zdarzeń w określonej lokalizacji geograficznej, w grupie zasobów Nazwa_grupy zasobów MyResourceGroupName z włączonymi funkcjami Kafka i \` \` \` \` \` \` AutoInflate.</span><span class="sxs-lookup"><span data-stu-id="26eac-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="26eac-116">Przykład 4. Przestrzeń nazw z włączoną przestrzenią nazw ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="26eac-116">Example 4: ZoneRedundant enabled namespace</span></span>
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

<span data-ttu-id="26eac-117">Tworzy przestrzeń nazw MyNamespaceName w centrum zdarzeń w określonej lokalizacji geograficznej, w grupie zasobów MyResourceGroupName z włączonymi funkcjami Kafka i \` \` \` \` \` \` AutoInflate.</span><span class="sxs-lookup"><span data-stu-id="26eac-117">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="26eac-118">Przykład 5. Tworzenie przestrzeni nazw z zarządzaniem tożsamością w klastrze</span><span class="sxs-lookup"><span data-stu-id="26eac-118">Example 5: Creating Namespace with Manage Identity in a cluster</span></span> 
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

## <span data-ttu-id="26eac-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26eac-119">PARAMETERS</span></span>

### <span data-ttu-id="26eac-120">- ClusterARMId</span><span class="sxs-lookup"><span data-stu-id="26eac-120">-ClusterARMId</span></span>
<span data-ttu-id="26eac-121">ARM identyfikator klastrów, w którym należy utworzyć przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="26eac-121">ARM ID of Cluster where namespace is to be created</span></span>

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

### <span data-ttu-id="26eac-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26eac-122">-DefaultProfile</span></span>
<span data-ttu-id="26eac-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="26eac-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26eac-124">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="26eac-124">-EnableAutoInflate</span></span>
<span data-ttu-id="26eac-125">Wskazuje, czy funkcja Autoinflate jest włączona.</span><span class="sxs-lookup"><span data-stu-id="26eac-125">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="26eac-126">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="26eac-126">-EnableKafka</span></span>
<span data-ttu-id="26eac-127">Włączanie lub wyłączanie platformy Kafka dla przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="26eac-127">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="26eac-128">— Tożsamość</span><span class="sxs-lookup"><span data-stu-id="26eac-128">-Identity</span></span>
<span data-ttu-id="26eac-129">Włączanie lub wyłączanie tożsamości dla przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="26eac-129">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="26eac-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="26eac-130">-Location</span></span>
<span data-ttu-id="26eac-131">Lokalizacja przestrzeni nazw w usłudze EventHub.</span><span class="sxs-lookup"><span data-stu-id="26eac-131">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="26eac-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="26eac-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="26eac-133">Górny limit jednostek przepływności, gdy funkcja Autoinflate jest włączona, wartość powinna być w granicach od 0 do 20 jednostek przepływności.</span><span class="sxs-lookup"><span data-stu-id="26eac-133">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="26eac-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="26eac-134">-Name</span></span>
<span data-ttu-id="26eac-135">Nazwa przestrzeni nazw aplikacji EventHub.</span><span class="sxs-lookup"><span data-stu-id="26eac-135">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="26eac-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26eac-136">-ResourceGroupName</span></span>
<span data-ttu-id="26eac-137">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="26eac-137">Resource Group Name</span></span>

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

### <span data-ttu-id="26eac-138">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="26eac-138">-SkuCapacity</span></span>
<span data-ttu-id="26eac-139">Jednostki przepływności w aplikacji EventHub.</span><span class="sxs-lookup"><span data-stu-id="26eac-139">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="26eac-140">-SKUName</span><span class="sxs-lookup"><span data-stu-id="26eac-140">-SkuName</span></span>
<span data-ttu-id="26eac-141">Nazwa sku przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="26eac-141">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="26eac-142">— Tag</span><span class="sxs-lookup"><span data-stu-id="26eac-142">-Tag</span></span>
<span data-ttu-id="26eac-143">Skróty reprezentujące tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="26eac-143">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="26eac-144">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="26eac-144">-ZoneRedundant</span></span>
<span data-ttu-id="26eac-145">Włączanie lub wyłączanie nadmiarowej strefy dla przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="26eac-145">enabling or disabling Zone Redundant for namespace</span></span>

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

### <span data-ttu-id="26eac-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26eac-146">-Confirm</span></span>
<span data-ttu-id="26eac-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="26eac-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26eac-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26eac-148">-WhatIf</span></span>
<span data-ttu-id="26eac-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26eac-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26eac-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="26eac-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26eac-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26eac-151">CommonParameters</span></span>
<span data-ttu-id="26eac-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26eac-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26eac-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26eac-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26eac-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26eac-154">INPUTS</span></span>

### <span data-ttu-id="26eac-155">System.String</span><span class="sxs-lookup"><span data-stu-id="26eac-155">System.String</span></span>

### <span data-ttu-id="26eac-156">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="26eac-156">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="26eac-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="26eac-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="26eac-158">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26eac-158">OUTPUTS</span></span>

### <span data-ttu-id="26eac-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="26eac-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="26eac-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="26eac-160">NOTES</span></span>

## <span data-ttu-id="26eac-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26eac-161">RELATED LINKS</span></span>
