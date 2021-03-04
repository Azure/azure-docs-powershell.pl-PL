---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: acb0e2811f184f7c3162635b87849a35ce9156ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001473"
---
# <span data-ttu-id="a5fb5-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="a5fb5-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="a5fb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="a5fb5-103">Pobiera definicje SAS magazynu zarządzanego przez magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="a5fb5-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="a5fb5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a5fb5-104">SYNTAX</span></span>

### <span data-ttu-id="a5fb5-105">ByDefinitionName (Default)</span><span class="sxs-lookup"><span data-stu-id="a5fb5-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5fb5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a5fb5-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5fb5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a5fb5-107">DESCRIPTION</span></span>
<span data-ttu-id="a5fb5-108">Pobiera definicję SAS magazynu zarządzanego przez magazyn kluczy, jeśli określono nazwę definicji.</span><span class="sxs-lookup"><span data-stu-id="a5fb5-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="a5fb5-109">Jeśli nazwa definicji nie zostanie określona, zostaną wyświetlone wszystkie definicje sygnatur SAS skojarzone z określonym kontem magazynu zarządzanego magazynu kluczy w magazynie.</span><span class="sxs-lookup"><span data-stu-id="a5fb5-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="a5fb5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a5fb5-110">EXAMPLES</span></span>

### <span data-ttu-id="a5fb5-111">Przykład 1. Lista wszystkich definicji SAS magazynu zarządzanego przez magazyn kluczy</span><span class="sxs-lookup"><span data-stu-id="a5fb5-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="a5fb5-112">Lista wszystkich definicji SAS skojarzonych z zarządzanym kontem magazynu kluczy "mystorageaccount" zarządzanym przez magazyn "myvault"</span><span class="sxs-lookup"><span data-stu-id="a5fb5-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="a5fb5-113">Przykład 2. Uzyskiwanie zarządzanego konta magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="a5fb5-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Secret Id   : https://myvault.vault.azure.net/secrets/mystorageaccount-accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="a5fb5-114">Pobiera szczegółowe informacje o "kontach" funkcji SAS Definition skojarzonych z zarządzanym kontem magazynu magazynu kluczy "mystorageaccount" zarządzanym przez magazyn "myvault".</span><span class="sxs-lookup"><span data-stu-id="a5fb5-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="a5fb5-115">Przykład 3. Lista wszystkich definicji SAS magazynu zarządzanego przez magazyn kluczy przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="a5fb5-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name "account*"

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas1
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas1
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas2
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas2
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="a5fb5-116">Lista wszystkich definicji SAS skojarzonych z zarządzanym kontem magazynu kluczy "mystorageaccount" zarządzanym przez magazyn "myvault", które zaczynają się od "konta".</span><span class="sxs-lookup"><span data-stu-id="a5fb5-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="a5fb5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5fb5-117">PARAMETERS</span></span>

### <span data-ttu-id="a5fb5-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a5fb5-118">-AccountName</span></span>
<span data-ttu-id="a5fb5-119">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="a5fb5-119">Vault name.</span></span>
<span data-ttu-id="a5fb5-120">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="a5fb5-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fb5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5fb5-121">-DefaultProfile</span></span>
<span data-ttu-id="a5fb5-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a5fb5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5fb5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5fb5-123">-InputObject</span></span>
<span data-ttu-id="a5fb5-124">Obiekt ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="a5fb5-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="a5fb5-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a5fb5-125">-InRemovedState</span></span>
<span data-ttu-id="a5fb5-126">Określa, czy w wynikach mają być wyświetlane definicje sygnatur SAS wcześniej usuniętych magazynów.</span><span class="sxs-lookup"><span data-stu-id="a5fb5-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="a5fb5-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a5fb5-127">-Name</span></span>
<span data-ttu-id="a5fb5-128">Nazwa definicji sas magazynu.</span><span class="sxs-lookup"><span data-stu-id="a5fb5-128">Storage sas definition name.</span></span>
<span data-ttu-id="a5fb5-129">Polecenie cmdlet konstruuje nazwę FQDN definicji sas magazynu z nazwy magazynu, obecnie wybranego środowiska, nazwy konta magazynu i nazwy definicji sas.</span><span class="sxs-lookup"><span data-stu-id="a5fb5-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fb5-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a5fb5-130">-VaultName</span></span>
<span data-ttu-id="a5fb5-131">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="a5fb5-131">Vault name.</span></span>
<span data-ttu-id="a5fb5-132">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="a5fb5-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a5fb5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5fb5-133">CommonParameters</span></span>
<span data-ttu-id="a5fb5-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5fb5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5fb5-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5fb5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5fb5-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5fb5-136">INPUTS</span></span>

### <span data-ttu-id="a5fb5-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a5fb5-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="a5fb5-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5fb5-138">OUTPUTS</span></span>

### <span data-ttu-id="a5fb5-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a5fb5-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="a5fb5-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="a5fb5-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="a5fb5-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="a5fb5-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="a5fb5-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a5fb5-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="a5fb5-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a5fb5-143">NOTES</span></span>

## <span data-ttu-id="a5fb5-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5fb5-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

