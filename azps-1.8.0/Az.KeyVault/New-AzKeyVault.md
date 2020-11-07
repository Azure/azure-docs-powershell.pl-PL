---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 08f3b7ebaa7b1bc07bdac10b5b7cc16cb4405534
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867963"
---
# <span data-ttu-id="12fd9-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="12fd9-101">New-AzKeyVault</span></span>

## <span data-ttu-id="12fd9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="12fd9-103">Tworzy magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="12fd9-103">Creates a key vault.</span></span>

## <span data-ttu-id="12fd9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12fd9-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-EnablePurgeProtection]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12fd9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="12fd9-105">DESCRIPTION</span></span>
<span data-ttu-id="12fd9-106">Polecenie cmdlet **New-AzKeyVault** tworzy magazyn kluczy w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="12fd9-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="12fd9-107">To polecenie cmdlet udziela również uprawnień do aktualnie zalogowanego użytkownika w celu dodawania, usuwania lub list kluczy i sekretów w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="12fd9-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="12fd9-108">Uwaga: Jeśli zobaczysz błąd **, subskrypcja nie jest zarejestrowana w celu użycia obszaru nazw "Microsoft.** DataTable" podczas próby utworzenia nowego magazynu kluczy Uruchom polecenie **register-AzResourceProvider-ProviderNamespace "Microsoft.** Keying", a następnie uruchom polecenie **New-AzKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="12fd9-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="12fd9-109">Aby uzyskać więcej informacji, zobacz Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="12fd9-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="12fd9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12fd9-110">EXAMPLES</span></span>

### <span data-ttu-id="12fd9-111">Przykład 1. Tworzenie standardowego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="12fd9-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="12fd9-112">To polecenie tworzy magazyn kluczy o nazwie Contoso03Vault w obszarze Azure wschodniego USA.</span><span class="sxs-lookup"><span data-stu-id="12fd9-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="12fd9-113">Polecenie dodaje Magazyn kluczy do grupy zasobów o nazwie Group14.</span><span class="sxs-lookup"><span data-stu-id="12fd9-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="12fd9-114">Ponieważ polecenie nie określa wartości parametru *SKU* , tworzy on standardowy magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="12fd9-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="12fd9-115">Przykład 2: Tworzenie dużego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="12fd9-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="12fd9-116">To polecenie tworzy magazyn kluczy, podobnie jak w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="12fd9-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="12fd9-117">Jednak określa wartość Premium dla parametru *SKU* w celu utworzenia magazynu kluczy Premium.</span><span class="sxs-lookup"><span data-stu-id="12fd9-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="12fd9-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12fd9-118">PARAMETERS</span></span>

### <span data-ttu-id="12fd9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12fd9-119">-DefaultProfile</span></span>
<span data-ttu-id="12fd9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="12fd9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12fd9-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="12fd9-121">-EnabledForDeployment</span></span>
<span data-ttu-id="12fd9-122">Umożliwia dostawcy zasobów Microsoft. COMPUTE na pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się tworzenie zasobów, na przykład podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="12fd9-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="12fd9-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="12fd9-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="12fd9-124">Umożliwia usłudze szyfrowania dysków Azure uzyskiwanie kluczy tajnych i ich odwinięcie z tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="12fd9-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="12fd9-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="12fd9-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="12fd9-126">Umożliwia menedżerowi zasobów platformy Azure pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się wdrożenie szablonu.</span><span class="sxs-lookup"><span data-stu-id="12fd9-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="12fd9-127">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="12fd9-127">-EnablePurgeProtection</span></span>
<span data-ttu-id="12fd9-128">Jeśli ta opcja jest określona, ochrona przed natychmiastowe usuwaniem jest włączona dla tego magazynu; wymaga również włączenia usuwania miękkiego.</span><span class="sxs-lookup"><span data-stu-id="12fd9-128">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="12fd9-129">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="12fd9-129">-EnableSoftDelete</span></span>
<span data-ttu-id="12fd9-130">Określa, że funkcja soft-DELETE jest włączona dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="12fd9-130">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="12fd9-131">Jeśli funkcja usuwania nietrwałego jest włączona, w okresie prolongaty możesz odzyskać ten magazyn kluczy wraz z jego zawartością po jego usunięciu.</span><span class="sxs-lookup"><span data-stu-id="12fd9-131">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>
<span data-ttu-id="12fd9-132">Aby uzyskać więcej informacji na temat tej funkcji, zobacz programowy [Magazyn kluczy Azure — omówienie usuwania](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span><span class="sxs-lookup"><span data-stu-id="12fd9-132">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="12fd9-133">Aby uzyskać instrukcje, zobacz [Korzystanie z programu PowerShell w celu korzystania z magazynu kluczy](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span><span class="sxs-lookup"><span data-stu-id="12fd9-133">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

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

### <span data-ttu-id="12fd9-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="12fd9-134">-Location</span></span>
<span data-ttu-id="12fd9-135">Określa obszar Azure, w którym ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="12fd9-135">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="12fd9-136">Użyj polecenia [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) , aby wyświetlić wybrane opcje.</span><span class="sxs-lookup"><span data-stu-id="12fd9-136">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="12fd9-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="12fd9-137">-Name</span></span>
<span data-ttu-id="12fd9-138">Określa nazwę magazynu kluczy, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="12fd9-138">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="12fd9-139">Nazwa może być dowolną kombinacją liter, cyfr lub łączników.</span><span class="sxs-lookup"><span data-stu-id="12fd9-139">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="12fd9-140">Nazwa musi zaczynać się i kończyć literą lub cyfrą.</span><span class="sxs-lookup"><span data-stu-id="12fd9-140">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="12fd9-141">Nazwa musi być uniwersalnie unikatowa.</span><span class="sxs-lookup"><span data-stu-id="12fd9-141">The name must be universally unique.</span></span>

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

### <span data-ttu-id="12fd9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12fd9-142">-ResourceGroupName</span></span>
<span data-ttu-id="12fd9-143">Określa nazwę istniejącej grupy zasobów, w której ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="12fd9-143">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="12fd9-144">-SKU</span><span class="sxs-lookup"><span data-stu-id="12fd9-144">-Sku</span></span>
<span data-ttu-id="12fd9-145">Określa jednostkę SKU wystąpienia magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="12fd9-145">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="12fd9-146">Aby uzyskać informacje o tym, jakie funkcje są dostępne dla poszczególnych wersji SKU, zobacz witrynę sieci Web usługi Azure Key (cennik) https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="12fd9-146">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="12fd9-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="12fd9-147">-Tag</span></span>
<span data-ttu-id="12fd9-148">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="12fd9-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="12fd9-149">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="12fd9-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="12fd9-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12fd9-150">-Confirm</span></span>
<span data-ttu-id="12fd9-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12fd9-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12fd9-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12fd9-152">-WhatIf</span></span>
<span data-ttu-id="12fd9-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12fd9-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12fd9-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12fd9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12fd9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12fd9-155">CommonParameters</span></span>
<span data-ttu-id="12fd9-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12fd9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12fd9-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12fd9-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12fd9-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12fd9-158">INPUTS</span></span>

### <span data-ttu-id="12fd9-159">System. String</span><span class="sxs-lookup"><span data-stu-id="12fd9-159">System.String</span></span>

### <span data-ttu-id="12fd9-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="12fd9-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="12fd9-161">Microsoft. Azure. Management. DataModel. modele. SkuName</span><span class="sxs-lookup"><span data-stu-id="12fd9-161">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="12fd9-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="12fd9-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="12fd9-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12fd9-163">OUTPUTS</span></span>

### <span data-ttu-id="12fd9-164">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="12fd9-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="12fd9-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12fd9-165">NOTES</span></span>

## <span data-ttu-id="12fd9-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12fd9-166">RELATED LINKS</span></span>

[<span data-ttu-id="12fd9-167">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="12fd9-167">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="12fd9-168">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="12fd9-168">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
