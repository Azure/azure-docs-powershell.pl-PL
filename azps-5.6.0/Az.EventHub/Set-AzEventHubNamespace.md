---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: 6afbd081eca842e2185428f90a18932e05c3bbe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984649"
---
# <span data-ttu-id="131c3-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="131c3-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="131c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="131c3-102">SYNOPSIS</span></span>
<span data-ttu-id="131c3-103">Aktualizuje określoną przestrzeń nazw centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="131c3-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="131c3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="131c3-104">SYNTAX</span></span>

### <span data-ttu-id="131c3-105">NamespaceParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="131c3-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-Identity] [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="131c3-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="131c3-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity]
 [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="131c3-107">IdentityUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="131c3-107">IdentityUpdateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="131c3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="131c3-108">DESCRIPTION</span></span>
<span data-ttu-id="131c3-109">Polecenie Set-AzEventHubNamespace aktualizuje właściwości przestrzeni nazw określonych centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="131c3-109">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="131c3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="131c3-110">EXAMPLES</span></span>

### <span data-ttu-id="131c3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="131c3-111">Example 1</span></span>
```powershell
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

<span data-ttu-id="131c3-112">Aktualizuje tagi przestrzeni nazw \` MyNamespaceName \` na Utworzone.</span><span class="sxs-lookup"><span data-stu-id="131c3-112">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="131c3-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="131c3-113">Example 2</span></span>
```powershell
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

<span data-ttu-id="131c3-114">Aktualizacja stanu przestrzeni nazw \` MyNamespaceName przy \` użyciu funkcji AutoInflate = enabled i MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="131c3-114">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

### <span data-ttu-id="131c3-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="131c3-115">Example 3</span></span>

<span data-ttu-id="131c3-116">Aktualizuje określoną przestrzeń nazw centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="131c3-116">Updates the specified Event Hubs namespace.</span></span> <span data-ttu-id="131c3-117">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="131c3-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzEventHubNamespace -Location 'WestUS' -Name MyNamespaceName -ResourceGroupName MyResourceGroupName -SkuName Basic
```

### <span data-ttu-id="131c3-118">Przykład 5. Tworzenie i aktualizowanie przestrzeni nazw za pomocą zarządzania tożsamością w klastrze</span><span class="sxs-lookup"><span data-stu-id="131c3-118">Example 5: Creating and updating Namespace with Manage Identity in a cluster</span></span> 
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
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
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
PS C:\> $getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
$key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperty @(@($key.Name, $keyvault.VaultUri,""))

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

## <span data-ttu-id="131c3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="131c3-119">PARAMETERS</span></span>

### <span data-ttu-id="131c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="131c3-120">-DefaultProfile</span></span>
<span data-ttu-id="131c3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="131c3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="131c3-122">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="131c3-122">-EnableAutoInflate</span></span>
<span data-ttu-id="131c3-123">Wskazuje, czy funkcja Autoinflate jest włączona.</span><span class="sxs-lookup"><span data-stu-id="131c3-123">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="131c3-124">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="131c3-124">-EnableKafka</span></span>
<span data-ttu-id="131c3-125">Włączanie lub wyłączanie platformy Kafka dla przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="131c3-125">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="131c3-126">— Tożsamość</span><span class="sxs-lookup"><span data-stu-id="131c3-126">-Identity</span></span>
<span data-ttu-id="131c3-127">Włączanie lub wyłączanie tożsamości dla przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="131c3-127">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="131c3-128">-IdentityUserDefined</span><span class="sxs-lookup"><span data-stu-id="131c3-128">-IdentityUserDefined</span></span>
<span data-ttu-id="131c3-129">Tożsamość zdefiniowana przez użytkownika lub brak</span><span class="sxs-lookup"><span data-stu-id="131c3-129">User defined Identity or None</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="131c3-130">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="131c3-130">-KeyProperty</span></span>
<span data-ttu-id="131c3-131">Lista właściwości klucza, @(@(Nazwa_klucza;KeyVaultUri;Keyversion),@(Nazwa_klucza,KeyVaultUri,Keyversion))</span><span class="sxs-lookup"><span data-stu-id="131c3-131">List of Key Properties, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String[]]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="131c3-132">-KeySource</span><span class="sxs-lookup"><span data-stu-id="131c3-132">-KeySource</span></span>
<span data-ttu-id="131c3-133">Źródło kluczy</span><span class="sxs-lookup"><span data-stu-id="131c3-133">Key Source</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="131c3-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="131c3-134">-Location</span></span>
<span data-ttu-id="131c3-135">Lokalizacja przestrzeni nazw w usłudze EventHub.</span><span class="sxs-lookup"><span data-stu-id="131c3-135">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="131c3-136">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="131c3-136">-MaximumThroughputUnits</span></span>
<span data-ttu-id="131c3-137">Górny limit jednostek przepływności, gdy funkcja Autoinflate jest włączona, wartość powinna być w granicach od 0 do 20 jednostek przepływności.</span><span class="sxs-lookup"><span data-stu-id="131c3-137">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131c3-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="131c3-138">-Name</span></span>
<span data-ttu-id="131c3-139">Nazwa przestrzeni nazw aplikacji EventHub.</span><span class="sxs-lookup"><span data-stu-id="131c3-139">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="131c3-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="131c3-140">-ResourceGroupName</span></span>
<span data-ttu-id="131c3-141">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="131c3-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="131c3-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="131c3-142">-SkuCapacity</span></span>
<span data-ttu-id="131c3-143">Jednostki przepływności w aplikacji EventHub.</span><span class="sxs-lookup"><span data-stu-id="131c3-143">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="131c3-144">-SKUName</span><span class="sxs-lookup"><span data-stu-id="131c3-144">-SkuName</span></span>
<span data-ttu-id="131c3-145">Nazwa sku przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="131c3-145">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="131c3-146">— województwo</span><span class="sxs-lookup"><span data-stu-id="131c3-146">-State</span></span>
<span data-ttu-id="131c3-147">Wyłączanie/włączanie przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="131c3-147">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131c3-148">— Tag</span><span class="sxs-lookup"><span data-stu-id="131c3-148">-Tag</span></span>
<span data-ttu-id="131c3-149">Skróty reprezentujące tag zasobu.</span><span class="sxs-lookup"><span data-stu-id="131c3-149">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="131c3-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="131c3-150">-Confirm</span></span>
<span data-ttu-id="131c3-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="131c3-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="131c3-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="131c3-152">-WhatIf</span></span>
<span data-ttu-id="131c3-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="131c3-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="131c3-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="131c3-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="131c3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131c3-155">CommonParameters</span></span>
<span data-ttu-id="131c3-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="131c3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131c3-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="131c3-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131c3-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="131c3-158">INPUTS</span></span>

### <span data-ttu-id="131c3-159">System.String</span><span class="sxs-lookup"><span data-stu-id="131c3-159">System.String</span></span>

### <span data-ttu-id="131c3-160">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="131c3-160">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="131c3-161">System.Nullable'1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlet.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="131c3-161">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="131c3-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="131c3-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="131c3-163">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="131c3-163">OUTPUTS</span></span>

### <span data-ttu-id="131c3-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="131c3-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="131c3-165">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="131c3-165">NOTES</span></span>

## <span data-ttu-id="131c3-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="131c3-166">RELATED LINKS</span></span>
