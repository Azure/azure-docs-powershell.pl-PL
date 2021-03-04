---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 05c744050cc377eda01e309fb30122f83b9a8f5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007866"
---
# <span data-ttu-id="252d4-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="252d4-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="252d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="252d4-102">SYNOPSIS</span></span>
<span data-ttu-id="252d4-103">Dodaje istniejące konto magazynu platformy Azure do określonego magazynu kluczy, aby jego klucze zostały zarządzane przez usługę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="252d4-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="252d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="252d4-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="252d4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="252d4-105">DESCRIPTION</span></span>
<span data-ttu-id="252d4-106">Konfiguruje istniejące konto magazynu platformy Azure z magazynem kluczy dla kluczy konta magazynu, które ma być zarządzane przez magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="252d4-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="252d4-107">Konto magazynu musi już istnieć.</span><span class="sxs-lookup"><span data-stu-id="252d4-107">The Storage Account must already exist.</span></span> <span data-ttu-id="252d4-108">Klucze magazynu nigdy nie są udostępniane dzwoniącemu.</span><span class="sxs-lookup"><span data-stu-id="252d4-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="252d4-109">Magazyn kluczy automatycznie ponownie generuje i przełącza klucz aktywny na podstawie okresu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="252d4-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="252d4-110">Aby uzyskać omówienie tej funkcji, zobacz konto zarządzanego magazynu kluczy platformy [Azure — program PowerShell.](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell)</span><span class="sxs-lookup"><span data-stu-id="252d4-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="252d4-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="252d4-111">EXAMPLES</span></span>

### <span data-ttu-id="252d4-112">Przykład 1. Ustawianie konta magazynu platformy Azure z magazynem kluczy w celu zarządzania jego kluczami</span><span class="sxs-lookup"><span data-stu-id="252d4-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $storage = Get-AzStorageAccount -ResourceGroupName "mystorageResourceGroup" -StorageAccountName "mystorage"
PS C:\> $servicePrincipal = Get-AzADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
PS C:\> New-AzRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope $storage.Id
PS C:\> $userPrincipalId = $(Get-AzADUser -SearchString "developer@contoso.com").Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName $keyVaultName -ObjectId $userPrincipalId -PermissionsToStorage get, set
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="252d4-113">Ustawia konto magazynu z magazynem kluczy, aby jego kluczami zarządzał magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="252d4-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="252d4-114">Zestaw aktywnych klawiszy to "klucz1".</span><span class="sxs-lookup"><span data-stu-id="252d4-114">The active key set is 'key1'.</span></span> <span data-ttu-id="252d4-115">Ten klucz będzie używany do generowania tokenów sas.</span><span class="sxs-lookup"><span data-stu-id="252d4-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="252d4-116">Magazyn kluczy ponownie wygeneruje klucz "klucz2" po okresie przerwy od czasu tego polecenia i ustawi go jako klucz aktywny.</span><span class="sxs-lookup"><span data-stu-id="252d4-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="252d4-117">Ten proces automatycznego przetwarzania będzie kontynuowany między wartościami "key1" i "key2" z odstępem 90 dni.</span><span class="sxs-lookup"><span data-stu-id="252d4-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="252d4-118">Przykład 2. Ustawianie klasycznego konta magazynu platformy Azure z magazynem kluczy w celu zarządzania jego kluczami</span><span class="sxs-lookup"><span data-stu-id="252d4-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myvault/providers/Microsoft.Cl
                      assicStorage/storageAccounts/mystorageaccount
Active Key Name     : Primary
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="252d4-119">Ustawia klasyczne konto magazynu z magazynem kluczy, aby jego kluczami zarządzał magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="252d4-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="252d4-120">Zestaw kluczy aktywnych to "Podstawowy".</span><span class="sxs-lookup"><span data-stu-id="252d4-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="252d4-121">Ten klucz będzie używany do generowania tokenów sas.</span><span class="sxs-lookup"><span data-stu-id="252d4-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="252d4-122">Magazyn kluczy ponownie wygeneruje klucz pomocniczy po okresie aktywności od czasu tego polecenia i ustawi go jako klucz aktywny.</span><span class="sxs-lookup"><span data-stu-id="252d4-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="252d4-123">Ten proces automatycznego przetwarzania będzie kontynuowany między ustawieniami "Podstawowy" i "Pomocniczy" z przerwą 90-dniową.</span><span class="sxs-lookup"><span data-stu-id="252d4-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="252d4-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="252d4-124">PARAMETERS</span></span>

### <span data-ttu-id="252d4-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="252d4-125">-AccountName</span></span>
<span data-ttu-id="252d4-126">Nazwa konta magazynu zarządzanego przez magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="252d4-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="252d4-127">Polecenie cmdlet konstruuje nazwę FQDN zarządzanego konta magazynu z nazwy magazynu, obecnie wybranego środowiska i nazwy konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="252d4-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="252d4-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="252d4-128">-AccountResourceId</span></span>
<span data-ttu-id="252d4-129">Identyfikator zasobu Azure konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="252d4-129">Azure resource id of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="252d4-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="252d4-130">-ActiveKeyName</span></span>
<span data-ttu-id="252d4-131">Nazwa klucza konta magazynu, który musi być używany do generowania tokenów sas.</span><span class="sxs-lookup"><span data-stu-id="252d4-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="252d4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="252d4-132">-DefaultProfile</span></span>
<span data-ttu-id="252d4-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="252d4-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="252d4-134">- Wyłącz</span><span class="sxs-lookup"><span data-stu-id="252d4-134">-Disable</span></span>
<span data-ttu-id="252d4-135">Wyłącza użycie klucza zarządzanego konta magazynu do generowania tokenów sas.</span><span class="sxs-lookup"><span data-stu-id="252d4-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="252d4-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="252d4-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="252d4-137">Automatycznie generuj klucz.</span><span class="sxs-lookup"><span data-stu-id="252d4-137">Auto regenerate key.</span></span> <span data-ttu-id="252d4-138">Jeśli zostanie spełnione, klucz nieaktywny zarządzanego konta magazynu zostanie automatycznie ponownie wygenerowany i stanie się nowym kluczem aktywnym po okresie przechowywania.</span><span class="sxs-lookup"><span data-stu-id="252d4-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="252d4-139">Jeśli wartość jest fałszywa, klucze zarządzanego konta magazynu nie są automatycznie ponownie wygenerowane.</span><span class="sxs-lookup"><span data-stu-id="252d4-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="252d4-140">-WiodłoDziedzik</span><span class="sxs-lookup"><span data-stu-id="252d4-140">-RegenerationPeriod</span></span>
<span data-ttu-id="252d4-141">Okres niedyscytizacji.</span><span class="sxs-lookup"><span data-stu-id="252d4-141">Regeneration period.</span></span> <span data-ttu-id="252d4-142">Jeśli jest włączony klucz automatycznej generowania, ta wartość określa czas, po upływie którego nieaktywne klucze zarządzanego konta magazynu są automatycznie generowane i staje się nowym kluczem aktywnym.</span><span class="sxs-lookup"><span data-stu-id="252d4-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="252d4-143">— Tag</span><span class="sxs-lookup"><span data-stu-id="252d4-143">-Tag</span></span>
<span data-ttu-id="252d4-144">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="252d4-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="252d4-145">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="252d4-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="252d4-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="252d4-146">-VaultName</span></span>
<span data-ttu-id="252d4-147">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="252d4-147">Vault name.</span></span>
<span data-ttu-id="252d4-148">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="252d4-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="252d4-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="252d4-149">-Confirm</span></span>
<span data-ttu-id="252d4-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="252d4-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="252d4-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="252d4-151">-WhatIf</span></span>
<span data-ttu-id="252d4-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="252d4-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="252d4-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="252d4-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="252d4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="252d4-154">CommonParameters</span></span>
<span data-ttu-id="252d4-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="252d4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="252d4-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="252d4-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="252d4-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="252d4-157">INPUTS</span></span>

### <span data-ttu-id="252d4-158">System.String</span><span class="sxs-lookup"><span data-stu-id="252d4-158">System.String</span></span>

### <span data-ttu-id="252d4-159">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="252d4-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="252d4-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="252d4-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="252d4-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="252d4-161">OUTPUTS</span></span>

### <span data-ttu-id="252d4-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="252d4-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="252d4-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="252d4-163">NOTES</span></span>

## <span data-ttu-id="252d4-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="252d4-164">RELATED LINKS</span></span>

[<span data-ttu-id="252d4-165">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="252d4-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
