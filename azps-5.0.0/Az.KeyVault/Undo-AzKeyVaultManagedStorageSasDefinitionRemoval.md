---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: bb44bc8f5e4537691d1e5d5493a29111ceaf42a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233512"
---
# <span data-ttu-id="9b528-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="9b528-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="9b528-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b528-102">SYNOPSIS</span></span>
<span data-ttu-id="9b528-103">Odkrycie uprzednio usuniętej definicji skojarzeń SAS magazynu zarządzanych przez magazyny danych.</span><span class="sxs-lookup"><span data-stu-id="9b528-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="9b528-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b528-104">SYNTAX</span></span>

### <span data-ttu-id="9b528-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9b528-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b528-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="9b528-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b528-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9b528-107">DESCRIPTION</span></span>
<span data-ttu-id="9b528-108">Polecenie **Cofnij — AzKeyVaultManagedStorageSasDefinitionRemoval** powoduje odzyskanie uprzednio usuniętej definicji skojarzeń SAS magazynu zarządzanego, pod warunkiem że dla tego magazynu jest włączona funkcja usuwania nietrwałego, a próba odzyskania następuje w trakcie interwału odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="9b528-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="9b528-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b528-109">EXAMPLES</span></span>

### <span data-ttu-id="9b528-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b528-110">Example 1</span></span>
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

<span data-ttu-id="9b528-111">Ta sekwencja poleceń określa, czy określona definicja SAS magazynu istnieje w magazynie w stanie usunięcia. polecenie następne umożliwia odkrycie usuniętej definicji skojarzenia zabezpieczeń, a następnie przywrócenie stanu aktywnego.</span><span class="sxs-lookup"><span data-stu-id="9b528-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="9b528-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b528-112">PARAMETERS</span></span>

### <span data-ttu-id="9b528-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9b528-113">-AccountName</span></span>
<span data-ttu-id="9b528-114">Nazwa konta magazynu zarządzanego przez magazyny.</span><span class="sxs-lookup"><span data-stu-id="9b528-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="9b528-115">Polecenie cmdlet umożliwia podwyższenie nazwy FQDN zarządzanej definicji SAS magazynu zarządzanego na podstawie nazwy magazynu, obecnie wybranego środowiska i nazwy konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="9b528-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

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

### <span data-ttu-id="9b528-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b528-116">-DefaultProfile</span></span>
<span data-ttu-id="9b528-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b528-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b528-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9b528-118">-InputObject</span></span>
<span data-ttu-id="9b528-119">Usunięto obiekt definicji SAS zarządzanego magazynu</span><span class="sxs-lookup"><span data-stu-id="9b528-119">Deleted managed storage SAS definition object</span></span>

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

### <span data-ttu-id="9b528-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b528-120">-Name</span></span>
<span data-ttu-id="9b528-121">Nazwa definicji SAS magazynu zarządzanego przez magazyny danych.</span><span class="sxs-lookup"><span data-stu-id="9b528-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="9b528-122">Polecenie cmdlet tworzy nazwę FQDN elementu docelowego na podstawie nazwy magazynu, obecnie wybranego środowiska, nazwy zarządzanego konta magazynu oraz nazwy definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="9b528-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

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

### <span data-ttu-id="9b528-123">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="9b528-123">-VaultName</span></span>
<span data-ttu-id="9b528-124">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="9b528-124">Vault name.</span></span>
<span data-ttu-id="9b528-125">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="9b528-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9b528-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b528-126">-Confirm</span></span>
<span data-ttu-id="9b528-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b528-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b528-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b528-128">-WhatIf</span></span>
<span data-ttu-id="9b528-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b528-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b528-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b528-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b528-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b528-131">CommonParameters</span></span>
<span data-ttu-id="9b528-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b528-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b528-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b528-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b528-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b528-134">INPUTS</span></span>

### <span data-ttu-id="9b528-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9b528-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="9b528-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b528-136">OUTPUTS</span></span>

### <span data-ttu-id="9b528-137">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="9b528-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="9b528-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b528-138">NOTES</span></span>

## <span data-ttu-id="9b528-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b528-139">RELATED LINKS</span></span>
