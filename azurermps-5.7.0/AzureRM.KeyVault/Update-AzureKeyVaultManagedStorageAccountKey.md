---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 317a7f72e68f442608a0b163afd99af6eaac28c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542547"
---
# <span data-ttu-id="2e55e-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2e55e-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="2e55e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e55e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e55e-103">Generuje ponownie określony klucz konta usługi Azure Storage zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="2e55e-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e55e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e55e-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e55e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e55e-105">DESCRIPTION</span></span>
<span data-ttu-id="2e55e-106">Generuje ponownie określony klucz konta usługi Azure Storage zarządzanego magazynu kluczy i ustawia klucz jako aktywny.</span><span class="sxs-lookup"><span data-stu-id="2e55e-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="2e55e-107">Główne serwery proxy magazynu połączenie z Menedżerem zasobów Azure w celu ponownego wygenerowania klucza.</span><span class="sxs-lookup"><span data-stu-id="2e55e-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="2e55e-108">Osoba dzwoniąca musi posses uprawnienia do ponownego generowania kluczy na danym koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2e55e-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="2e55e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e55e-109">EXAMPLES</span></span>

### <span data-ttu-id="2e55e-110">Przykład 1: ponowne wygenerowanie klucza</span><span class="sxs-lookup"><span data-stu-id="2e55e-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="2e55e-111">Generuje ponownie "KEY1" konta "mystorageaccount" i ustawia "KEY1" jako aktywną konto usługi Azure Storage z zarządzaniem magazynem kluczy.</span><span class="sxs-lookup"><span data-stu-id="2e55e-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="2e55e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e55e-112">PARAMETERS</span></span>

### <span data-ttu-id="2e55e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2e55e-113">-AccountName</span></span>
<span data-ttu-id="2e55e-114">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="2e55e-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="2e55e-115">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="2e55e-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e55e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e55e-116">-DefaultProfile</span></span>
<span data-ttu-id="2e55e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2e55e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e55e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2e55e-118">-Force</span></span>
<span data-ttu-id="2e55e-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2e55e-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e55e-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="2e55e-120">-KeyName</span></span>
<span data-ttu-id="2e55e-121">Nazwa klucza konta magazynu do ponownego wygenerowania i uaktywnienia.</span><span class="sxs-lookup"><span data-stu-id="2e55e-121">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e55e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e55e-122">-PassThru</span></span>
<span data-ttu-id="2e55e-123">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="2e55e-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2e55e-124">Jeśli ten przełącznik jest określony, polecenie cmdlet zwróci konto zarządzanego magazynu, które zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="2e55e-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e55e-125">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="2e55e-125">-VaultName</span></span>
<span data-ttu-id="2e55e-126">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="2e55e-126">Vault name.</span></span>
<span data-ttu-id="2e55e-127">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="2e55e-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2e55e-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e55e-128">-Confirm</span></span>
<span data-ttu-id="2e55e-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e55e-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e55e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e55e-130">-WhatIf</span></span>
<span data-ttu-id="2e55e-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e55e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e55e-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e55e-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e55e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e55e-133">CommonParameters</span></span>
<span data-ttu-id="2e55e-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e55e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e55e-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e55e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e55e-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e55e-136">INPUTS</span></span>

### <span data-ttu-id="2e55e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2e55e-137">System.String</span></span>

## <span data-ttu-id="2e55e-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e55e-138">OUTPUTS</span></span>

### <span data-ttu-id="2e55e-139">Microsoft. Azure. Commands. platforming. models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e55e-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="2e55e-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e55e-140">NOTES</span></span>

## <span data-ttu-id="2e55e-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e55e-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
