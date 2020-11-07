---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 165419eb13376becedf72b4e44ee17f0c3655ec4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705156"
---
# <span data-ttu-id="3cfd4-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3cfd4-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="3cfd4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cfd4-102">SYNOPSIS</span></span>
<span data-ttu-id="3cfd4-103">Pobiera konta usługi Azure Storage zarządzane za pomocą magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="3cfd4-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="3cfd4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cfd4-104">SYNTAX</span></span>

### <span data-ttu-id="3cfd4-105">ByAccountName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3cfd4-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cfd4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3cfd4-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cfd4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3cfd4-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cfd4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3cfd4-108">DESCRIPTION</span></span>
<span data-ttu-id="3cfd4-109">Pobiera konto magazynu usługi Azure Storage zarządzane, jeśli określono nazwę konta, a klucze kont są zarządzane przez określony magazyn.</span><span class="sxs-lookup"><span data-stu-id="3cfd4-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="3cfd4-110">Jeśli nazwa konta nie zostanie określona, na liście znajdują się wszystkie konta, których klucze są zarządzane przez określony magazyn.</span><span class="sxs-lookup"><span data-stu-id="3cfd4-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="3cfd4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cfd4-111">EXAMPLES</span></span>

### <span data-ttu-id="3cfd4-112">Przykład 1: wyświetlanie wszystkich kont magazynu zarządzanych przez Magazyn kluczy</span><span class="sxs-lookup"><span data-stu-id="3cfd4-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
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

<span data-ttu-id="3cfd4-113">Wyświetla listę wszystkich kont, których klucze zarządza magazynem magazynu.</span><span class="sxs-lookup"><span data-stu-id="3cfd4-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="3cfd4-114">Przykład 2: Uzyskiwanie konta magazynu zarządzanego w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="3cfd4-114">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="3cfd4-115">Pobiera szczegóły konta magazynu zarządzanego w magazynie kluczy "mystorageaccount", jeśli klucze są zarządzane przez magazyn "Moja magazyn"</span><span class="sxs-lookup"><span data-stu-id="3cfd4-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="3cfd4-116">Przykład 3: Lista wszystkich kont magazynu zarządzanego w magazynie kluczy przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="3cfd4-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
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

<span data-ttu-id="3cfd4-117">Wyświetla wszystkie konta, których klucze są zarządzane przez magazyn "Moja magazyn", rozpoczynające się od tekstu "test"</span><span class="sxs-lookup"><span data-stu-id="3cfd4-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="3cfd4-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cfd4-118">PARAMETERS</span></span>

### <span data-ttu-id="3cfd4-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3cfd4-119">-AccountName</span></span>
<span data-ttu-id="3cfd4-120">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="3cfd4-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="3cfd4-121">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3cfd4-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="3cfd4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cfd4-122">-DefaultProfile</span></span>
<span data-ttu-id="3cfd4-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3cfd4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cfd4-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3cfd4-124">-InputObject</span></span>
<span data-ttu-id="3cfd4-125">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="3cfd4-125">Vault object.</span></span>

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

### <span data-ttu-id="3cfd4-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="3cfd4-126">-InRemovedState</span></span>
<span data-ttu-id="3cfd4-127">Określa, czy mają być pokazywane uprzednio usunięte konta magazynu w danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3cfd4-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="3cfd4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cfd4-128">-ResourceId</span></span>
<span data-ttu-id="3cfd4-129">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="3cfd4-129">Vault resource id.</span></span>

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

### <span data-ttu-id="3cfd4-130">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="3cfd4-130">-VaultName</span></span>
<span data-ttu-id="3cfd4-131">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="3cfd4-131">Vault name.</span></span>
<span data-ttu-id="3cfd4-132">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="3cfd4-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3cfd4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cfd4-133">CommonParameters</span></span>
<span data-ttu-id="3cfd4-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cfd4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cfd4-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cfd4-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cfd4-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cfd4-136">INPUTS</span></span>

### <span data-ttu-id="3cfd4-137">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3cfd4-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="3cfd4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3cfd4-138">System.String</span></span>

## <span data-ttu-id="3cfd4-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cfd4-139">OUTPUTS</span></span>

### <span data-ttu-id="3cfd4-140">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3cfd4-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="3cfd4-141">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3cfd4-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="3cfd4-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3cfd4-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="3cfd4-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3cfd4-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="3cfd4-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cfd4-144">NOTES</span></span>

## <span data-ttu-id="3cfd4-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cfd4-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
