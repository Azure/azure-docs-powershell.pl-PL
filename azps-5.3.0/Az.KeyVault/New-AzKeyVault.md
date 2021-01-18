---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 0da8ce1e7da509c140e5893240fadb37d7852ad8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499069"
---
# <span data-ttu-id="88558-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="88558-101">New-AzKeyVault</span></span>

## <span data-ttu-id="88558-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88558-102">SYNOPSIS</span></span>
<span data-ttu-id="88558-103">Tworzy magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="88558-103">Creates a key vault.</span></span>

## <span data-ttu-id="88558-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88558-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88558-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88558-105">DESCRIPTION</span></span>
<span data-ttu-id="88558-106">Polecenie cmdlet **New-AzKeyVault** tworzy magazyn kluczy w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="88558-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="88558-107">To polecenie cmdlet udziela również uprawnień do aktualnie zalogowanego użytkownika w celu dodawania, usuwania lub list kluczy i sekretów w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="88558-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="88558-108">Uwaga: Jeśli zobaczysz błąd **, subskrypcja nie jest zarejestrowana w celu użycia obszaru nazw "Microsoft.** DataTable" podczas próby utworzenia nowego magazynu kluczy Uruchom polecenie **register-AzResourceProvider-ProviderNamespace "Microsoft.** Keying", a następnie uruchom polecenie **New-AzKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="88558-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="88558-109">Aby uzyskać więcej informacji, zobacz Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="88558-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="88558-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88558-110">EXAMPLES</span></span>

### <span data-ttu-id="88558-111">Przykład 1. Tworzenie standardowego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="88558-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="88558-112">To polecenie tworzy magazyn kluczy o nazwie Contoso03Vault w obszarze Azure wschodniego USA.</span><span class="sxs-lookup"><span data-stu-id="88558-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="88558-113">Polecenie dodaje Magazyn kluczy do grupy zasobów o nazwie Group14.</span><span class="sxs-lookup"><span data-stu-id="88558-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="88558-114">Ponieważ polecenie nie określa wartości parametru *SKU* , tworzy on standardowy magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="88558-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="88558-115">Przykład 2: Tworzenie dużego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="88558-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="88558-116">To polecenie tworzy magazyn kluczy, podobnie jak w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="88558-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="88558-117">Jednak określa wartość Premium dla parametru *SKU* w celu utworzenia magazynu kluczy Premium.</span><span class="sxs-lookup"><span data-stu-id="88558-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="88558-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="88558-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="88558-119">Utworzenie magazynu kluczy i określenie reguł sieciowych umożliwiających dostęp do określonego adresu IP z sieci wirtualnej określonej przez $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="88558-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="88558-120">`New-AzKeyVaultNetworkRuleSetObject`Aby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="88558-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="88558-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88558-121">PARAMETERS</span></span>

### <span data-ttu-id="88558-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88558-122">-DefaultProfile</span></span>
<span data-ttu-id="88558-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="88558-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88558-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="88558-124">-EnabledForDeployment</span></span>
<span data-ttu-id="88558-125">Umożliwia dostawcy zasobów Microsoft. COMPUTE na pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się tworzenie zasobów, na przykład podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="88558-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="88558-126">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="88558-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="88558-127">Umożliwia usłudze szyfrowania dysków Azure uzyskiwanie kluczy tajnych i ich odwinięcie z tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="88558-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="88558-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="88558-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="88558-129">Umożliwia menedżerowi zasobów platformy Azure pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się wdrożenie szablonu.</span><span class="sxs-lookup"><span data-stu-id="88558-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="88558-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="88558-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="88558-131">Jeśli ta opcja jest określona, ochrona przed natychmiastowe usuwaniem jest włączona dla tego magazynu; wymaga również włączenia usuwania miękkiego.</span><span class="sxs-lookup"><span data-stu-id="88558-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="88558-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="88558-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="88558-133">Jeśli ta właściwość jest określona, umożliwia autoryzację akcji danych według kontroli dostępu opartej na rolach, a następnie zasady dostępu określone we właściwościach magazynu będą ignorowane.</span><span class="sxs-lookup"><span data-stu-id="88558-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="88558-134">Pamiętaj, że akcje zarządzania są zawsze autoryzowane za pomocą RBAC.</span><span class="sxs-lookup"><span data-stu-id="88558-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="88558-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="88558-135">-Location</span></span>
<span data-ttu-id="88558-136">Określa obszar Azure, w którym ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="88558-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="88558-137">Użyj polecenia [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) , aby wyświetlić wybrane opcje.</span><span class="sxs-lookup"><span data-stu-id="88558-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="88558-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88558-138">-Name</span></span>
<span data-ttu-id="88558-139">Określa nazwę magazynu kluczy, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="88558-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="88558-140">Nazwa może być dowolną kombinacją liter, cyfr lub łączników.</span><span class="sxs-lookup"><span data-stu-id="88558-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="88558-141">Nazwa musi zaczynać się i kończyć literą lub cyfrą.</span><span class="sxs-lookup"><span data-stu-id="88558-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="88558-142">Nazwa musi być uniwersalnie unikatowa.</span><span class="sxs-lookup"><span data-stu-id="88558-142">The name must be universally unique.</span></span>

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

### <span data-ttu-id="88558-143">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="88558-143">-NetworkRuleSet</span></span>
<span data-ttu-id="88558-144">Określa zestaw reguł sieci magazynu.</span><span class="sxs-lookup"><span data-stu-id="88558-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="88558-145">Decyduje o ułatwieniach dostępu do magazynu kluczy z konkretnych lokalizacji sieciowych.</span><span class="sxs-lookup"><span data-stu-id="88558-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="88558-146">Utworzona przez `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="88558-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

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

### <span data-ttu-id="88558-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88558-147">-ResourceGroupName</span></span>
<span data-ttu-id="88558-148">Określa nazwę istniejącej grupy zasobów, w której ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="88558-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="88558-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="88558-149">-Sku</span></span>
<span data-ttu-id="88558-150">Określa jednostkę SKU wystąpienia magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="88558-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="88558-151">Aby uzyskać informacje o tym, jakie funkcje są dostępne dla poszczególnych wersji SKU, zobacz witrynę sieci Web usługi Azure Key (cennik) https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="88558-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88558-152">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="88558-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="88558-153">Określa, jak długo usunięte zasoby są zachowywane, oraz jak długo można przeczyścić magazyn lub obiekt w stanie usunięcia.</span><span class="sxs-lookup"><span data-stu-id="88558-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="88558-154">Wartość domyślna to 90 dni.</span><span class="sxs-lookup"><span data-stu-id="88558-154">The default is 90 days.</span></span>

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

### <span data-ttu-id="88558-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="88558-155">-Tag</span></span>
<span data-ttu-id="88558-156">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="88558-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="88558-157">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="88558-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="88558-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88558-158">-Confirm</span></span>
<span data-ttu-id="88558-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88558-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88558-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88558-160">-WhatIf</span></span>
<span data-ttu-id="88558-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88558-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88558-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88558-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88558-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88558-163">CommonParameters</span></span>
<span data-ttu-id="88558-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88558-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88558-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88558-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88558-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88558-166">INPUTS</span></span>

### <span data-ttu-id="88558-167">System. String</span><span class="sxs-lookup"><span data-stu-id="88558-167">System.String</span></span>

### <span data-ttu-id="88558-168">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="88558-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="88558-169">Microsoft. Azure. Management. DataModel. modele. SkuName</span><span class="sxs-lookup"><span data-stu-id="88558-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="88558-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="88558-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="88558-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88558-171">OUTPUTS</span></span>

### <span data-ttu-id="88558-172">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="88558-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="88558-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88558-173">NOTES</span></span>

## <span data-ttu-id="88558-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88558-174">RELATED LINKS</span></span>

[<span data-ttu-id="88558-175">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="88558-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="88558-176">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="88558-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
