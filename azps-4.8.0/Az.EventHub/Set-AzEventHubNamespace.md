---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: f13a92bef4bfbafc67beec6d99cf02d8d1d63c31
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062246"
---
# <span data-ttu-id="11c85-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="11c85-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="11c85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11c85-102">SYNOPSIS</span></span>
<span data-ttu-id="11c85-103">Umożliwia zaktualizowanie określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="11c85-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="11c85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11c85-104">SYNTAX</span></span>

### <span data-ttu-id="11c85-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="11c85-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-Identity] [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11c85-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="11c85-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity]
 [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11c85-107">IdentityUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="11c85-107">IdentityUpdateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11c85-108">Opis</span><span class="sxs-lookup"><span data-stu-id="11c85-108">DESCRIPTION</span></span>
<span data-ttu-id="11c85-109">Polecenie cmdlet Set-AzEventHubNamespace aktualizuje właściwości określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="11c85-109">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="11c85-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11c85-110">EXAMPLES</span></span>

### <span data-ttu-id="11c85-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11c85-111">Example 1</span></span>
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

<span data-ttu-id="11c85-112">Aktualizuje znaczniki obszaru nazw NamespaceName \` \` na utworzony.</span><span class="sxs-lookup"><span data-stu-id="11c85-112">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="11c85-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="11c85-113">Example 2</span></span>
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

<span data-ttu-id="11c85-114">Umożliwia zaktualizowanie stanu przestrzeni nazw obszar_nazwname \` \` za pomocą funkcji autorozdęcie = włączone i MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="11c85-114">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

### <span data-ttu-id="11c85-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="11c85-115">Example 3</span></span>

<span data-ttu-id="11c85-116">Umożliwia zaktualizowanie określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="11c85-116">Updates the specified Event Hubs namespace.</span></span> <span data-ttu-id="11c85-117">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="11c85-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzEventHubNamespace -Location 'WestUS' -Name MyNamespaceName -ResourceGroupName MyResourceGroupName -SkuName Basic
```

### <span data-ttu-id="11c85-118">Przykład 5: Tworzenie i aktualizowanie obszaru nazw za pomocą zarządzania tożsamością w klastrze</span><span class="sxs-lookup"><span data-stu-id="11c85-118">Example 5: Creating and updating Namespace with Manage Identity in a cluster</span></span> 
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

## <span data-ttu-id="11c85-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11c85-119">PARAMETERS</span></span>

### <span data-ttu-id="11c85-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c85-120">-DefaultProfile</span></span>
<span data-ttu-id="11c85-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11c85-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11c85-122">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="11c85-122">-EnableAutoInflate</span></span>
<span data-ttu-id="11c85-123">Wskazuje, czy funkcja autorozdęcie jest włączona</span><span class="sxs-lookup"><span data-stu-id="11c85-123">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="11c85-124">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="11c85-124">-EnableKafka</span></span>
<span data-ttu-id="11c85-125">Włączanie lub wyłączanie Kafka dla obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="11c85-125">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="11c85-126">-Identity (tożsamość)</span><span class="sxs-lookup"><span data-stu-id="11c85-126">-Identity</span></span>
<span data-ttu-id="11c85-127">Włączanie lub wyłączanie tożsamości obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="11c85-127">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="11c85-128">-IdentityUserDefined</span><span class="sxs-lookup"><span data-stu-id="11c85-128">-IdentityUserDefined</span></span>
<span data-ttu-id="11c85-129">Tożsamość zdefiniowana przez użytkownika lub brak</span><span class="sxs-lookup"><span data-stu-id="11c85-129">User defined Identity or None</span></span>

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

### <span data-ttu-id="11c85-130">-Właściwość</span><span class="sxs-lookup"><span data-stu-id="11c85-130">-KeyProperty</span></span>
<span data-ttu-id="11c85-131">Lista właściwości klucza, @ (@ (NazwaKlucza, KeyVaultUri, wersja klawiszowa), @ (NazwaKlucza, KeyVaultUri, wersja klawiszowa))</span><span class="sxs-lookup"><span data-stu-id="11c85-131">List of Key Properties, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span></span>

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

### <span data-ttu-id="11c85-132">-Źródło</span><span class="sxs-lookup"><span data-stu-id="11c85-132">-KeySource</span></span>
<span data-ttu-id="11c85-133">Źródło klucza</span><span class="sxs-lookup"><span data-stu-id="11c85-133">Key Source</span></span>

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

### <span data-ttu-id="11c85-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="11c85-134">-Location</span></span>
<span data-ttu-id="11c85-135">Lokalizacja obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="11c85-135">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="11c85-136">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="11c85-136">-MaximumThroughputUnits</span></span>
<span data-ttu-id="11c85-137">Górny limit jednostek przepływności, gdy funkcja podwyższanie jest włączona, wartość powinna należeć do zakresu od 0 do 20 jednostek przepływności.</span><span class="sxs-lookup"><span data-stu-id="11c85-137">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="11c85-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11c85-138">-Name</span></span>
<span data-ttu-id="11c85-139">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="11c85-139">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="11c85-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c85-140">-ResourceGroupName</span></span>
<span data-ttu-id="11c85-141">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11c85-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="11c85-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="11c85-142">-SkuCapacity</span></span>
<span data-ttu-id="11c85-143">Jednostki przepływności eventhub.</span><span class="sxs-lookup"><span data-stu-id="11c85-143">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="11c85-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="11c85-144">-SkuName</span></span>
<span data-ttu-id="11c85-145">Nazwa SKU obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="11c85-145">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="11c85-146">-State</span><span class="sxs-lookup"><span data-stu-id="11c85-146">-State</span></span>
<span data-ttu-id="11c85-147">Wyłącz/Włącz obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="11c85-147">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="11c85-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="11c85-148">-Tag</span></span>
<span data-ttu-id="11c85-149">Hashtable, które reprezentują znacznik zasobu.</span><span class="sxs-lookup"><span data-stu-id="11c85-149">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="11c85-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11c85-150">-Confirm</span></span>
<span data-ttu-id="11c85-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11c85-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11c85-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11c85-152">-WhatIf</span></span>
<span data-ttu-id="11c85-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11c85-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11c85-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="11c85-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11c85-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c85-155">CommonParameters</span></span>
<span data-ttu-id="11c85-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11c85-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c85-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11c85-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c85-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11c85-158">INPUTS</span></span>

### <span data-ttu-id="11c85-159">System. String</span><span class="sxs-lookup"><span data-stu-id="11c85-159">System.String</span></span>

### <span data-ttu-id="11c85-160">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="11c85-160">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="11c85-161">System. Nullable "1 [[Microsoft. Azure. Commands. EventHub. MODELES. NamespaceState; Microsoft. Azure. PowerShell. PowerShell. w usłudze EventHub, Version = 1.4.3.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="11c85-161">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="11c85-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="11c85-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="11c85-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11c85-163">OUTPUTS</span></span>

### <span data-ttu-id="11c85-164">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="11c85-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="11c85-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11c85-165">NOTES</span></span>

## <span data-ttu-id="11c85-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11c85-166">RELATED LINKS</span></span>
