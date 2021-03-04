---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 552a696a31b8c5fb26a1c6a17434ef53380d0491
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001482"
---
# <span data-ttu-id="d7c50-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d7c50-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d7c50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7c50-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c50-103">Pobiera zarządzane konta magazynu platformy Azure z magazynem kluczy.</span><span class="sxs-lookup"><span data-stu-id="d7c50-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="d7c50-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d7c50-104">SYNTAX</span></span>

### <span data-ttu-id="d7c50-105">ByAccountName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="d7c50-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7c50-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7c50-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7c50-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7c50-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7c50-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d7c50-108">DESCRIPTION</span></span>
<span data-ttu-id="d7c50-109">Pobiera zarządzane konto magazynu platformy Azure, jeśli określono nazwę konta, a klucze konta są zarządzane przez określony magazyn.</span><span class="sxs-lookup"><span data-stu-id="d7c50-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="d7c50-110">Jeśli nazwa konta nie zostanie określona, zostaną wyświetlone wszystkie konta, których kluczami zarządza określony magazyn.</span><span class="sxs-lookup"><span data-stu-id="d7c50-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="d7c50-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d7c50-111">EXAMPLES</span></span>

### <span data-ttu-id="d7c50-112">Przykład 1. Lista wszystkich kont magazynu zarządzanego przez magazyn kluczy</span><span class="sxs-lookup"><span data-stu-id="d7c50-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'

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

<span data-ttu-id="d7c50-113">Lista wszystkich kont, których kluczami zarządza magazyn "myvault"</span><span class="sxs-lookup"><span data-stu-id="d7c50-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="d7c50-114">Przykład 2. Uzyskiwanie zarządzanego konta magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="d7c50-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/maddie1/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="d7c50-115">Pobiera szczegółowe informacje o koncie magazynu zarządzanego przez magazyn kluczy "mystorageaccount", jeśli jego klucze są zarządzane przez magazyn "myvault"</span><span class="sxs-lookup"><span data-stu-id="d7c50-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="d7c50-116">Przykład 3. Lista wszystkich zarządzanych kont magazynu kluczy przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="d7c50-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name "test*"

Id                  : https://myvault.vault.azure.net:443/storage/test1
Vault Name          : myvault
AccountName         : test1
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test1
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :

Id                  : https://myvault.vault.azure.net:443/storage/test2
Vault Name          : myvault
AccountName         : test2
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test2
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="d7c50-117">Lista wszystkich kont, których kluczami zarządza magazyn "myvault", których nazwa rozpoczyna się od "test"</span><span class="sxs-lookup"><span data-stu-id="d7c50-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="d7c50-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7c50-118">PARAMETERS</span></span>

### <span data-ttu-id="d7c50-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d7c50-119">-AccountName</span></span>
<span data-ttu-id="d7c50-120">Nazwa konta magazynu zarządzanego przez magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="d7c50-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="d7c50-121">Polecenie cmdlet konstruuje nazwę FQDN zarządzanego konta magazynu z nazwy magazynu, obecnie wybranego środowiska i nazwy konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="d7c50-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d7c50-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c50-122">-DefaultProfile</span></span>
<span data-ttu-id="d7c50-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d7c50-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7c50-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7c50-124">-InputObject</span></span>
<span data-ttu-id="d7c50-125">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="d7c50-125">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c50-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d7c50-126">-InRemovedState</span></span>
<span data-ttu-id="d7c50-127">Określa, czy w wynikach mają być wyświetlane usunięte wcześniej konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d7c50-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="d7c50-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7c50-128">-ResourceId</span></span>
<span data-ttu-id="d7c50-129">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="d7c50-129">Vault resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c50-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d7c50-130">-VaultName</span></span>
<span data-ttu-id="d7c50-131">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="d7c50-131">Vault name.</span></span>
<span data-ttu-id="d7c50-132">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="d7c50-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c50-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c50-133">CommonParameters</span></span>
<span data-ttu-id="d7c50-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7c50-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c50-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7c50-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c50-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7c50-136">INPUTS</span></span>

### <span data-ttu-id="d7c50-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d7c50-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d7c50-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d7c50-138">System.String</span></span>

## <span data-ttu-id="d7c50-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7c50-139">OUTPUTS</span></span>

### <span data-ttu-id="d7c50-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d7c50-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="d7c50-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d7c50-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="d7c50-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d7c50-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="d7c50-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d7c50-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d7c50-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d7c50-144">NOTES</span></span>

## <span data-ttu-id="d7c50-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7c50-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

