---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 7606293338e6467247e257f34e6850f52b67a1c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717744"
---
# <span data-ttu-id="cabff-101">Get-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="cabff-101">Get-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="cabff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cabff-102">SYNOPSIS</span></span>
<span data-ttu-id="cabff-103">Pobiera definicje SAS magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="cabff-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cabff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cabff-104">SYNTAX</span></span>

### <span data-ttu-id="cabff-105">ByAccountName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cabff-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cabff-106">ByDefinitionName</span><span class="sxs-lookup"><span data-stu-id="cabff-106">ByDefinitionName</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cabff-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cabff-107">DESCRIPTION</span></span>
<span data-ttu-id="cabff-108">Pobiera definicję SAS magazynu zarządzanego w magazynie kluczy, jeśli określono nazwę definicji.</span><span class="sxs-lookup"><span data-stu-id="cabff-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="cabff-109">Jeśli nie podano nazwy definicji, zostanie wyświetlona lista wszystkich definicji skojarzeń zabezpieczeń skojarzonych z określonym kontem magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="cabff-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="cabff-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cabff-110">EXAMPLES</span></span>

### <span data-ttu-id="cabff-111">Przykład 1: Lista wszystkich definicji skojarzeń SAS magazynu zarządzanego przez Magazyn kluczy</span><span class="sxs-lookup"><span data-stu-id="cabff-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="cabff-112">Wyświetla listę wszystkich definicji skojarzeń zabezpieczeń skojarzonych z kontem magazynu zarządzanego w magazynie kluczy "mystorageaccount" zarządzaną przez magazyn magazynu ".</span><span class="sxs-lookup"><span data-stu-id="cabff-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="cabff-113">Przykład 2: Uzyskiwanie konta magazynu zarządzanego w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="cabff-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

<span data-ttu-id="cabff-114">Pobiera szczegóły definicji SAS "mysasDef" skojarzonej z kontem "mystorageaccount" zarządzanym magazynem kluczy zarządzanym przez magazyn magazynu ".</span><span class="sxs-lookup"><span data-stu-id="cabff-114">Gets the details of SAS Definition 'mysasDef' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="cabff-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cabff-115">PARAMETERS</span></span>

### <span data-ttu-id="cabff-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cabff-116">-AccountName</span></span>
<span data-ttu-id="cabff-117">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="cabff-117">Vault name.</span></span>
<span data-ttu-id="cabff-118">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="cabff-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cabff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cabff-119">-DefaultProfile</span></span>
<span data-ttu-id="cabff-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cabff-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabff-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cabff-121">-Name</span></span>
<span data-ttu-id="cabff-122">Nazwa definicji SAS magazynu.</span><span class="sxs-lookup"><span data-stu-id="cabff-122">Storage sas definition name.</span></span>
<span data-ttu-id="cabff-123">Polecenie cmdlet tworzy nazwę FQDN definicji SAS magazynu danych na podstawie nazwy magazynu, obecnie wybranego środowiska, nazwy konta magazynu i nazwy definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="cabff-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cabff-124">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="cabff-124">-VaultName</span></span>
<span data-ttu-id="cabff-125">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="cabff-125">Vault name.</span></span>
<span data-ttu-id="cabff-126">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="cabff-126">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cabff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cabff-127">CommonParameters</span></span>
<span data-ttu-id="cabff-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cabff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cabff-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cabff-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cabff-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cabff-130">INPUTS</span></span>

### <span data-ttu-id="cabff-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cabff-131">System.String</span></span>

## <span data-ttu-id="cabff-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cabff-132">OUTPUTS</span></span>

### <span data-ttu-id="cabff-133">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. platforming. models. ManagedStorageSasDefinitionListItem, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="cabff-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinitionListItem, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="cabff-134">Microsoft. Azure. Commands. platforming. models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="cabff-134">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="cabff-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cabff-135">NOTES</span></span>

## <span data-ttu-id="cabff-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cabff-136">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
