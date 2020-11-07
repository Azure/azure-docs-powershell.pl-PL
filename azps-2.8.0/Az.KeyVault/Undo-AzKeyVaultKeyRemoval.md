---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: ff4682a7c97f721dac9fb53f375c2a96f4bb33b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705103"
---
# <span data-ttu-id="ab205-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="ab205-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="ab205-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab205-102">SYNOPSIS</span></span>
<span data-ttu-id="ab205-103">Umożliwia odkrycie usuniętego klucza w magazynie kluczy w aktywnym stanie.</span><span class="sxs-lookup"><span data-stu-id="ab205-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="ab205-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab205-104">SYNTAX</span></span>

### <span data-ttu-id="ab205-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ab205-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab205-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="ab205-106">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab205-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ab205-107">DESCRIPTION</span></span>
<span data-ttu-id="ab205-108">Polecenie cmdlet **Undo-AzKeyVaultKeyRemoval** powoduje odzyskanie uprzednio usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="ab205-108">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="ab205-109">Odzyskany klucz jest aktywny i będzie można go użyć do wszystkich zwykłych operacji kluczowych.</span><span class="sxs-lookup"><span data-stu-id="ab205-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="ab205-110">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="ab205-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="ab205-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab205-111">EXAMPLES</span></span>

### <span data-ttu-id="ab205-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab205-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

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

<span data-ttu-id="ab205-113">To polecenie odzyska klucz "MyKey", który został wcześniej usunięty, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="ab205-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="ab205-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab205-114">PARAMETERS</span></span>

### <span data-ttu-id="ab205-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab205-115">-DefaultProfile</span></span>
<span data-ttu-id="ab205-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ab205-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab205-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ab205-117">-InputObject</span></span>
<span data-ttu-id="ab205-118">Usunięto obiekt klucza</span><span class="sxs-lookup"><span data-stu-id="ab205-118">Deleted key object</span></span>

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

### <span data-ttu-id="ab205-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ab205-119">-Name</span></span>
<span data-ttu-id="ab205-120">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="ab205-120">Key name.</span></span>
<span data-ttu-id="ab205-121">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwy magazynu, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="ab205-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="ab205-122">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="ab205-122">-VaultName</span></span>
<span data-ttu-id="ab205-123">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="ab205-123">Vault name.</span></span>
<span data-ttu-id="ab205-124">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="ab205-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ab205-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab205-125">-Confirm</span></span>
<span data-ttu-id="ab205-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab205-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab205-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab205-127">-WhatIf</span></span>
<span data-ttu-id="ab205-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab205-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab205-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab205-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab205-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab205-130">CommonParameters</span></span>
<span data-ttu-id="ab205-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab205-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab205-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab205-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab205-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab205-133">INPUTS</span></span>

### <span data-ttu-id="ab205-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ab205-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="ab205-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab205-135">OUTPUTS</span></span>

### <span data-ttu-id="ab205-136">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ab205-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="ab205-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab205-137">NOTES</span></span>

## <span data-ttu-id="ab205-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab205-138">RELATED LINKS</span></span>

[<span data-ttu-id="ab205-139">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ab205-139">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="ab205-140">Dodaj-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ab205-140">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="ab205-141">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ab205-141">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

