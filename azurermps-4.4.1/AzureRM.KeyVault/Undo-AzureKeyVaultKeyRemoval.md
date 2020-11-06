---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: df29d88fbac1a8d2dc382522e24ff143cf075573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553239"
---
# <span data-ttu-id="88dfc-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="88dfc-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="88dfc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="88dfc-103">Umożliwia odkrycie usuniętego klucza w magazynie kluczy w aktywnym stanie.</span><span class="sxs-lookup"><span data-stu-id="88dfc-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88dfc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88dfc-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88dfc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="88dfc-106">Polecenie cmdlet **Undo-AzureKeyVaultKeyRemoval** powoduje odzyskanie uprzednio usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="88dfc-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="88dfc-107">Odzyskany klucz jest aktywny i będzie można go użyć do wszystkich zwykłych operacji kluczowych.</span><span class="sxs-lookup"><span data-stu-id="88dfc-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="88dfc-108">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="88dfc-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="88dfc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88dfc-109">EXAMPLES</span></span>

### <span data-ttu-id="88dfc-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88dfc-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="88dfc-111">To polecenie odzyska klucz "MyKey", który został wcześniej usunięty, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="88dfc-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="88dfc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88dfc-112">PARAMETERS</span></span>

### <span data-ttu-id="88dfc-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88dfc-113">-Name</span></span>
<span data-ttu-id="88dfc-114">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="88dfc-114">Key name.</span></span>
<span data-ttu-id="88dfc-115">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwy magazynu, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="88dfc-115">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88dfc-116">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="88dfc-116">-VaultName</span></span>
<span data-ttu-id="88dfc-117">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="88dfc-117">Vault name.</span></span>
<span data-ttu-id="88dfc-118">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="88dfc-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88dfc-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88dfc-119">-Confirm</span></span>
<span data-ttu-id="88dfc-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88dfc-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88dfc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88dfc-121">-WhatIf</span></span>
<span data-ttu-id="88dfc-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88dfc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88dfc-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88dfc-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88dfc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88dfc-124">-DefaultProfile</span></span>
<span data-ttu-id="88dfc-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88dfc-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88dfc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88dfc-126">CommonParameters</span></span>
<span data-ttu-id="88dfc-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88dfc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88dfc-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88dfc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88dfc-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88dfc-129">INPUTS</span></span>

### <span data-ttu-id="88dfc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="88dfc-130">System.String</span></span>

## <span data-ttu-id="88dfc-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88dfc-131">OUTPUTS</span></span>

### <span data-ttu-id="88dfc-132">Microsoft. Azure. Commands. platforming. MODELES.</span><span class="sxs-lookup"><span data-stu-id="88dfc-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="88dfc-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88dfc-133">NOTES</span></span>

## <span data-ttu-id="88dfc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88dfc-134">RELATED LINKS</span></span>

[<span data-ttu-id="88dfc-135">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="88dfc-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="88dfc-136">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="88dfc-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="88dfc-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="88dfc-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

