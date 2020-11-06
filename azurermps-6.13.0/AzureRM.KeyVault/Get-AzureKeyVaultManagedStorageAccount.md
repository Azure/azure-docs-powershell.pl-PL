---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: f3a1e4d1e938b84a434c07451f3d2294e203f440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551251"
---
# <span data-ttu-id="a2c65-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2c65-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="a2c65-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2c65-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c65-103">Pobiera konta usługi Azure Storage zarządzane za pomocą magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a2c65-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2c65-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2c65-104">SYNTAX</span></span>

### <span data-ttu-id="a2c65-105">ByAccountName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a2c65-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2c65-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a2c65-106">ByInputObject</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2c65-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c65-107">ByResourceId</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2c65-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a2c65-108">DESCRIPTION</span></span>
<span data-ttu-id="a2c65-109">Pobiera konto magazynu usługi Azure Storage zarządzane, jeśli określono nazwę konta, a klucze kont są zarządzane przez określony magazyn.</span><span class="sxs-lookup"><span data-stu-id="a2c65-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="a2c65-110">Jeśli nazwa konta nie zostanie określona, na liście znajdują się wszystkie konta, których klucze są zarządzane przez określony magazyn.</span><span class="sxs-lookup"><span data-stu-id="a2c65-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="a2c65-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2c65-111">EXAMPLES</span></span>

### <span data-ttu-id="a2c65-112">Przykład 1: wyświetlanie wszystkich kont magazynu zarządzanych przez Magazyn kluczy</span><span class="sxs-lookup"><span data-stu-id="a2c65-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'

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

<span data-ttu-id="a2c65-113">Wyświetla listę wszystkich kont, których klucze zarządza magazynem magazynu.</span><span class="sxs-lookup"><span data-stu-id="a2c65-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="a2c65-114">Przykład 2: Uzyskiwanie konta magazynu zarządzanego w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="a2c65-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

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

<span data-ttu-id="a2c65-115">Pobiera szczegóły konta magazynu zarządzanego w magazynie kluczy "mystorageaccount", jeśli klucze są zarządzane przez magazyn "Moja magazyn"</span><span class="sxs-lookup"><span data-stu-id="a2c65-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="a2c65-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2c65-116">PARAMETERS</span></span>

### <span data-ttu-id="a2c65-117">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a2c65-117">-AccountName</span></span>
<span data-ttu-id="a2c65-118">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="a2c65-118">Key Vault managed storage account name.</span></span> <span data-ttu-id="a2c65-119">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a2c65-119">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c65-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c65-120">-DefaultProfile</span></span>
<span data-ttu-id="a2c65-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a2c65-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c65-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a2c65-122">-InputObject</span></span>
<span data-ttu-id="a2c65-123">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="a2c65-123">Vault object.</span></span>

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

### <span data-ttu-id="a2c65-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a2c65-124">-InRemovedState</span></span>
<span data-ttu-id="a2c65-125">Określa, czy mają być pokazywane uprzednio usunięte konta magazynu w danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a2c65-125">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="a2c65-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c65-126">-ResourceId</span></span>
<span data-ttu-id="a2c65-127">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="a2c65-127">Vault resource id.</span></span>

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

### <span data-ttu-id="a2c65-128">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="a2c65-128">-VaultName</span></span>
<span data-ttu-id="a2c65-129">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="a2c65-129">Vault name.</span></span>
<span data-ttu-id="a2c65-130">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="a2c65-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a2c65-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c65-131">CommonParameters</span></span>
<span data-ttu-id="a2c65-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c65-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c65-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2c65-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c65-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2c65-134">INPUTS</span></span>

### <span data-ttu-id="a2c65-135">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a2c65-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="a2c65-136">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a2c65-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a2c65-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a2c65-137">System.String</span></span>

## <span data-ttu-id="a2c65-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2c65-138">OUTPUTS</span></span>

### <span data-ttu-id="a2c65-139">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a2c65-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="a2c65-140">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2c65-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="a2c65-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a2c65-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="a2c65-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2c65-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="a2c65-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2c65-143">NOTES</span></span>

## <span data-ttu-id="a2c65-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2c65-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

