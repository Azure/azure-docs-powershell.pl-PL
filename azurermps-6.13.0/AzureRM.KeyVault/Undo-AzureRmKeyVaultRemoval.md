---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: af6ed0e4db688cdc9ad6da598c0bc240e9b3c958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545187"
---
# <span data-ttu-id="9da5a-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="9da5a-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="9da5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9da5a-102">SYNOPSIS</span></span>
<span data-ttu-id="9da5a-103">Odkrycie usuniętego magazynu kluczy w stanie aktywnym.</span><span class="sxs-lookup"><span data-stu-id="9da5a-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9da5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9da5a-104">SYNTAX</span></span>

### <span data-ttu-id="9da5a-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9da5a-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9da5a-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="9da5a-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9da5a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9da5a-107">DESCRIPTION</span></span>
<span data-ttu-id="9da5a-108">Polecenie cmdlet **Undo-AzureRmKeyVaultRemoval** powoduje odzyskanie uprzednio usuniętego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="9da5a-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="9da5a-109">Odzyskany magazyn będzie aktywny po odzyskaniu</span><span class="sxs-lookup"><span data-stu-id="9da5a-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="9da5a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9da5a-110">EXAMPLES</span></span>

### <span data-ttu-id="9da5a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9da5a-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

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

<span data-ttu-id="9da5a-112">To polecenie odzyska Magazyn kluczy "MyKeyVault", który został wcześniej usunięty z obszaru eastus2 i grupy zasobów "moja grupa zasobów", w stan aktywny i dostępny.</span><span class="sxs-lookup"><span data-stu-id="9da5a-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="9da5a-113">Znaczniki są również zastępowane nowym znacznikiem.</span><span class="sxs-lookup"><span data-stu-id="9da5a-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="9da5a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9da5a-114">PARAMETERS</span></span>

### <span data-ttu-id="9da5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da5a-115">-DefaultProfile</span></span>
<span data-ttu-id="9da5a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9da5a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9da5a-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9da5a-117">-InputObject</span></span>
<span data-ttu-id="9da5a-118">Usunięto obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="9da5a-118">Deleted vault object</span></span>

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

### <span data-ttu-id="9da5a-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9da5a-119">-Location</span></span>
<span data-ttu-id="9da5a-120">Określa oryginalny region usługi Azure w magazynie usunięty.</span><span class="sxs-lookup"><span data-stu-id="9da5a-120">Specifies the deleted vault original Azure region.</span></span>

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

### <span data-ttu-id="9da5a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9da5a-121">-ResourceGroupName</span></span>
<span data-ttu-id="9da5a-122">Określa nazwę istniejącej grupy zasobów, w której ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="9da5a-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="9da5a-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="9da5a-123">-Tag</span></span>
<span data-ttu-id="9da5a-124">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9da5a-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9da5a-125">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="9da5a-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9da5a-126">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="9da5a-126">-VaultName</span></span>
<span data-ttu-id="9da5a-127">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="9da5a-127">Vault name.</span></span>
<span data-ttu-id="9da5a-128">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="9da5a-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9da5a-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9da5a-129">-Confirm</span></span>
<span data-ttu-id="9da5a-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9da5a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9da5a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9da5a-131">-WhatIf</span></span>
<span data-ttu-id="9da5a-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9da5a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9da5a-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9da5a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9da5a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da5a-134">CommonParameters</span></span>
<span data-ttu-id="9da5a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da5a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da5a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9da5a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da5a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9da5a-137">INPUTS</span></span>

### <span data-ttu-id="9da5a-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="9da5a-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>
<span data-ttu-id="9da5a-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9da5a-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9da5a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9da5a-140">OUTPUTS</span></span>

### <span data-ttu-id="9da5a-141">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9da5a-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="9da5a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9da5a-142">NOTES</span></span>

## <span data-ttu-id="9da5a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9da5a-143">RELATED LINKS</span></span>

[<span data-ttu-id="9da5a-144">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9da5a-144">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="9da5a-145">Nowe — AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9da5a-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="9da5a-146">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9da5a-146">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
