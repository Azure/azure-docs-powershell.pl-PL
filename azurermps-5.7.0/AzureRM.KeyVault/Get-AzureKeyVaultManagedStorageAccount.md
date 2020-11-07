---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 6cde1ab6a0f2041e154756e730f73e350a3c93d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719471"
---
# <span data-ttu-id="a58a2-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a58a2-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="a58a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a58a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a58a2-103">Pobiera konta usługi Azure Storage zarządzane za pomocą magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a58a2-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a58a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a58a2-104">SYNTAX</span></span>

### <span data-ttu-id="a58a2-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a58a2-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a58a2-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="a58a2-106">ByAccountName</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a58a2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a58a2-107">DESCRIPTION</span></span>
<span data-ttu-id="a58a2-108">Pobiera konto magazynu usługi Azure Storage zarządzane, jeśli określono nazwę konta, a klucze kont są zarządzane przez określony magazyn.</span><span class="sxs-lookup"><span data-stu-id="a58a2-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="a58a2-109">Jeśli nazwa konta nie zostanie określona, na liście znajdują się wszystkie konta, których klucze są zarządzane przez określony magazyn.</span><span class="sxs-lookup"><span data-stu-id="a58a2-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="a58a2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a58a2-110">EXAMPLES</span></span>

### <span data-ttu-id="a58a2-111">Przykład 1: wyświetlanie wszystkich kont magazynu zarządzanych przez Magazyn kluczy</span><span class="sxs-lookup"><span data-stu-id="a58a2-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="a58a2-112">Wyświetla listę wszystkich kont, których klucze zarządza magazynem magazynu.</span><span class="sxs-lookup"><span data-stu-id="a58a2-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="a58a2-113">Przykład 2: Uzyskiwanie konta magazynu zarządzanego w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="a58a2-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="a58a2-114">Pobiera szczegóły konta magazynu zarządzanego w magazynie kluczy "mystorageaccount", jeśli klucze są zarządzane przez magazyn "Moja magazyn"</span><span class="sxs-lookup"><span data-stu-id="a58a2-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="a58a2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a58a2-115">PARAMETERS</span></span>

### <span data-ttu-id="a58a2-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a58a2-116">-AccountName</span></span>
<span data-ttu-id="a58a2-117">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="a58a2-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="a58a2-118">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a58a2-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a58a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58a2-119">-DefaultProfile</span></span>
<span data-ttu-id="a58a2-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a58a2-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a58a2-121">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="a58a2-121">-VaultName</span></span>
<span data-ttu-id="a58a2-122">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="a58a2-122">Vault name.</span></span>
<span data-ttu-id="a58a2-123">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="a58a2-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a58a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58a2-124">CommonParameters</span></span>
<span data-ttu-id="a58a2-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a58a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58a2-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a58a2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58a2-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a58a2-127">INPUTS</span></span>

### <span data-ttu-id="a58a2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a58a2-128">System.String</span></span>

## <span data-ttu-id="a58a2-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a58a2-129">OUTPUTS</span></span>

### <span data-ttu-id="a58a2-130">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. platforming. models. ManagedStorageAccount, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="a58a2-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="a58a2-131">Microsoft. Azure. Commands. platforming. models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a58a2-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="a58a2-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a58a2-132">NOTES</span></span>

## <span data-ttu-id="a58a2-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a58a2-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
