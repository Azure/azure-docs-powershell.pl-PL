---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: ff7dea63b4731b4a2a6becfc31d0b312345978bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977002"
---
# <span data-ttu-id="ecb91-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="ecb91-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="ecb91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecb91-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb91-103">Przywraca usunięty magazyn kluczy do stanu aktywnego.</span><span class="sxs-lookup"><span data-stu-id="ecb91-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="ecb91-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ecb91-104">SYNTAX</span></span>

### <span data-ttu-id="ecb91-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ecb91-105">Default (Default)</span></span>
```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecb91-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ecb91-106">InputObject</span></span>
```
Undo-AzKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecb91-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ecb91-107">DESCRIPTION</span></span>
<span data-ttu-id="ecb91-108">Polecenie **cmdlet Undo-AzKeyVaultRemoval** spowoduje odzyskanie poprzednio usuniętego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="ecb91-108">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="ecb91-109">Odzyskany magazyn będzie aktywny po odzyskaniu</span><span class="sxs-lookup"><span data-stu-id="ecb91-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="ecb91-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ecb91-110">EXAMPLES</span></span>

### <span data-ttu-id="ecb91-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ecb91-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

Vault Name                       : MyKeyVault
Resource Group Name              : MyResourceGroup
Location                         : eastus2
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers
                                   /Microsoft.KeyVault/vaults/mykeyvault
Vault URI                        : https://mykeyvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : True
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update

Tags                             :
                                   Name  Value
                                   ====  =====
                                   x     y
```

<span data-ttu-id="ecb91-112">To polecenie spowoduje odzyskanie magazynu kluczy "MyKeyVault", który został wcześniej usunięty z regionu Eastus2 i grupy zasobów "MyResourceGroup", w stanie aktywnym i użytecznym.</span><span class="sxs-lookup"><span data-stu-id="ecb91-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="ecb91-113">Ponadto zastępuje tagi nowym tagiem.</span><span class="sxs-lookup"><span data-stu-id="ecb91-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="ecb91-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecb91-114">PARAMETERS</span></span>

### <span data-ttu-id="ecb91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb91-115">-DefaultProfile</span></span>
<span data-ttu-id="ecb91-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ecb91-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecb91-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecb91-117">-InputObject</span></span>
<span data-ttu-id="ecb91-118">Usunięto obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="ecb91-118">Deleted vault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb91-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ecb91-119">-Location</span></span>
<span data-ttu-id="ecb91-120">Określa oryginalny magazyn usunięty na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ecb91-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb91-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecb91-121">-ResourceGroupName</span></span>
<span data-ttu-id="ecb91-122">Określa nazwę istniejącej grupy zasobów, w której ma być tworzyć magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="ecb91-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb91-123">— Tag</span><span class="sxs-lookup"><span data-stu-id="ecb91-123">-Tag</span></span>
<span data-ttu-id="ecb91-124">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="ecb91-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ecb91-125">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ecb91-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb91-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ecb91-126">-VaultName</span></span>
<span data-ttu-id="ecb91-127">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="ecb91-127">Vault name.</span></span>
<span data-ttu-id="ecb91-128">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="ecb91-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ecb91-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ecb91-129">-Confirm</span></span>
<span data-ttu-id="ecb91-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ecb91-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecb91-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecb91-131">-WhatIf</span></span>
<span data-ttu-id="ecb91-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecb91-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecb91-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ecb91-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecb91-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb91-134">CommonParameters</span></span>
<span data-ttu-id="ecb91-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecb91-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb91-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecb91-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb91-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecb91-137">INPUTS</span></span>

### <span data-ttu-id="ecb91-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="ecb91-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="ecb91-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecb91-139">OUTPUTS</span></span>

### <span data-ttu-id="ecb91-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ecb91-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="ecb91-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ecb91-141">NOTES</span></span>

## <span data-ttu-id="ecb91-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ecb91-142">RELATED LINKS</span></span>

[<span data-ttu-id="ecb91-143">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ecb91-143">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="ecb91-144">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ecb91-144">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="ecb91-145">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ecb91-145">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
