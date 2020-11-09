---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: c09218b960fb6c11b685106a3cb90bfdfd2f546a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304620"
---
# <span data-ttu-id="f5da8-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f5da8-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="f5da8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5da8-102">SYNOPSIS</span></span>
<span data-ttu-id="f5da8-103">Pobiera definicje SAS magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="f5da8-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="f5da8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5da8-104">SYNTAX</span></span>

### <span data-ttu-id="f5da8-105">ByDefinitionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f5da8-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5da8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f5da8-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5da8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f5da8-107">DESCRIPTION</span></span>
<span data-ttu-id="f5da8-108">Pobiera definicję SAS magazynu zarządzanego w magazynie kluczy, jeśli określono nazwę definicji.</span><span class="sxs-lookup"><span data-stu-id="f5da8-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="f5da8-109">Jeśli nie podano nazwy definicji, zostanie wyświetlona lista wszystkich definicji skojarzeń zabezpieczeń skojarzonych z określonym kontem magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="f5da8-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="f5da8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5da8-110">EXAMPLES</span></span>

### <span data-ttu-id="f5da8-111">Przykład 1: Lista wszystkich definicji skojarzeń SAS magazynu zarządzanego przez Magazyn kluczy</span><span class="sxs-lookup"><span data-stu-id="f5da8-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
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

<span data-ttu-id="f5da8-112">Wyświetla listę wszystkich definicji skojarzeń zabezpieczeń skojarzonych z kontem magazynu zarządzanego w magazynie kluczy "mystorageaccount" zarządzaną przez magazyn magazynu ".</span><span class="sxs-lookup"><span data-stu-id="f5da8-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="f5da8-113">Przykład 2: Uzyskiwanie konta magazynu zarządzanego w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="f5da8-113">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="f5da8-114">Pobiera szczegóły definicji SAS "accountsas" skojarzonej z kontem "mystorageaccount" zarządzanym magazynem kluczy zarządzanym przez magazyn magazynu ".</span><span class="sxs-lookup"><span data-stu-id="f5da8-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="f5da8-115">Przykład 3: Lista wszystkich definicji skojarzeń SAS magazynu zarządzanych przez Magazyn kluczy przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="f5da8-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
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

<span data-ttu-id="f5da8-116">Wyświetla listę wszystkich definicji skojarzeń zabezpieczeń skojarzonych z kontem magazynu "mystorageaccount" zarządzanym magazynem kluczy, którym zarządza Magazyn "konto".</span><span class="sxs-lookup"><span data-stu-id="f5da8-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="f5da8-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5da8-117">PARAMETERS</span></span>

### <span data-ttu-id="f5da8-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5da8-118">-AccountName</span></span>
<span data-ttu-id="f5da8-119">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="f5da8-119">Vault name.</span></span>
<span data-ttu-id="f5da8-120">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="f5da8-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f5da8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5da8-121">-DefaultProfile</span></span>
<span data-ttu-id="f5da8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f5da8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5da8-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f5da8-123">-InputObject</span></span>
<span data-ttu-id="f5da8-124">Obiekt ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="f5da8-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="f5da8-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f5da8-125">-InRemovedState</span></span>
<span data-ttu-id="f5da8-126">Określa, czy w danych wyjściowych mają być pokazywane uprzednio usunięte definicje SAS magazynu.</span><span class="sxs-lookup"><span data-stu-id="f5da8-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="f5da8-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f5da8-127">-Name</span></span>
<span data-ttu-id="f5da8-128">Nazwa definicji SAS magazynu.</span><span class="sxs-lookup"><span data-stu-id="f5da8-128">Storage sas definition name.</span></span>
<span data-ttu-id="f5da8-129">Polecenie cmdlet tworzy nazwę FQDN definicji SAS magazynu danych na podstawie nazwy magazynu, obecnie wybranego środowiska, nazwy konta magazynu i nazwy definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="f5da8-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="f5da8-130">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="f5da8-130">-VaultName</span></span>
<span data-ttu-id="f5da8-131">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="f5da8-131">Vault name.</span></span>
<span data-ttu-id="f5da8-132">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="f5da8-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f5da8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5da8-133">CommonParameters</span></span>
<span data-ttu-id="f5da8-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5da8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5da8-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5da8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5da8-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5da8-136">INPUTS</span></span>

### <span data-ttu-id="f5da8-137">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f5da8-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="f5da8-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5da8-138">OUTPUTS</span></span>

### <span data-ttu-id="f5da8-139">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f5da8-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="f5da8-140">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f5da8-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="f5da8-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f5da8-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="f5da8-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f5da8-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="f5da8-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5da8-143">NOTES</span></span>

## <span data-ttu-id="f5da8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5da8-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

