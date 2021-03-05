---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 6af82533540bd93b90847c51b9aaf0bd603dc727
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001377"
---
# <span data-ttu-id="e4e22-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="e4e22-101">New-AzKeyVault</span></span>

## <span data-ttu-id="e4e22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4e22-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e22-103">Tworzy magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="e4e22-103">Creates a key vault.</span></span>

## <span data-ttu-id="e4e22-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e4e22-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4e22-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e4e22-105">DESCRIPTION</span></span>
<span data-ttu-id="e4e22-106">Polecenie **cmdlet New-AzKeyVault** tworzy magazyn kluczy w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4e22-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="e4e22-107">To polecenie cmdlet udziela również uprawnień obecnie zalogowanego użytkownika do dodawania, usuwania lub list kluczy i tajemnic w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="e4e22-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="e4e22-108">Uwaga: Jeśli zostanie wyświetlony błąd Subskrypcji nie zarejestrowano w celu używania przestrzeni nazw **"Microsoft.KeyVault"** podczas próby utworzenia nowego magazynu kluczy, uruchom polecenie **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault",** a następnie uruchom ponownie polecenie **New-AzKeyVault.**</span><span class="sxs-lookup"><span data-stu-id="e4e22-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="e4e22-109">Aby uzyskać więcej informacji, zobacz Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="e4e22-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="e4e22-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e4e22-110">EXAMPLES</span></span>

### <span data-ttu-id="e4e22-111">Przykład 1. Tworzenie standardowego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="e4e22-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="e4e22-112">To polecenie tworzy magazyn kluczy o nazwie Contoso03Vault w regionie Azure — Wschód USA.</span><span class="sxs-lookup"><span data-stu-id="e4e22-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="e4e22-113">To polecenie dodaje magazyn kluczy do grupy zasobów o nazwie Grupa14.</span><span class="sxs-lookup"><span data-stu-id="e4e22-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="e4e22-114">Ponieważ to polecenie nie określa wartości dla parametru *SKU,* tworzy ono standardowy magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="e4e22-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="e4e22-115">Przykład 2. Tworzenie magazynu kluczy premium</span><span class="sxs-lookup"><span data-stu-id="e4e22-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="e4e22-116">To polecenie tworzy magazyn kluczy, podobnie jak w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="e4e22-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="e4e22-117">Jednak określa wartość premium dla parametru *SKU* w celu utworzenia magazynu kluczy Premium.</span><span class="sxs-lookup"><span data-stu-id="e4e22-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="e4e22-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e4e22-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="e4e22-119">Tworzenie magazynu kluczy i określa reguły sieciowe umożliwiające dostęp do określonego adresu IP z sieci wirtualnej wskazanej przez $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="e4e22-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="e4e22-120">Aby `New-AzKeyVaultNetworkRuleSetObject` uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="e4e22-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="e4e22-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4e22-121">PARAMETERS</span></span>

### <span data-ttu-id="e4e22-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e22-122">-DefaultProfile</span></span>
<span data-ttu-id="e4e22-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e4e22-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4e22-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="e4e22-124">-EnabledForDeployment</span></span>
<span data-ttu-id="e4e22-125">Umożliwia dostawcy zasobów Microsoft.Compute pobieranie sekretów z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się podczas tworzenia zasobów, na przykład podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e4e22-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="e4e22-126">-EnabledForScriptEncryption</span><span class="sxs-lookup"><span data-stu-id="e4e22-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="e4e22-127">Umożliwia usłudze szyfrowania dysków Platformy Azure uzyskiwanie sekretów i odłącza klucze z tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e4e22-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="e4e22-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="e4e22-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="e4e22-129">Umożliwia usłudze Azure Resource Manager uzyskiwanie sekretów z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się we wdrożeniu szablonu.</span><span class="sxs-lookup"><span data-stu-id="e4e22-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="e4e22-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="e4e22-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="e4e22-131">Jeśli jest określona, dla tego magazynu jest włączona ochrona przed natychmiastowym usunięciem. wymaga również włączonego "miękkiego usunięcia".</span><span class="sxs-lookup"><span data-stu-id="e4e22-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="e4e22-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="e4e22-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="e4e22-133">Jeśli jest to określone, umożliwia autoryzowanie akcji danych za pomocą kontroli dostępu opartej na rolach (RBAC, Role Based Access Control), a następnie zasady dostępu określone we właściwościach magazynu będą ignorowane.</span><span class="sxs-lookup"><span data-stu-id="e4e22-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="e4e22-134">Pamiętaj, że akcje zarządzania są zawsze autoryzowane przy użyciu RBAC.</span><span class="sxs-lookup"><span data-stu-id="e4e22-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="e4e22-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e4e22-135">-Location</span></span>
<span data-ttu-id="e4e22-136">Określa region platformy Azure, w którym ma być tworzyć magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="e4e22-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="e4e22-137">Użyj polecenia [Get-AzLocation,](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) aby wyświetlić dostępne opcje.</span><span class="sxs-lookup"><span data-stu-id="e4e22-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="e4e22-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e4e22-138">-Name</span></span>
<span data-ttu-id="e4e22-139">Określa nazwę magazynu kluczy do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="e4e22-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="e4e22-140">Nazwa może być dowolną kombinacją liter, cyfr lub łączników.</span><span class="sxs-lookup"><span data-stu-id="e4e22-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="e4e22-141">Nazwa musi zaczynać się i kończyć literą lub cyfrą.</span><span class="sxs-lookup"><span data-stu-id="e4e22-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="e4e22-142">Nazwa musi być unikatowa.</span><span class="sxs-lookup"><span data-stu-id="e4e22-142">The name must be universally unique.</span></span>

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

### <span data-ttu-id="e4e22-143">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e4e22-143">-NetworkRuleSet</span></span>
<span data-ttu-id="e4e22-144">Określa zestaw reguł sieciowych dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="e4e22-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="e4e22-145">Podlega on ułatwień dostępu magazynu kluczy z określonych lokalizacji sieciowych.</span><span class="sxs-lookup"><span data-stu-id="e4e22-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="e4e22-146">Utworzone `New-AzKeyVaultNetworkRuleSetObject` przez.</span><span class="sxs-lookup"><span data-stu-id="e4e22-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

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

### <span data-ttu-id="e4e22-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4e22-147">-ResourceGroupName</span></span>
<span data-ttu-id="e4e22-148">Określa nazwę istniejącej grupy zasobów, w której ma być tworzyć magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="e4e22-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="e4e22-149">- SKU</span><span class="sxs-lookup"><span data-stu-id="e4e22-149">-Sku</span></span>
<span data-ttu-id="e4e22-150">Określa sku wystąpienia magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e4e22-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="e4e22-151">Aby uzyskać informacje o funkcjach dostępnych dla poszczególnych wersji SKU, zobacz witrynę internetową Ceny magazynu kluczy platformy Azure https://go.microsoft.com/fwlink/?linkid=512521) (.</span><span class="sxs-lookup"><span data-stu-id="e4e22-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="e4e22-152">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e4e22-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="e4e22-153">Określa czas zachowywania usuniętych zasobów oraz czas, przez jaki można przeczyścić magazyn lub obiekt w stanie usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e4e22-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="e4e22-154">Wartość domyślna to 90 dni.</span><span class="sxs-lookup"><span data-stu-id="e4e22-154">The default is 90 days.</span></span>

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

### <span data-ttu-id="e4e22-155">— Tag</span><span class="sxs-lookup"><span data-stu-id="e4e22-155">-Tag</span></span>
<span data-ttu-id="e4e22-156">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="e4e22-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e4e22-157">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="e4e22-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e4e22-158">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4e22-158">-Confirm</span></span>
<span data-ttu-id="e4e22-159">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e4e22-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4e22-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4e22-160">-WhatIf</span></span>
<span data-ttu-id="e4e22-161">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4e22-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4e22-162">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e4e22-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4e22-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e22-163">CommonParameters</span></span>
<span data-ttu-id="e4e22-164">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e22-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e22-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4e22-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e22-166">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4e22-166">INPUTS</span></span>

### <span data-ttu-id="e4e22-167">System.String</span><span class="sxs-lookup"><span data-stu-id="e4e22-167">System.String</span></span>

### <span data-ttu-id="e4e22-168">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e4e22-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e4e22-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span><span class="sxs-lookup"><span data-stu-id="e4e22-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="e4e22-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e4e22-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e4e22-171">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4e22-171">OUTPUTS</span></span>

### <span data-ttu-id="e4e22-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e4e22-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="e4e22-173">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e4e22-173">NOTES</span></span>

## <span data-ttu-id="e4e22-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4e22-174">RELATED LINKS</span></span>

[<span data-ttu-id="e4e22-175">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="e4e22-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="e4e22-176">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="e4e22-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
