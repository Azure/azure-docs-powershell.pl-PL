---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 89452f2a00aea9d3ab42300c2f28bde67fec0905
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200035"
---
# <span data-ttu-id="07d9a-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07d9a-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="07d9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="07d9a-103">Pobiera zarządzane konta magazynu platformy Azure z magazynem kluczy.</span><span class="sxs-lookup"><span data-stu-id="07d9a-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="07d9a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="07d9a-104">SYNTAX</span></span>

### <span data-ttu-id="07d9a-105">ByAccountName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="07d9a-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07d9a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="07d9a-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07d9a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="07d9a-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07d9a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="07d9a-108">DESCRIPTION</span></span>
<span data-ttu-id="07d9a-109">Pobiera zarządzane konto magazynu platformy Azure, jeśli określono nazwę konta, a klucze konta są zarządzane przez określony magazyn.</span><span class="sxs-lookup"><span data-stu-id="07d9a-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="07d9a-110">Jeśli nazwa konta nie zostanie określona, zostaną wyświetlone wszystkie konta, których kluczami zarządza określony magazyn.</span><span class="sxs-lookup"><span data-stu-id="07d9a-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="07d9a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="07d9a-111">EXAMPLES</span></span>

### <span data-ttu-id="07d9a-112">Przykład 1. Lista wszystkich kont magazynu zarządzanego przez magazyn kluczy</span><span class="sxs-lookup"><span data-stu-id="07d9a-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
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

<span data-ttu-id="07d9a-113">Lista wszystkich kont, których kluczami zarządza magazyn "myvault"</span><span class="sxs-lookup"><span data-stu-id="07d9a-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="07d9a-114">Przykład 2. Uzyskiwanie konta magazynu zarządzanego przez magazyn kluczy</span><span class="sxs-lookup"><span data-stu-id="07d9a-114">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="07d9a-115">Pobiera szczegółowe informacje o koncie magazynu zarządzanego przez magazyn kluczy "mystorageaccount", jeśli jego klucze są zarządzane przez magazyn "myvault"</span><span class="sxs-lookup"><span data-stu-id="07d9a-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="07d9a-116">Przykład 3. Lista wszystkich zarządzanych kont magazynu kluczy przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="07d9a-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
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

<span data-ttu-id="07d9a-117">Lista wszystkich kont, których kluczami zarządza magazyn "myvault", których nazwa rozpoczyna się od "test"</span><span class="sxs-lookup"><span data-stu-id="07d9a-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="07d9a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07d9a-118">PARAMETERS</span></span>

### <span data-ttu-id="07d9a-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="07d9a-119">-AccountName</span></span>
<span data-ttu-id="07d9a-120">Nazwa konta magazynu zarządzanego przez magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="07d9a-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="07d9a-121">Polecenie cmdlet konstruuje nazwę FQDN zarządzanego konta magazynu z nazwy magazynu, obecnie wybranego środowiska i nazwy konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="07d9a-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="07d9a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d9a-122">-DefaultProfile</span></span>
<span data-ttu-id="07d9a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="07d9a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07d9a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07d9a-124">-InputObject</span></span>
<span data-ttu-id="07d9a-125">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="07d9a-125">Vault object.</span></span>

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

### <span data-ttu-id="07d9a-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="07d9a-126">-InRemovedState</span></span>
<span data-ttu-id="07d9a-127">Określa, czy w wynikach mają być wyświetlane usunięte wcześniej konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="07d9a-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="07d9a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07d9a-128">-ResourceId</span></span>
<span data-ttu-id="07d9a-129">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="07d9a-129">Vault resource id.</span></span>

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

### <span data-ttu-id="07d9a-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="07d9a-130">-VaultName</span></span>
<span data-ttu-id="07d9a-131">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="07d9a-131">Vault name.</span></span>
<span data-ttu-id="07d9a-132">Polecenie cmdlet konstruuje nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="07d9a-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="07d9a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d9a-133">CommonParameters</span></span>
<span data-ttu-id="07d9a-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d9a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d9a-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07d9a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d9a-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07d9a-136">INPUTS</span></span>

### <span data-ttu-id="07d9a-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="07d9a-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="07d9a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="07d9a-138">System.String</span></span>

## <span data-ttu-id="07d9a-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07d9a-139">OUTPUTS</span></span>

### <span data-ttu-id="07d9a-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="07d9a-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="07d9a-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07d9a-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="07d9a-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="07d9a-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="07d9a-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07d9a-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="07d9a-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="07d9a-144">NOTES</span></span>

## <span data-ttu-id="07d9a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07d9a-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

