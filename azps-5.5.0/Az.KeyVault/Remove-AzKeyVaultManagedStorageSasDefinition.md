---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192347"
---
# <span data-ttu-id="781da-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="781da-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="781da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="781da-102">SYNOPSIS</span></span>
<span data-ttu-id="781da-103">Usuwa definicje SAS magazynu zarządzanego przez magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="781da-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="781da-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="781da-104">SYNTAX</span></span>

### <span data-ttu-id="781da-105">ByDefinitionName (Default)</span><span class="sxs-lookup"><span data-stu-id="781da-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="781da-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="781da-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="781da-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="781da-107">DESCRIPTION</span></span>
<span data-ttu-id="781da-108">Usuwa definicje SAS magazynu zarządzanego przez magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="781da-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="781da-109">Usuwa to także tajny klucz używany do uzyskania tokenu SAS na tę definicję sas.</span><span class="sxs-lookup"><span data-stu-id="781da-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="781da-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="781da-110">EXAMPLES</span></span>

### <span data-ttu-id="781da-111">Przykład 1. Usuwanie zarządzanej definicji SAS magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="781da-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
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

<span data-ttu-id="781da-112">Usuwa definicję sas sas magazynu zarządzanego magazynem magazynu "mysasdef" skojarzoną z kontem "mystorageaccount" w magazynie "myvault".</span><span class="sxs-lookup"><span data-stu-id="781da-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="781da-113">Przykład 2. Usuwanie zarządzanej definicji SAS magazynu platformy Azure bez potwierdzenia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="781da-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
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

<span data-ttu-id="781da-114">Usuwa definicję sas sas magazynu zarządzanego magazynem magazynu "mysasdef" skojarzoną z kontem "mystorageaccount" w magazynie "myvault".</span><span class="sxs-lookup"><span data-stu-id="781da-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="781da-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="781da-115">PARAMETERS</span></span>

### <span data-ttu-id="781da-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="781da-116">-AccountName</span></span>
<span data-ttu-id="781da-117">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="781da-117">Storage account name.</span></span>
<span data-ttu-id="781da-118">Polecenie cmdlet konstruuje nazwę FQDN zarządzanego konta magazynu z nazwy magazynu, obecnie wybranego środowiska i nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="781da-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="781da-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="781da-119">-DefaultProfile</span></span>
<span data-ttu-id="781da-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="781da-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="781da-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="781da-121">-Force</span></span>
<span data-ttu-id="781da-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="781da-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="781da-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="781da-123">-InputObject</span></span>
<span data-ttu-id="781da-124">Obiekt ManagedStorageSasDefinition.</span><span class="sxs-lookup"><span data-stu-id="781da-124">ManagedStorageSasDefinition object.</span></span>

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

### <span data-ttu-id="781da-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="781da-125">-Name</span></span>
<span data-ttu-id="781da-126">Nazwa definicji sas magazynu.</span><span class="sxs-lookup"><span data-stu-id="781da-126">Storage sas definition name.</span></span>
<span data-ttu-id="781da-127">Polecenie cmdlet konstruuje nazwę FQDN definicji sas magazynu z nazwy magazynu, obecnie wybranego środowiska, nazwy konta magazynu i nazwy definicji sas.</span><span class="sxs-lookup"><span data-stu-id="781da-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="781da-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="781da-128">-PassThru</span></span>
<span data-ttu-id="781da-129">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="781da-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="781da-130">Jeśli ten przełącznik zostanie określony, polecenie cmdlet zwróci usunięte konto magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="781da-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="781da-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="781da-131">-VaultName</span></span>
<span data-ttu-id="781da-132">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="781da-132">Vault name.</span></span>
<span data-ttu-id="781da-133">Polecenie cmdlet konstruuje nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="781da-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="781da-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="781da-134">-Confirm</span></span>
<span data-ttu-id="781da-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="781da-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="781da-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="781da-136">-WhatIf</span></span>
<span data-ttu-id="781da-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="781da-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="781da-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="781da-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="781da-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="781da-139">CommonParameters</span></span>
<span data-ttu-id="781da-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="781da-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="781da-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="781da-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="781da-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="781da-142">INPUTS</span></span>

### <span data-ttu-id="781da-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="781da-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="781da-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="781da-144">OUTPUTS</span></span>

### <span data-ttu-id="781da-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="781da-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="781da-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="781da-146">NOTES</span></span>

## <span data-ttu-id="781da-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="781da-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

