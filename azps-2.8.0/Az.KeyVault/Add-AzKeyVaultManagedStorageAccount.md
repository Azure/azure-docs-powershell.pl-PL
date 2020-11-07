---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 56883ecc1ca562ed4a259be9d1940683e652a280
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705188"
---
# <span data-ttu-id="41d1c-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="41d1c-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="41d1c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="41d1c-103">Umożliwia dodanie istniejącego konta usługi Azure Storage do określonego magazynu kluczy dla swoich kluczy, które mają być zarządzane przez usługę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="41d1c-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="41d1c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41d1c-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41d1c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41d1c-105">DESCRIPTION</span></span>
<span data-ttu-id="41d1c-106">Skonfiguruj istniejące konto usługi Azure Storage, korzystając z magazynu kluczy na potrzeby kluczy konta magazynu, które mają być zarządzane przez Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="41d1c-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="41d1c-107">Konto magazynu musi już istnieć.</span><span class="sxs-lookup"><span data-stu-id="41d1c-107">The Storage Account must already exist.</span></span> <span data-ttu-id="41d1c-108">Klucze magazynowania nigdy nie są narażone na dzwonienie.</span><span class="sxs-lookup"><span data-stu-id="41d1c-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="41d1c-109">Automatyczne ponowne generowanie magazynu kluczy i przełączanie aktywnego klucza na podstawie okresu regeneracji.</span><span class="sxs-lookup"><span data-stu-id="41d1c-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="41d1c-110">Zobacz [zarządzane konto magazynu kluczy Azure — program PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) , aby zapoznać się z omówieniem tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="41d1c-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="41d1c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41d1c-111">EXAMPLES</span></span>

### <span data-ttu-id="41d1c-112">Przykład 1: Ustawianie konta usługi Azure Storage za pomocą magazynu kluczy do zarządzania kluczami</span><span class="sxs-lookup"><span data-stu-id="41d1c-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="41d1c-113">Ustawia konto magazynu z kluczowym magazynem dla swoich kluczy, które mają być zarządzane przez Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="41d1c-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="41d1c-114">Aktywnym zestawem kluczy jest "KEY1".</span><span class="sxs-lookup"><span data-stu-id="41d1c-114">The active key set is 'key1'.</span></span> <span data-ttu-id="41d1c-115">Ten klucz zostanie wykorzystany do wygenerowania tokenów SAS.</span><span class="sxs-lookup"><span data-stu-id="41d1c-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="41d1c-116">Po upływie czasu tego polecenia Magazyn kluczy będzie ponownie generował klucz "key2", a następnie ustawił go jako aktywny klucz.</span><span class="sxs-lookup"><span data-stu-id="41d1c-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="41d1c-117">Ten proces automatycznego ponownego generowania będzie kontynuowany między "KEY1" a "key2" z przerwą 90 dni.</span><span class="sxs-lookup"><span data-stu-id="41d1c-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="41d1c-118">Przykład 2: Ustawianie klasycznego konta magazynu platformy Azure za pomocą magazynu kluczy do zarządzania kluczami</span><span class="sxs-lookup"><span data-stu-id="41d1c-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="41d1c-119">Umożliwia ustawienie klasycznego konta magazynu za pomocą magazynu kluczy na potrzeby zarządzania kluczami w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="41d1c-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="41d1c-120">Aktywnym zestawem kluczy jest "podstawowy".</span><span class="sxs-lookup"><span data-stu-id="41d1c-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="41d1c-121">Ten klucz zostanie wykorzystany do wygenerowania tokenów SAS.</span><span class="sxs-lookup"><span data-stu-id="41d1c-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="41d1c-122">Po upływie czasu tego polecenia Magazyn kluczy ponownie wygeneruje klucz pomocniczy po okresie ponownego generowania i ustawi go jako aktywny.</span><span class="sxs-lookup"><span data-stu-id="41d1c-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="41d1c-123">Ten proces automatycznego ponownego generowania będzie kontynuowany między "podstawowy" a "drugorzędny" z przerwą 90 dni.</span><span class="sxs-lookup"><span data-stu-id="41d1c-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="41d1c-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41d1c-124">PARAMETERS</span></span>

### <span data-ttu-id="41d1c-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="41d1c-125">-AccountName</span></span>
<span data-ttu-id="41d1c-126">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="41d1c-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="41d1c-127">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="41d1c-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="41d1c-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="41d1c-128">-AccountResourceId</span></span>
<span data-ttu-id="41d1c-129">Identyfikator zasobu platformy Azure konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="41d1c-129">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="41d1c-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="41d1c-130">-ActiveKeyName</span></span>
<span data-ttu-id="41d1c-131">Nazwa klucza konta magazynu, który musi być wykorzystywany do generowania tokenów SAS.</span><span class="sxs-lookup"><span data-stu-id="41d1c-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="41d1c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d1c-132">-DefaultProfile</span></span>
<span data-ttu-id="41d1c-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="41d1c-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41d1c-134">-Disable</span><span class="sxs-lookup"><span data-stu-id="41d1c-134">-Disable</span></span>
<span data-ttu-id="41d1c-135">Wyłącza używanie klucza zarządzanych kont magazynu na potrzeby generowania tokenów SAS.</span><span class="sxs-lookup"><span data-stu-id="41d1c-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="41d1c-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="41d1c-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="41d1c-137">Automatyczne generowanie klucza.</span><span class="sxs-lookup"><span data-stu-id="41d1c-137">Auto regenerate key.</span></span> <span data-ttu-id="41d1c-138">Jeśli prawda, nieaktywny klucz konta magazynu zarządzanego jest automatycznie regenerowany i staje się nowym kluczem po upływie okresu regeneracji.</span><span class="sxs-lookup"><span data-stu-id="41d1c-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="41d1c-139">Jeśli wartość false, klucze zarządzanego konta magazynu nie są automatycznie generowane ponownie.</span><span class="sxs-lookup"><span data-stu-id="41d1c-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="41d1c-140">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="41d1c-140">-RegenerationPeriod</span></span>
<span data-ttu-id="41d1c-141">Okres regeneracji.</span><span class="sxs-lookup"><span data-stu-id="41d1c-141">Regeneration period.</span></span> <span data-ttu-id="41d1c-142">Jeśli klucz automatycznego ponownego generowania jest włączony, ta wartość określa przedział czasu, po którym nieaktywny klucz konta zarządzanej przestrzeni dyskowej zostanie automatycznie wygenerowany ponownie i stanie się nowym aktywnym kluczem.</span><span class="sxs-lookup"><span data-stu-id="41d1c-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="41d1c-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="41d1c-143">-Tag</span></span>
<span data-ttu-id="41d1c-144">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="41d1c-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="41d1c-145">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="41d1c-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="41d1c-146">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="41d1c-146">-VaultName</span></span>
<span data-ttu-id="41d1c-147">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="41d1c-147">Vault name.</span></span>
<span data-ttu-id="41d1c-148">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="41d1c-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="41d1c-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41d1c-149">-Confirm</span></span>
<span data-ttu-id="41d1c-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41d1c-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41d1c-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d1c-151">-WhatIf</span></span>
<span data-ttu-id="41d1c-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41d1c-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41d1c-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41d1c-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41d1c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d1c-154">CommonParameters</span></span>
<span data-ttu-id="41d1c-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41d1c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d1c-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41d1c-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d1c-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41d1c-157">INPUTS</span></span>

### <span data-ttu-id="41d1c-158">System. String</span><span class="sxs-lookup"><span data-stu-id="41d1c-158">System.String</span></span>

### <span data-ttu-id="41d1c-159">System. Nullable "1 [[System. TimeSpan, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="41d1c-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="41d1c-160">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="41d1c-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="41d1c-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41d1c-161">OUTPUTS</span></span>

### <span data-ttu-id="41d1c-162">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="41d1c-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="41d1c-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41d1c-163">NOTES</span></span>

## <span data-ttu-id="41d1c-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41d1c-164">RELATED LINKS</span></span>

[<span data-ttu-id="41d1c-165">AZ.</span><span class="sxs-lookup"><span data-stu-id="41d1c-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
