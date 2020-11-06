---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: 29a7c2d3bb2060b77871cea0c088c50a59197cb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526813"
---
# <span data-ttu-id="03681-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="03681-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="03681-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03681-102">SYNOPSIS</span></span>
<span data-ttu-id="03681-103">Umożliwia odkrycie usuniętego klucza w magazynie kluczy w aktywnym stanie.</span><span class="sxs-lookup"><span data-stu-id="03681-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03681-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03681-104">SYNTAX</span></span>

### <span data-ttu-id="03681-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="03681-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03681-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="03681-106">InputObject</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03681-107">Opis</span><span class="sxs-lookup"><span data-stu-id="03681-107">DESCRIPTION</span></span>
<span data-ttu-id="03681-108">Polecenie cmdlet **Undo-AzureKeyVaultKeyRemoval** powoduje odzyskanie uprzednio usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="03681-108">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="03681-109">Odzyskany klucz jest aktywny i będzie można go użyć do wszystkich zwykłych operacji kluczowych.</span><span class="sxs-lookup"><span data-stu-id="03681-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="03681-110">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="03681-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="03681-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03681-111">EXAMPLES</span></span>

### <span data-ttu-id="03681-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03681-112">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="03681-113">To polecenie odzyska klucz "MyKey", który został wcześniej usunięty, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="03681-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="03681-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03681-114">PARAMETERS</span></span>

### <span data-ttu-id="03681-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03681-115">-DefaultProfile</span></span>
<span data-ttu-id="03681-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="03681-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03681-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03681-117">-InputObject</span></span>
<span data-ttu-id="03681-118">Usunięto obiekt klucza</span><span class="sxs-lookup"><span data-stu-id="03681-118">Deleted key object</span></span>

```yaml
Type: PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03681-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03681-119">-Name</span></span>
<span data-ttu-id="03681-120">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="03681-120">Key name.</span></span>
<span data-ttu-id="03681-121">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwy magazynu, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="03681-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03681-122">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="03681-122">-VaultName</span></span>
<span data-ttu-id="03681-123">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="03681-123">Vault name.</span></span>
<span data-ttu-id="03681-124">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="03681-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03681-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03681-125">-Confirm</span></span>
<span data-ttu-id="03681-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03681-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03681-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03681-127">-WhatIf</span></span>
<span data-ttu-id="03681-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03681-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03681-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03681-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03681-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03681-130">CommonParameters</span></span>
<span data-ttu-id="03681-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03681-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03681-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03681-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03681-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03681-133">INPUTS</span></span>

### <span data-ttu-id="03681-134">System. String</span><span class="sxs-lookup"><span data-stu-id="03681-134">System.String</span></span>

## <span data-ttu-id="03681-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03681-135">OUTPUTS</span></span>

### <span data-ttu-id="03681-136">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="03681-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="03681-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03681-137">NOTES</span></span>

## <span data-ttu-id="03681-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03681-138">RELATED LINKS</span></span>

[<span data-ttu-id="03681-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="03681-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="03681-140">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="03681-140">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="03681-141">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="03681-141">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

