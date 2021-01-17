---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c415a7b80609a9e8794df183b2ae1cea73a7f1cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333010"
---
# <span data-ttu-id="80fa6-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80fa6-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="80fa6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="80fa6-103">Umożliwia usunięcie konta usługi Azure Storage zarządzanego w magazynie kluczy oraz wszystkich skojarzonych definicji skojarzeń zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="80fa6-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="80fa6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80fa6-104">SYNTAX</span></span>

### <span data-ttu-id="80fa6-105">ByDefinitionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="80fa6-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80fa6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="80fa6-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80fa6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="80fa6-107">DESCRIPTION</span></span>
<span data-ttu-id="80fa6-108">Odkojarzy konto usługi Azure Storage z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="80fa6-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="80fa6-109">Nie spowoduje to usunięcia konta usługi Azure Storage, ale usunie klucze kont z zarządzania przez Magazyn kluczy Azure.</span><span class="sxs-lookup"><span data-stu-id="80fa6-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="80fa6-110">Wszystkie skojarzone definicje SAS magazynu zarządzanego magazynu kluczy również zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="80fa6-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="80fa6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80fa6-111">EXAMPLES</span></span>

### <span data-ttu-id="80fa6-112">Przykład 1: Usunięcie konta usługi Azure Storage zarządzanego magazynu kluczy oraz wszystkich skojarzonych definicji skojarzeń zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="80fa6-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
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

<span data-ttu-id="80fa6-113">Odkojarzy konto magazynu platformy Azure "mystorageaccount" z magazynu kluczy i zaprzestaje zarządzania kluczami w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="80fa6-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="80fa6-114">Konto "mystorageaccount" nie zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="80fa6-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="80fa6-115">Wszystkie definicje skojarzeń SAS magazynu zarządzanego w magazynie kluczy skojarzone z tym kontem zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="80fa6-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="80fa6-116">Przykład 2: Usunięcie konta usługi Azure Storage zarządzanego magazynu kluczy oraz wszystkich skojarzonych definicji skojarzeń zabezpieczeń bez potwierdzenia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="80fa6-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
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

<span data-ttu-id="80fa6-117">Odkojarzy konto magazynu platformy Azure "mystorageaccount" z magazynu kluczy i zaprzestaje zarządzania kluczami w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="80fa6-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="80fa6-118">Konto "mystorageaccount" nie zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="80fa6-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="80fa6-119">Wszystkie definicje skojarzeń SAS magazynu zarządzanego w magazynie kluczy skojarzone z tym kontem zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="80fa6-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="80fa6-120">Przykład 3: trwałe usuwanie (przeczyszczanie) konta usługi Azure Storage zarządzanego przez Magazyn kluczy oraz wszystkich skojarzonych definicji skojarzeń zabezpieczeń w magazynie z włączonym miękkim usuwaniem.</span><span class="sxs-lookup"><span data-stu-id="80fa6-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="80fa6-121">W przykładzie przyjęto założenie, że dla tego magazynu jest włączony miękki usuwanie.</span><span class="sxs-lookup"><span data-stu-id="80fa6-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="80fa6-122">Sprawdź, czy jest to przypadek, przeglądając właściwości magazynu lub atrybut RecoveryLevel jednostki w magazynie.</span><span class="sxs-lookup"><span data-stu-id="80fa6-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="80fa6-123">Pierwsze polecenie cmdlet powoduje odkojarzenie konta magazynu platformy Azure "mystorageaccount" z magazynu kluczy i zatrzymuje zarządzanie kluczami w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="80fa6-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="80fa6-124">Konto "mystorageaccount" nie zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="80fa6-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="80fa6-125">Wszystkie definicje skojarzeń SAS magazynu zarządzanego w magazynie kluczy skojarzone z tym kontem zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="80fa6-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="80fa6-126">Drugie polecenie cmdlet weryfikuje, czy konto magazynu zostało usunięte, ale stan odzyskania.</span><span class="sxs-lookup"><span data-stu-id="80fa6-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="80fa6-127">Uzyskanie dostępu do tego stanu może wymagać jakiegoś czasu, więc zanim spróbujesz, daj ~ 30s.</span><span class="sxs-lookup"><span data-stu-id="80fa6-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="80fa6-128">Trzecia operacja cmdlet powoduje trwałe usunięcie konta magazynu — odzyskiwanie nie będzie już możliwe.</span><span class="sxs-lookup"><span data-stu-id="80fa6-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="80fa6-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80fa6-129">PARAMETERS</span></span>

### <span data-ttu-id="80fa6-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="80fa6-130">-AccountName</span></span>
<span data-ttu-id="80fa6-131">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="80fa6-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="80fa6-132">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="80fa6-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="80fa6-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80fa6-133">-DefaultProfile</span></span>
<span data-ttu-id="80fa6-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="80fa6-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80fa6-135">-Force</span><span class="sxs-lookup"><span data-stu-id="80fa6-135">-Force</span></span>
<span data-ttu-id="80fa6-136">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="80fa6-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="80fa6-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="80fa6-137">-InputObject</span></span>
<span data-ttu-id="80fa6-138">Obiekt ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="80fa6-138">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="80fa6-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="80fa6-139">-InRemovedState</span></span>
<span data-ttu-id="80fa6-140">Trwale Usuń wcześniej usunięte konto zarządzanego magazynu.</span><span class="sxs-lookup"><span data-stu-id="80fa6-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="80fa6-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80fa6-141">-PassThru</span></span>
<span data-ttu-id="80fa6-142">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="80fa6-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="80fa6-143">Jeśli ten przełącznik jest określony, polecenie cmdlet zwróci konto zarządzanego magazynu, które zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="80fa6-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="80fa6-144">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="80fa6-144">-VaultName</span></span>
<span data-ttu-id="80fa6-145">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="80fa6-145">Vault name.</span></span>
<span data-ttu-id="80fa6-146">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="80fa6-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="80fa6-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80fa6-147">-Confirm</span></span>
<span data-ttu-id="80fa6-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80fa6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80fa6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80fa6-149">-WhatIf</span></span>
<span data-ttu-id="80fa6-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80fa6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80fa6-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="80fa6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80fa6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80fa6-152">CommonParameters</span></span>
<span data-ttu-id="80fa6-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80fa6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80fa6-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80fa6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80fa6-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80fa6-155">INPUTS</span></span>

### <span data-ttu-id="80fa6-156">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="80fa6-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="80fa6-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80fa6-157">OUTPUTS</span></span>

### <span data-ttu-id="80fa6-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80fa6-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="80fa6-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80fa6-159">NOTES</span></span>

## <span data-ttu-id="80fa6-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80fa6-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

