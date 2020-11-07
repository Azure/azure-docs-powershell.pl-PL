---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 642c5ff36fb0647907cf72218bd626bcdafe19ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705101"
---
# <span data-ttu-id="57321-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="57321-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="57321-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57321-102">SYNOPSIS</span></span>
<span data-ttu-id="57321-103">Odkrycie poprzednio usuniętego konta magazynu zarządzanego przez magazyny.</span><span class="sxs-lookup"><span data-stu-id="57321-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="57321-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57321-104">SYNTAX</span></span>

### <span data-ttu-id="57321-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="57321-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57321-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="57321-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57321-107">Opis</span><span class="sxs-lookup"><span data-stu-id="57321-107">DESCRIPTION</span></span>
<span data-ttu-id="57321-108">Polecenie **Cofnij — AzKeyVaultManagedStorageAccountRemoval** powoduje odzyskanie uprzednio usuniętego zarządzanego konta magazynu, pod warunkiem że dla tego magazynu jest włączona funkcja usuwania nietrwałego, a próba odzyskania następuje w trakcie interwału odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="57321-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="57321-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57321-109">EXAMPLES</span></span>

### <span data-ttu-id="57321-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="57321-110">Example 1</span></span>
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

<span data-ttu-id="57321-111">Ta sekwencja poleceń określa, czy określone konto magazynu istnieje w magazynie w stanie usunięcia. następne polecenie przywraca usunięte konto magazynu, przywracając je w stanie aktywnym.</span><span class="sxs-lookup"><span data-stu-id="57321-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="57321-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57321-112">PARAMETERS</span></span>

### <span data-ttu-id="57321-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57321-113">-DefaultProfile</span></span>
<span data-ttu-id="57321-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57321-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57321-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="57321-115">-InputObject</span></span>
<span data-ttu-id="57321-116">Usunięto obiekt zarządzanego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="57321-116">Deleted Managed Storage Account object</span></span>

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

### <span data-ttu-id="57321-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57321-117">-Name</span></span>
<span data-ttu-id="57321-118">Nazwa konta magazynu zarządzanego w magazynie.</span><span class="sxs-lookup"><span data-stu-id="57321-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="57321-119">Polecenie cmdlet tworzy nazwę FQDN elementu docelowego na podstawie nazwy magazynu, obecnie wybranego środowiska i nazwy zarządzanego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="57321-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

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

### <span data-ttu-id="57321-120">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="57321-120">-VaultName</span></span>
<span data-ttu-id="57321-121">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="57321-121">Vault name.</span></span>
<span data-ttu-id="57321-122">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="57321-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="57321-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57321-123">-Confirm</span></span>
<span data-ttu-id="57321-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57321-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57321-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57321-125">-WhatIf</span></span>
<span data-ttu-id="57321-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57321-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57321-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="57321-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57321-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57321-128">CommonParameters</span></span>
<span data-ttu-id="57321-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57321-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57321-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57321-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57321-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57321-131">INPUTS</span></span>

### <span data-ttu-id="57321-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="57321-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="57321-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57321-133">OUTPUTS</span></span>

### <span data-ttu-id="57321-134">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57321-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="57321-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57321-135">NOTES</span></span>

## <span data-ttu-id="57321-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57321-136">RELATED LINKS</span></span>
