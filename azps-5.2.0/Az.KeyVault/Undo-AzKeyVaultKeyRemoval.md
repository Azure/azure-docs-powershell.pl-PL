---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: d6637b8c180dd2ef25bdba5326f0a42a364bc8ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335050"
---
# <span data-ttu-id="10cf9-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="10cf9-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="10cf9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="10cf9-103">Umożliwia odkrycie usuniętego klucza w magazynie kluczy w aktywnym stanie.</span><span class="sxs-lookup"><span data-stu-id="10cf9-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="10cf9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10cf9-104">SYNTAX</span></span>

### <span data-ttu-id="10cf9-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="10cf9-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10cf9-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="10cf9-106">HsmInteractive</span></span>
```
Undo-AzKeyVaultKeyRemoval -HsmName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10cf9-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="10cf9-107">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10cf9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="10cf9-108">DESCRIPTION</span></span>
<span data-ttu-id="10cf9-109">Polecenie cmdlet **Undo-AzKeyVaultKeyRemoval** powoduje odzyskanie uprzednio usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="10cf9-109">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="10cf9-110">Odzyskany klucz jest aktywny i będzie można go użyć do wszystkich zwykłych operacji kluczowych.</span><span class="sxs-lookup"><span data-stu-id="10cf9-110">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="10cf9-111">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="10cf9-111">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="10cf9-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10cf9-112">EXAMPLES</span></span>

### <span data-ttu-id="10cf9-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10cf9-113">Example 1</span></span>
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

<span data-ttu-id="10cf9-114">To polecenie odzyska klucz "MyKey", który został wcześniej usunięty, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="10cf9-114">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="10cf9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10cf9-115">PARAMETERS</span></span>

### <span data-ttu-id="10cf9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10cf9-116">-DefaultProfile</span></span>
<span data-ttu-id="10cf9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="10cf9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10cf9-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="10cf9-118">-HsmName</span></span>
<span data-ttu-id="10cf9-119">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="10cf9-119">HSM name.</span></span> <span data-ttu-id="10cf9-120">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="10cf9-120">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cf9-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="10cf9-121">-InputObject</span></span>
<span data-ttu-id="10cf9-122">Usunięto obiekt klucza</span><span class="sxs-lookup"><span data-stu-id="10cf9-122">Deleted key object</span></span>

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

### <span data-ttu-id="10cf9-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10cf9-123">-Name</span></span>
<span data-ttu-id="10cf9-124">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="10cf9-124">Key name.</span></span>
<span data-ttu-id="10cf9-125">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwy magazynu, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="10cf9-125">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cf9-126">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="10cf9-126">-VaultName</span></span>
<span data-ttu-id="10cf9-127">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="10cf9-127">Vault name.</span></span>
<span data-ttu-id="10cf9-128">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="10cf9-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="10cf9-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10cf9-129">-Confirm</span></span>
<span data-ttu-id="10cf9-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10cf9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10cf9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10cf9-131">-WhatIf</span></span>
<span data-ttu-id="10cf9-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10cf9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10cf9-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="10cf9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10cf9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10cf9-134">CommonParameters</span></span>
<span data-ttu-id="10cf9-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10cf9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10cf9-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10cf9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10cf9-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10cf9-137">INPUTS</span></span>

### <span data-ttu-id="10cf9-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="10cf9-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="10cf9-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10cf9-139">OUTPUTS</span></span>

### <span data-ttu-id="10cf9-140">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="10cf9-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="10cf9-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10cf9-141">NOTES</span></span>

## <span data-ttu-id="10cf9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10cf9-142">RELATED LINKS</span></span>

[<span data-ttu-id="10cf9-143">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="10cf9-143">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="10cf9-144">Dodaj-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="10cf9-144">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="10cf9-145">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="10cf9-145">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

