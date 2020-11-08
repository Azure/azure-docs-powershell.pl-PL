---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: a11e962e2af6beaa3f3004cec104530f7603bb3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220702"
---
# <span data-ttu-id="d0327-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d0327-101">New-AzKeyVault</span></span>

## <span data-ttu-id="d0327-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0327-102">SYNOPSIS</span></span>
<span data-ttu-id="d0327-103">Tworzy magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0327-103">Creates a key vault.</span></span>

## <span data-ttu-id="d0327-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0327-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-DisableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0327-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0327-105">DESCRIPTION</span></span>
<span data-ttu-id="d0327-106">Polecenie cmdlet **New-AzKeyVault** tworzy magazyn kluczy w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d0327-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="d0327-107">To polecenie cmdlet udziela również uprawnień do aktualnie zalogowanego użytkownika w celu dodawania, usuwania lub list kluczy i sekretów w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0327-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="d0327-108">Uwaga: Jeśli zobaczysz błąd **, subskrypcja nie jest zarejestrowana w celu użycia obszaru nazw "Microsoft.** DataTable" podczas próby utworzenia nowego magazynu kluczy Uruchom polecenie **register-AzResourceProvider-ProviderNamespace "Microsoft.** Keying", a następnie uruchom polecenie **New-AzKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="d0327-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="d0327-109">Aby uzyskać więcej informacji, zobacz Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="d0327-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="d0327-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0327-110">EXAMPLES</span></span>

### <span data-ttu-id="d0327-111">Przykład 1. Tworzenie standardowego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="d0327-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="d0327-112">To polecenie tworzy magazyn kluczy o nazwie Contoso03Vault w obszarze Azure wschodniego USA.</span><span class="sxs-lookup"><span data-stu-id="d0327-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="d0327-113">Polecenie dodaje Magazyn kluczy do grupy zasobów o nazwie Group14.</span><span class="sxs-lookup"><span data-stu-id="d0327-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="d0327-114">Ponieważ polecenie nie określa wartości parametru *SKU* , tworzy on standardowy magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0327-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="d0327-115">Przykład 2: Tworzenie dużego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="d0327-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="d0327-116">To polecenie tworzy magazyn kluczy, podobnie jak w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="d0327-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="d0327-117">Jednak określa wartość Premium dla parametru *SKU* w celu utworzenia magazynu kluczy Premium.</span><span class="sxs-lookup"><span data-stu-id="d0327-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="d0327-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d0327-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="d0327-119">Utworzenie magazynu kluczy i określenie reguł sieciowych umożliwiających dostęp do określonego adresu IP z sieci wirtualnej określonej przez $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="d0327-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="d0327-120">`New-AzKeyVaultNetworkRuleSetObject`Aby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="d0327-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="d0327-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0327-121">PARAMETERS</span></span>

### <span data-ttu-id="d0327-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0327-122">-DefaultProfile</span></span>
<span data-ttu-id="d0327-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d0327-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0327-124">-DisableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="d0327-124">-DisableSoftDelete</span></span>
<span data-ttu-id="d0327-125">Jeśli ta opcja jest określona, funkcja "łagodne usuwanie" jest wyłączona dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0327-125">If specified, 'soft delete' functionality is disabled for this key vault.</span></span>

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

### <span data-ttu-id="d0327-126">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="d0327-126">-EnabledForDeployment</span></span>
<span data-ttu-id="d0327-127">Umożliwia dostawcy zasobów Microsoft. COMPUTE na pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się tworzenie zasobów, na przykład podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d0327-127">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0327-128">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d0327-128">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="d0327-129">Umożliwia usłudze szyfrowania dysków Azure uzyskiwanie kluczy tajnych i ich odwinięcie z tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0327-129">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0327-130">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="d0327-130">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="d0327-131">Umożliwia menedżerowi zasobów platformy Azure pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się wdrożenie szablonu.</span><span class="sxs-lookup"><span data-stu-id="d0327-131">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0327-132">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="d0327-132">-EnablePurgeProtection</span></span>
<span data-ttu-id="d0327-133">Jeśli ta opcja jest określona, ochrona przed natychmiastowe usuwaniem jest włączona dla tego magazynu; wymaga również włączenia usuwania miękkiego.</span><span class="sxs-lookup"><span data-stu-id="d0327-133">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="d0327-134">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="d0327-134">-EnableRbacAuthorization</span></span>
<span data-ttu-id="d0327-135">Jeśli ta właściwość jest określona, umożliwia autoryzację akcji danych według kontroli dostępu opartej na rolach, a następnie zasady dostępu określone we właściwościach magazynu będą ignorowane.</span><span class="sxs-lookup"><span data-stu-id="d0327-135">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="d0327-136">Pamiętaj, że akcje zarządzania są zawsze autoryzowane za pomocą RBAC.</span><span class="sxs-lookup"><span data-stu-id="d0327-136">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="d0327-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d0327-137">-Location</span></span>
<span data-ttu-id="d0327-138">Określa obszar Azure, w którym ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0327-138">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="d0327-139">Użyj polecenia [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) , aby wyświetlić wybrane opcje.</span><span class="sxs-lookup"><span data-stu-id="d0327-139">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="d0327-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0327-140">-Name</span></span>
<span data-ttu-id="d0327-141">Określa nazwę magazynu kluczy, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="d0327-141">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="d0327-142">Nazwa może być dowolną kombinacją liter, cyfr lub łączników.</span><span class="sxs-lookup"><span data-stu-id="d0327-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="d0327-143">Nazwa musi zaczynać się i kończyć literą lub cyfrą.</span><span class="sxs-lookup"><span data-stu-id="d0327-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="d0327-144">Nazwa musi być uniwersalnie unikatowa.</span><span class="sxs-lookup"><span data-stu-id="d0327-144">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0327-145">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0327-145">-NetworkRuleSet</span></span>
<span data-ttu-id="d0327-146">Określa zestaw reguł sieci magazynu.</span><span class="sxs-lookup"><span data-stu-id="d0327-146">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="d0327-147">Decyduje o ułatwieniach dostępu do magazynu kluczy z konkretnych lokalizacji sieciowych.</span><span class="sxs-lookup"><span data-stu-id="d0327-147">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="d0327-148">Utworzona przez `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="d0327-148">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0327-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0327-149">-ResourceGroupName</span></span>
<span data-ttu-id="d0327-150">Określa nazwę istniejącej grupy zasobów, w której ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0327-150">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0327-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="d0327-151">-Sku</span></span>
<span data-ttu-id="d0327-152">Określa jednostkę SKU wystąpienia magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0327-152">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="d0327-153">Aby uzyskać informacje o tym, jakie funkcje są dostępne dla poszczególnych wersji SKU, zobacz witrynę sieci Web usługi Azure Key (cennik) https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="d0327-153">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0327-154">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d0327-154">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="d0327-155">Określa, jak długo usunięte zasoby są zachowywane, oraz jak długo można przeczyścić magazyn lub obiekt w stanie usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d0327-155">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="d0327-156">Wartość domyślna to 90 dni.</span><span class="sxs-lookup"><span data-stu-id="d0327-156">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0327-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="d0327-157">-Tag</span></span>
<span data-ttu-id="d0327-158">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d0327-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d0327-159">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d0327-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0327-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0327-160">-Confirm</span></span>
<span data-ttu-id="d0327-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0327-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0327-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0327-162">-WhatIf</span></span>
<span data-ttu-id="d0327-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0327-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0327-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d0327-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0327-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0327-165">CommonParameters</span></span>
<span data-ttu-id="d0327-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0327-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0327-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0327-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0327-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0327-168">INPUTS</span></span>

### <span data-ttu-id="d0327-169">System. String</span><span class="sxs-lookup"><span data-stu-id="d0327-169">System.String</span></span>

### <span data-ttu-id="d0327-170">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d0327-170">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d0327-171">Microsoft. Azure. Management. DataModel. modele. SkuName</span><span class="sxs-lookup"><span data-stu-id="d0327-171">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="d0327-172">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d0327-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d0327-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0327-173">OUTPUTS</span></span>

### <span data-ttu-id="d0327-174">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d0327-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="d0327-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0327-175">NOTES</span></span>

## <span data-ttu-id="d0327-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0327-176">RELATED LINKS</span></span>

[<span data-ttu-id="d0327-177">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d0327-177">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="d0327-178">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d0327-178">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
