---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 289adecd07837134fed9279758cf1142d30183a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010465"
---
# <span data-ttu-id="f30f5-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="f30f5-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="f30f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f30f5-102">SYNOPSIS</span></span>
<span data-ttu-id="f30f5-103">Odzyskiwanie poprzednio usuniętego konta magazynu zarządzanego przez usługę KeyVault.</span><span class="sxs-lookup"><span data-stu-id="f30f5-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="f30f5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f30f5-104">SYNTAX</span></span>

### <span data-ttu-id="f30f5-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f30f5-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f30f5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f30f5-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f30f5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f30f5-107">DESCRIPTION</span></span>
<span data-ttu-id="f30f5-108">Polecenie **Undo-AzKeyVaultManagedStorageAccountRemoval** umożliwia odzyskanie poprzednio usuniętego zarządzanego konta magazynu pod warunkiem, że dla tego magazynu włączono funkcję "miękkiego usuwania" i że próba odzyskania wystąpi w interwale odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="f30f5-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="f30f5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f30f5-109">EXAMPLES</span></span>

### <span data-ttu-id="f30f5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f30f5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

Id                  : https://myvault.vault.azure.net:443/storage/myaccount
Vault Name          : myVault
AccountName         : myAccount
Account Resource Id : /subscriptions/8bc48661-1801-4b7a-8ca1-6a3cadfb4870/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/myaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="f30f5-111">Ta sekwencja poleceń określa, czy określone konto magazynu istnieje w magazynie w stanie usunięcia. Kolejne polecenie przywraca usunięte konto magazynu i przywraca je do stanu aktywnego.</span><span class="sxs-lookup"><span data-stu-id="f30f5-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="f30f5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f30f5-112">PARAMETERS</span></span>

### <span data-ttu-id="f30f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30f5-113">-DefaultProfile</span></span>
<span data-ttu-id="f30f5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f30f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f30f5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f30f5-115">-InputObject</span></span>
<span data-ttu-id="f30f5-116">Usunięto obiekt Konta magazynu zarządzanego</span><span class="sxs-lookup"><span data-stu-id="f30f5-116">Deleted Managed Storage Account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f30f5-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f30f5-117">-Name</span></span>
<span data-ttu-id="f30f5-118">Nazwa konta magazynu zarządzanego przez usługę KeyVault.</span><span class="sxs-lookup"><span data-stu-id="f30f5-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="f30f5-119">Polecenie cmdlet konstruuje nazwę FQDN obiektu docelowego z nazwy magazynu, obecnie wybranego środowiska i nazwy konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="f30f5-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30f5-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f30f5-120">-VaultName</span></span>
<span data-ttu-id="f30f5-121">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="f30f5-121">Vault name.</span></span>
<span data-ttu-id="f30f5-122">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="f30f5-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f30f5-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f30f5-123">-Confirm</span></span>
<span data-ttu-id="f30f5-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f30f5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f30f5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f30f5-125">-WhatIf</span></span>
<span data-ttu-id="f30f5-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f30f5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f30f5-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f30f5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f30f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30f5-128">CommonParameters</span></span>
<span data-ttu-id="f30f5-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f30f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30f5-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f30f5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30f5-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f30f5-131">INPUTS</span></span>

### <span data-ttu-id="f30f5-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f30f5-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="f30f5-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f30f5-133">OUTPUTS</span></span>

### <span data-ttu-id="f30f5-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f30f5-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="f30f5-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f30f5-135">NOTES</span></span>

## <span data-ttu-id="f30f5-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f30f5-136">RELATED LINKS</span></span>
