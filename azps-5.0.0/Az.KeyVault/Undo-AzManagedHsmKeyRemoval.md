---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azmanagedhsmkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
ms.openlocfilehash: be1713584a1d0ce897c1c728f6aa7ae8b6ca3255
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224246"
---
# <span data-ttu-id="d0e82-101">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="d0e82-101">Undo-AzManagedHsmKeyRemoval</span></span>

## <span data-ttu-id="d0e82-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0e82-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e82-103">Przywraca usunięty klucz z zarządzanego modułu HSM do stanu aktywnego.</span><span class="sxs-lookup"><span data-stu-id="d0e82-103">Recovers a deleted key in a managed HSM into an active state.</span></span>

## <span data-ttu-id="d0e82-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0e82-104">SYNTAX</span></span>

### <span data-ttu-id="d0e82-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d0e82-105">Default (Default)</span></span>
```
Undo-AzManagedHsmKeyRemoval [-HsmName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0e82-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="d0e82-106">InputObject</span></span>
```
Undo-AzManagedHsmKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0e82-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d0e82-107">DESCRIPTION</span></span>
<span data-ttu-id="d0e82-108">Polecenie cmdlet **Undo-AzManagedHsmKeyRemoval** powoduje odzyskanie uprzednio usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="d0e82-108">The **Undo-AzManagedHsmKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="d0e82-109">Odzyskany klucz jest aktywny i będzie można go użyć do wszystkich zwykłych operacji kluczowych.</span><span class="sxs-lookup"><span data-stu-id="d0e82-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="d0e82-110">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="d0e82-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="d0e82-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0e82-111">EXAMPLES</span></span>

### <span data-ttu-id="d0e82-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d0e82-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzManagedHsmKeyRemoval -HsmName testmhsm -Name testkey001

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="d0e82-113">To polecenie odzyska klucz "testkey001", który został wcześniej usunięty, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="d0e82-113">This command will recover the key 'testkey001' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="d0e82-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0e82-114">PARAMETERS</span></span>

### <span data-ttu-id="d0e82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e82-115">-DefaultProfile</span></span>
<span data-ttu-id="d0e82-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0e82-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0e82-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="d0e82-117">-HsmName</span></span>
<span data-ttu-id="d0e82-118">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="d0e82-118">HSM name.</span></span> <span data-ttu-id="d0e82-119">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="d0e82-119">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d0e82-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d0e82-120">-InputObject</span></span>
<span data-ttu-id="d0e82-121">Usunięto obiekt klucza</span><span class="sxs-lookup"><span data-stu-id="d0e82-121">Deleted key object</span></span>

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

### <span data-ttu-id="d0e82-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0e82-122">-Name</span></span>
<span data-ttu-id="d0e82-123">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="d0e82-123">Key name.</span></span>
<span data-ttu-id="d0e82-124">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwa zarządzanego modułu HSM, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="d0e82-124">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="d0e82-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0e82-125">-Confirm</span></span>
<span data-ttu-id="d0e82-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0e82-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0e82-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0e82-127">-WhatIf</span></span>
<span data-ttu-id="d0e82-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0e82-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0e82-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d0e82-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0e82-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e82-130">CommonParameters</span></span>
<span data-ttu-id="d0e82-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e82-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e82-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0e82-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e82-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0e82-133">INPUTS</span></span>

### <span data-ttu-id="d0e82-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d0e82-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="d0e82-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0e82-135">OUTPUTS</span></span>

### <span data-ttu-id="d0e82-136">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d0e82-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="d0e82-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0e82-137">NOTES</span></span>

## <span data-ttu-id="d0e82-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0e82-138">RELATED LINKS</span></span>

[<span data-ttu-id="d0e82-139">Dodaj-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d0e82-139">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="d0e82-140">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d0e82-140">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="d0e82-141">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d0e82-141">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="d0e82-142">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d0e82-142">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)

[<span data-ttu-id="d0e82-143">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d0e82-143">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="d0e82-144">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d0e82-144">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)