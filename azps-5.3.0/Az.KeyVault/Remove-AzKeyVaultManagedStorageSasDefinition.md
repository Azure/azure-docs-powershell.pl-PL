---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500914"
---
# <span data-ttu-id="b254b-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="b254b-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="b254b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b254b-102">SYNOPSIS</span></span>
<span data-ttu-id="b254b-103">Usuwa definicje SAS magazynu kluczy zarządzane w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b254b-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="b254b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b254b-104">SYNTAX</span></span>

### <span data-ttu-id="b254b-105">ByDefinitionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b254b-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b254b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b254b-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b254b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b254b-107">DESCRIPTION</span></span>
<span data-ttu-id="b254b-108">Usuwa definicje SAS magazynu kluczy zarządzane w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b254b-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="b254b-109">Spowoduje to również usunięcie klucza tajnego użytego do uzyskania tokenu SAS dla tej definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="b254b-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="b254b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b254b-110">EXAMPLES</span></span>

### <span data-ttu-id="b254b-111">Przykład 1: usuwanie definicji skojarzeń SAS magazynu kluczy zarządzanych w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b254b-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="b254b-112">Usuwa definicję SAS magazynu zarządzanego w magazynie kluczy "mysasdef" skojarzoną z kontem "mystorageaccount" w magazynie magazynu ".</span><span class="sxs-lookup"><span data-stu-id="b254b-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="b254b-113">Przykład 2: usuwanie definicji skojarzeń SAS magazynu kluczy zarządzanego w usłudze Azure bez potwierdzenia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b254b-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="b254b-114">Usuwa definicję SAS magazynu zarządzanego w magazynie kluczy "mysasdef" skojarzoną z kontem "mystorageaccount" w magazynie magazynu ".</span><span class="sxs-lookup"><span data-stu-id="b254b-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="b254b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b254b-115">PARAMETERS</span></span>

### <span data-ttu-id="b254b-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b254b-116">-AccountName</span></span>
<span data-ttu-id="b254b-117">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b254b-117">Storage account name.</span></span>
<span data-ttu-id="b254b-118">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranej nazwy konta środowiska i magazynu.</span><span class="sxs-lookup"><span data-stu-id="b254b-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b254b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b254b-119">-DefaultProfile</span></span>
<span data-ttu-id="b254b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b254b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b254b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b254b-121">-Force</span></span>
<span data-ttu-id="b254b-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b254b-122">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b254b-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b254b-123">-InputObject</span></span>
<span data-ttu-id="b254b-124">Obiekt ManagedStorageSasDefinition.</span><span class="sxs-lookup"><span data-stu-id="b254b-124">ManagedStorageSasDefinition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b254b-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b254b-125">-Name</span></span>
<span data-ttu-id="b254b-126">Nazwa definicji SAS magazynu.</span><span class="sxs-lookup"><span data-stu-id="b254b-126">Storage sas definition name.</span></span>
<span data-ttu-id="b254b-127">Polecenie cmdlet tworzy nazwę FQDN definicji SAS magazynu danych na podstawie nazwy magazynu, obecnie wybranego środowiska, nazwy konta magazynu i nazwy definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="b254b-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b254b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b254b-128">-PassThru</span></span>
<span data-ttu-id="b254b-129">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="b254b-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b254b-130">Jeśli ten przełącznik jest określony, polecenie cmdlet zwróci konto zarządzanego magazynu, które zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="b254b-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b254b-131">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="b254b-131">-VaultName</span></span>
<span data-ttu-id="b254b-132">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="b254b-132">Vault name.</span></span>
<span data-ttu-id="b254b-133">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="b254b-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b254b-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b254b-134">-Confirm</span></span>
<span data-ttu-id="b254b-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b254b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b254b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b254b-136">-WhatIf</span></span>
<span data-ttu-id="b254b-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b254b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b254b-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b254b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b254b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b254b-139">CommonParameters</span></span>
<span data-ttu-id="b254b-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b254b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b254b-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b254b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b254b-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b254b-142">INPUTS</span></span>

### <span data-ttu-id="b254b-143">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b254b-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="b254b-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b254b-144">OUTPUTS</span></span>

### <span data-ttu-id="b254b-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="b254b-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="b254b-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b254b-146">NOTES</span></span>

## <span data-ttu-id="b254b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b254b-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

