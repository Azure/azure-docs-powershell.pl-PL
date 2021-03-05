---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: a8f90c2314ad645a8de3a72abc92928759e3b828
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960721"
---
# <span data-ttu-id="5a6f3-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="5a6f3-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="5a6f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="5a6f3-103">Przywraca usuniętą wcześniej definicję SAS magazynu zarządzanego przez usługę KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="5a6f3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a6f3-104">SYNTAX</span></span>

### <span data-ttu-id="5a6f3-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5a6f3-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6f3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5a6f3-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a6f3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a6f3-107">DESCRIPTION</span></span>
<span data-ttu-id="5a6f3-108">Polecenie **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** przywraca wcześniej usuniętą definicję SAS zarządzanego magazynu pod warunkiem, że dla tego magazynu włączono funkcję "miękkiego usuwania" i że próba odzyskania wystąpi w czasie interwału odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="5a6f3-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a6f3-109">EXAMPLES</span></span>

### <span data-ttu-id="5a6f3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a6f3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName myVault -AccountName myAccount -Name mySasName -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageSasDefinitionRemoval -VaultName myVault -AccountName myAccount -Name mySasName

Id          : https://myvault.vault.azure.net:443/storage/myaccount/sas/mysasname
Secret Id   : https://myvault.vault.azure.net/secrets/myaccount-mysasname
Vault Name  : myVault
AccountName : myAccount
Name        : mySasName
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="5a6f3-111">Ta sekwencja poleceń określa, czy określona definicja SAS magazynu istnieje w magazynie w stanie usunięcia. Kolejne polecenie przywraca usuniętą definicję sas, przywracając ją do stanu aktywnego.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="5a6f3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a6f3-112">PARAMETERS</span></span>

### <span data-ttu-id="5a6f3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5a6f3-113">-AccountName</span></span>
<span data-ttu-id="5a6f3-114">Nazwa konta magazynu zarządzanego przez usługę KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="5a6f3-115">Polecenie cmdlet konstruuje nazwę FQDN definicji SAS magazynu zarządzanego z nazwy magazynu, obecnie wybranego środowiska i nazwy konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a6f3-116">-DefaultProfile</span></span>
<span data-ttu-id="5a6f3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a6f3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a6f3-118">-InputObject</span></span>
<span data-ttu-id="5a6f3-119">Usunięto obiekt definicji SAS zarządzanego magazynu</span><span class="sxs-lookup"><span data-stu-id="5a6f3-119">Deleted managed storage SAS definition object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a6f3-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5a6f3-120">-Name</span></span>
<span data-ttu-id="5a6f3-121">Nazwa definicji SAS przestrzeni dyskowej zarządzanej przez usługę KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="5a6f3-122">Polecenie cmdlet konstruuje nazwę FQDN obiektu docelowego z nazwy magazynu, obecnie wybranego środowiska, nazwy konta magazynu zarządzanego i nazwy definicji sas.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6f3-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5a6f3-123">-VaultName</span></span>
<span data-ttu-id="5a6f3-124">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-124">Vault name.</span></span>
<span data-ttu-id="5a6f3-125">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="5a6f3-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a6f3-126">-Confirm</span></span>
<span data-ttu-id="5a6f3-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a6f3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a6f3-128">-WhatIf</span></span>
<span data-ttu-id="5a6f3-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a6f3-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a6f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a6f3-131">CommonParameters</span></span>
<span data-ttu-id="5a6f3-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a6f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a6f3-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a6f3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a6f3-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a6f3-134">INPUTS</span></span>

### <span data-ttu-id="5a6f3-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5a6f3-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="5a6f3-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a6f3-136">OUTPUTS</span></span>

### <span data-ttu-id="5a6f3-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="5a6f3-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="5a6f3-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a6f3-138">NOTES</span></span>

## <span data-ttu-id="5a6f3-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a6f3-139">RELATED LINKS</span></span>
