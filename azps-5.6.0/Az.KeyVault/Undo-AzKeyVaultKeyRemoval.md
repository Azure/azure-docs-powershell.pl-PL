---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: 9de4cc6572a20dc9ec241c6f93cb035162b914f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012058"
---
# <span data-ttu-id="29ad6-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="29ad6-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="29ad6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="29ad6-103">Przywraca usunięty klucz z magazynu kluczy do stanu aktywnego.</span><span class="sxs-lookup"><span data-stu-id="29ad6-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="29ad6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="29ad6-104">SYNTAX</span></span>

### <span data-ttu-id="29ad6-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="29ad6-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29ad6-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="29ad6-106">HsmInteractive</span></span>
```
Undo-AzKeyVaultKeyRemoval -HsmName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29ad6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="29ad6-107">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29ad6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="29ad6-108">DESCRIPTION</span></span>
<span data-ttu-id="29ad6-109">Polecenie **cmdlet Undo-AzKeyVaultKeyRemoval** spowoduje odzyskanie poprzednio usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="29ad6-109">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="29ad6-110">Odzyskany klucz będzie aktywny i będzie można go używać we wszystkich operacjach klucza normalnego.</span><span class="sxs-lookup"><span data-stu-id="29ad6-110">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="29ad6-111">Aby wykonać tę operację, dzwoniący musi mieć uprawnienie do odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="29ad6-111">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="29ad6-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="29ad6-112">EXAMPLES</span></span>

### <span data-ttu-id="29ad6-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="29ad6-113">Example 1</span></span>
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

<span data-ttu-id="29ad6-114">To polecenie spowoduje odzyskanie poprzednio usuniętego klucza "Mój Klucz" w stanie aktywnym i użytecznym.</span><span class="sxs-lookup"><span data-stu-id="29ad6-114">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="29ad6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29ad6-115">PARAMETERS</span></span>

### <span data-ttu-id="29ad6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ad6-116">-DefaultProfile</span></span>
<span data-ttu-id="29ad6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="29ad6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29ad6-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="29ad6-118">-HsmName</span></span>
<span data-ttu-id="29ad6-119">Nazwa HSM.</span><span class="sxs-lookup"><span data-stu-id="29ad6-119">HSM name.</span></span> <span data-ttu-id="29ad6-120">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="29ad6-120">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="29ad6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29ad6-121">-InputObject</span></span>
<span data-ttu-id="29ad6-122">Usunięto obiekt klucza</span><span class="sxs-lookup"><span data-stu-id="29ad6-122">Deleted key object</span></span>

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

### <span data-ttu-id="29ad6-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="29ad6-123">-Name</span></span>
<span data-ttu-id="29ad6-124">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="29ad6-124">Key name.</span></span>
<span data-ttu-id="29ad6-125">Polecenie cmdlet konstruuje nazwę FQDN klucza z nazwy magazynu, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="29ad6-125">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="29ad6-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="29ad6-126">-VaultName</span></span>
<span data-ttu-id="29ad6-127">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="29ad6-127">Vault name.</span></span>
<span data-ttu-id="29ad6-128">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="29ad6-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="29ad6-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29ad6-129">-Confirm</span></span>
<span data-ttu-id="29ad6-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="29ad6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29ad6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29ad6-131">-WhatIf</span></span>
<span data-ttu-id="29ad6-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29ad6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29ad6-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="29ad6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29ad6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ad6-134">CommonParameters</span></span>
<span data-ttu-id="29ad6-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29ad6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ad6-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29ad6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ad6-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29ad6-137">INPUTS</span></span>

### <span data-ttu-id="29ad6-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="29ad6-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="29ad6-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29ad6-139">OUTPUTS</span></span>

### <span data-ttu-id="29ad6-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="29ad6-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="29ad6-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="29ad6-141">NOTES</span></span>

## <span data-ttu-id="29ad6-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29ad6-142">RELATED LINKS</span></span>

[<span data-ttu-id="29ad6-143">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="29ad6-143">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="29ad6-144">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="29ad6-144">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="29ad6-145">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="29ad6-145">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

