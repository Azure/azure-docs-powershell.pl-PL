---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c415a7b80609a9e8794df183b2ae1cea73a7f1cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192362"
---
# <span data-ttu-id="30349-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30349-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="30349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30349-102">SYNOPSIS</span></span>
<span data-ttu-id="30349-103">Usuwa zarządzane konto magazynu platformy Azure i wszystkie skojarzone definicje sas.</span><span class="sxs-lookup"><span data-stu-id="30349-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="30349-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="30349-104">SYNTAX</span></span>

### <span data-ttu-id="30349-105">ByDefinitionName (Default)</span><span class="sxs-lookup"><span data-stu-id="30349-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30349-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="30349-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30349-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="30349-107">DESCRIPTION</span></span>
<span data-ttu-id="30349-108">Nie kojarzy konta magazynu platformy Azure z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="30349-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="30349-109">Nie spowoduje to usunięcia konta magazynu platformy Azure, ale usunie klucze konta z zarządzania przez magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="30349-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="30349-110">Usuwane są również wszystkie skojarzone definicje SAS magazynu zarządzanego przez magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="30349-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="30349-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="30349-111">EXAMPLES</span></span>

### <span data-ttu-id="30349-112">Przykład 1. Usuwanie zarządzanego konta magazynu platformy Azure i wszystkich skojarzonych definicji sas.</span><span class="sxs-lookup"><span data-stu-id="30349-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="30349-113">Przestaje skojarzyć "mystorageaccount" konta magazynu platformy Azure z magazynu kluczy "myvault" i zatrzymuje zarządzanie jego kluczami przez magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="30349-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="30349-114">Konto "mystorageaccount" nie zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="30349-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="30349-115">Wszystkie definicje SAS magazynu zarządzanego przez magazyn kluczy skojarzone z tym kontem zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="30349-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="30349-116">Przykład 2. Usuwanie zarządzanego konta magazynu platformy Azure i wszystkich skojarzonych definicji SAS bez potwierdzenia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="30349-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="30349-117">Przestaje skojarzyć "mystorageaccount" konta magazynu platformy Azure z magazynu kluczy "myvault" i zatrzymuje zarządzanie jego kluczami przez magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="30349-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="30349-118">Konto "mystorageaccount" nie zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="30349-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="30349-119">Wszystkie definicje SAS magazynu zarządzanego przez magazyn kluczy skojarzone z tym kontem zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="30349-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="30349-120">Przykład 3. Trwałe usuwanie (czyszczenie) zarządzanego konta magazynu platformy Azure i wszystkich skojarzonych definicji sas z magazynu z włączoną obsługą "miękkiego usuwania".</span><span class="sxs-lookup"><span data-stu-id="30349-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="30349-121">W tym przykładzie przyjęto założenie, że dla tego magazynu włączono funkcję "miękkiego usuwania".</span><span class="sxs-lookup"><span data-stu-id="30349-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="30349-122">Sprawdź, czy tak jest, analizując właściwości magazynu lub atrybut RecoveryLevel encji w magazynie.</span><span class="sxs-lookup"><span data-stu-id="30349-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="30349-123">Pierwsze polecenie cmdlet przestaje skojarzyć "mystorageaccount" konta magazynu platformy Azure z magazynu kluczy "myvault" i zatrzymuje zarządzanie jego kluczami przez magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="30349-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="30349-124">Konto "mystorageaccount" nie zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="30349-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="30349-125">Wszystkie definicje SAS magazynu zarządzanego przez magazyn kluczy skojarzone z tym kontem zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="30349-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="30349-126">Drugie polecenie cmdlet sprawdza, czy konto magazynu znajduje się w usuniętym, ale odzyskiwalnym stanie.</span><span class="sxs-lookup"><span data-stu-id="30349-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="30349-127">Osiągnięcie tego stanu może wymagać pewnego czasu, przed podjęciem próby należy zezwolić na ~30s.</span><span class="sxs-lookup"><span data-stu-id="30349-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="30349-128">Trzecie polecenie cmdlet trwale usuwa konto magazynu — odzyskiwanie nie będzie już możliwe.</span><span class="sxs-lookup"><span data-stu-id="30349-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="30349-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30349-129">PARAMETERS</span></span>

### <span data-ttu-id="30349-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="30349-130">-AccountName</span></span>
<span data-ttu-id="30349-131">Nazwa konta magazynu zarządzanego przez magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="30349-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="30349-132">Polecenie cmdlet konstruuje nazwę FQDN zarządzanego konta magazynu z nazwy magazynu, obecnie wybranego środowiska i nazwy konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="30349-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30349-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30349-133">-DefaultProfile</span></span>
<span data-ttu-id="30349-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="30349-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30349-135">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="30349-135">-Force</span></span>
<span data-ttu-id="30349-136">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="30349-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="30349-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30349-137">-InputObject</span></span>
<span data-ttu-id="30349-138">Obiekt ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="30349-138">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30349-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="30349-139">-InRemovedState</span></span>
<span data-ttu-id="30349-140">Trwałe usuwanie poprzednio usuniętego konta zarządzanego magazynu.</span><span class="sxs-lookup"><span data-stu-id="30349-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="30349-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30349-141">-PassThru</span></span>
<span data-ttu-id="30349-142">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="30349-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="30349-143">Jeśli ten przełącznik zostanie określony, polecenie cmdlet zwróci usunięte konto magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="30349-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="30349-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="30349-144">-VaultName</span></span>
<span data-ttu-id="30349-145">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="30349-145">Vault name.</span></span>
<span data-ttu-id="30349-146">Polecenie cmdlet konstruuje nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="30349-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30349-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30349-147">-Confirm</span></span>
<span data-ttu-id="30349-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="30349-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30349-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30349-149">-WhatIf</span></span>
<span data-ttu-id="30349-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30349-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30349-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="30349-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30349-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30349-152">CommonParameters</span></span>
<span data-ttu-id="30349-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30349-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30349-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30349-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30349-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30349-155">INPUTS</span></span>

### <span data-ttu-id="30349-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="30349-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="30349-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30349-157">OUTPUTS</span></span>

### <span data-ttu-id="30349-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30349-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="30349-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="30349-159">NOTES</span></span>

## <span data-ttu-id="30349-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30349-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

