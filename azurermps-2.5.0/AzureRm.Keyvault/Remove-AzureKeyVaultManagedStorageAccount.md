---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 438d36a5c9081da3124c0ef5ee03c7eb9ad8f634
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897373"
---
# <span data-ttu-id="67055-101">Remove-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67055-101">Remove-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="67055-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67055-102">SYNOPSIS</span></span>
<span data-ttu-id="67055-103">Umożliwia usunięcie konta usługi Azure Storage zarządzanego w magazynie kluczy oraz wszystkich skojarzonych definicji skojarzeń zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="67055-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67055-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67055-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67055-105">Opis</span><span class="sxs-lookup"><span data-stu-id="67055-105">DESCRIPTION</span></span>
<span data-ttu-id="67055-106">Odkojarzy konto usługi Azure Storage z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="67055-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="67055-107">Nie spowoduje to usunięcia konta usługi Azure Storage, ale usunie klucze kont z zarządzania przez Magazyn kluczy Azure.</span><span class="sxs-lookup"><span data-stu-id="67055-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="67055-108">Wszystkie skojarzone definicje SAS magazynu zarządzanego magazynu kluczy również zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="67055-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="67055-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67055-109">EXAMPLES</span></span>

### <span data-ttu-id="67055-110">Przykład 1: Usunięcie konta usługi Azure Storage zarządzanego magazynu kluczy oraz wszystkich skojarzonych definicji skojarzeń zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="67055-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="67055-111">Odkojarzy konto magazynu platformy Azure "mystorageaccount" z magazynu kluczy i zaprzestaje zarządzania kluczami w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="67055-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="67055-112">Konto "mystorageaccount" nie zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="67055-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="67055-113">Wszystkie definicje skojarzeń SAS magazynu zarządzanego w magazynie kluczy skojarzone z tym kontem zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="67055-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="67055-114">Przykład 2: Usunięcie konta usługi Azure Storage zarządzanego magazynu kluczy oraz wszystkich skojarzonych definicji skojarzeń zabezpieczeń bez potwierdzenia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="67055-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="67055-115">Odkojarzy konto magazynu platformy Azure "mystorageaccount" z magazynu kluczy i zaprzestaje zarządzania kluczami w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="67055-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="67055-116">Konto "mystorageaccount" nie zostanie usunięte.</span><span class="sxs-lookup"><span data-stu-id="67055-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="67055-117">Wszystkie definicje skojarzeń SAS magazynu zarządzanego w magazynie kluczy skojarzone z tym kontem zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="67055-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="67055-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67055-118">PARAMETERS</span></span>

### <span data-ttu-id="67055-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="67055-119">-AccountName</span></span>
<span data-ttu-id="67055-120">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="67055-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="67055-121">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="67055-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="67055-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67055-122">-DefaultProfile</span></span>
<span data-ttu-id="67055-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="67055-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67055-124">-Force</span><span class="sxs-lookup"><span data-stu-id="67055-124">-Force</span></span>
<span data-ttu-id="67055-125">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="67055-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="67055-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67055-126">-PassThru</span></span>
<span data-ttu-id="67055-127">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="67055-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="67055-128">Jeśli ten przełącznik jest określony, polecenie cmdlet zwróci konto zarządzanego magazynu, które zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="67055-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="67055-129">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="67055-129">-VaultName</span></span>
<span data-ttu-id="67055-130">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="67055-130">Vault name.</span></span>
<span data-ttu-id="67055-131">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="67055-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="67055-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67055-132">-Confirm</span></span>
<span data-ttu-id="67055-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67055-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67055-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67055-134">-WhatIf</span></span>
<span data-ttu-id="67055-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67055-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67055-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="67055-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67055-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67055-137">CommonParameters</span></span>
<span data-ttu-id="67055-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67055-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67055-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67055-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67055-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67055-140">INPUTS</span></span>

### <span data-ttu-id="67055-141">System. String</span><span class="sxs-lookup"><span data-stu-id="67055-141">System.String</span></span>

## <span data-ttu-id="67055-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67055-142">OUTPUTS</span></span>

### <span data-ttu-id="67055-143">Microsoft. Azure. Commands. platforming. models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67055-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="67055-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67055-144">NOTES</span></span>

## <span data-ttu-id="67055-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67055-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

