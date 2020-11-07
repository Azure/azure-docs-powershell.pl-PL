---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: 5b0e67fbbead536803dba8efeb2c8a61d7f75c5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892998"
---
# <span data-ttu-id="e3167-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="e3167-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="e3167-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3167-102">SYNOPSIS</span></span>
<span data-ttu-id="e3167-103">Umożliwia odkrycie usuniętego klucza w magazynie kluczy w aktywnym stanie.</span><span class="sxs-lookup"><span data-stu-id="e3167-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="e3167-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3167-104">SYNTAX</span></span>

```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3167-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3167-105">DESCRIPTION</span></span>
<span data-ttu-id="e3167-106">Polecenie cmdlet **Undo-AzKeyVaultKeyRemoval** powoduje odzyskanie uprzednio usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="e3167-106">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="e3167-107">Odzyskany klucz jest aktywny i będzie można go użyć do wszystkich zwykłych operacji kluczowych.</span><span class="sxs-lookup"><span data-stu-id="e3167-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="e3167-108">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="e3167-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="e3167-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3167-109">EXAMPLES</span></span>

### <span data-ttu-id="e3167-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e3167-110">Example 1</span></span>
```
PS C:\>Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="e3167-111">To polecenie odzyska klucz "MyKey", który został wcześniej usunięty, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="e3167-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="e3167-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3167-112">PARAMETERS</span></span>

### <span data-ttu-id="e3167-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3167-113">-DefaultProfile</span></span>
<span data-ttu-id="e3167-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e3167-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3167-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e3167-115">-Name</span></span>
<span data-ttu-id="e3167-116">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="e3167-116">Key name.</span></span>
<span data-ttu-id="e3167-117">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwy magazynu, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="e3167-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3167-118">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="e3167-118">-VaultName</span></span>
<span data-ttu-id="e3167-119">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="e3167-119">Vault name.</span></span>
<span data-ttu-id="e3167-120">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="e3167-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e3167-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3167-121">-Confirm</span></span>
<span data-ttu-id="e3167-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3167-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3167-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3167-123">-WhatIf</span></span>
<span data-ttu-id="e3167-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3167-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3167-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e3167-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3167-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3167-126">CommonParameters</span></span>
<span data-ttu-id="e3167-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3167-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3167-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3167-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3167-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3167-129">INPUTS</span></span>

### <span data-ttu-id="e3167-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e3167-130">System.String</span></span>

## <span data-ttu-id="e3167-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3167-131">OUTPUTS</span></span>

### <span data-ttu-id="e3167-132">Microsoft. Azure. Commands. platforming. MODELES.</span><span class="sxs-lookup"><span data-stu-id="e3167-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="e3167-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3167-133">NOTES</span></span>

## <span data-ttu-id="e3167-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3167-134">RELATED LINKS</span></span>

[<span data-ttu-id="e3167-135">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e3167-135">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="e3167-136">Dodaj-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e3167-136">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="e3167-137">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e3167-137">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

