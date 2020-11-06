---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: 6de9fecc4b9576f9d69ddc1f963ae537f4422371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552787"
---
# <span data-ttu-id="038fc-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="038fc-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="038fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="038fc-102">SYNOPSIS</span></span>
<span data-ttu-id="038fc-103">Umożliwia odkrycie usuniętego klucza w magazynie kluczy w aktywnym stanie.</span><span class="sxs-lookup"><span data-stu-id="038fc-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="038fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="038fc-104">SYNTAX</span></span>

### <span data-ttu-id="038fc-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="038fc-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="038fc-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="038fc-106">InputObject</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="038fc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="038fc-107">DESCRIPTION</span></span>
<span data-ttu-id="038fc-108">Polecenie cmdlet **Undo-AzureKeyVaultKeyRemoval** powoduje odzyskanie uprzednio usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="038fc-108">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="038fc-109">Odzyskany klucz jest aktywny i będzie można go użyć do wszystkich zwykłych operacji kluczowych.</span><span class="sxs-lookup"><span data-stu-id="038fc-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="038fc-110">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="038fc-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="038fc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="038fc-111">EXAMPLES</span></span>

### <span data-ttu-id="038fc-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="038fc-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="038fc-113">To polecenie odzyska klucz "MyKey", który został wcześniej usunięty, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="038fc-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="038fc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="038fc-114">PARAMETERS</span></span>

### <span data-ttu-id="038fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="038fc-115">-DefaultProfile</span></span>
<span data-ttu-id="038fc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="038fc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="038fc-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="038fc-117">-InputObject</span></span>
<span data-ttu-id="038fc-118">Usunięto obiekt klucza</span><span class="sxs-lookup"><span data-stu-id="038fc-118">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="038fc-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="038fc-119">-Name</span></span>
<span data-ttu-id="038fc-120">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="038fc-120">Key name.</span></span>
<span data-ttu-id="038fc-121">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwy magazynu, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="038fc-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="038fc-122">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="038fc-122">-VaultName</span></span>
<span data-ttu-id="038fc-123">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="038fc-123">Vault name.</span></span>
<span data-ttu-id="038fc-124">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="038fc-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="038fc-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="038fc-125">-Confirm</span></span>
<span data-ttu-id="038fc-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="038fc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="038fc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="038fc-127">-WhatIf</span></span>
<span data-ttu-id="038fc-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="038fc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="038fc-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="038fc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="038fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="038fc-130">CommonParameters</span></span>
<span data-ttu-id="038fc-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="038fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="038fc-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="038fc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="038fc-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="038fc-133">INPUTS</span></span>

### <span data-ttu-id="038fc-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="038fc-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="038fc-135">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="038fc-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="038fc-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="038fc-136">OUTPUTS</span></span>

### <span data-ttu-id="038fc-137">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="038fc-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="038fc-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="038fc-138">NOTES</span></span>

## <span data-ttu-id="038fc-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="038fc-139">RELATED LINKS</span></span>

[<span data-ttu-id="038fc-140">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="038fc-140">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="038fc-141">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="038fc-141">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="038fc-142">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="038fc-142">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

