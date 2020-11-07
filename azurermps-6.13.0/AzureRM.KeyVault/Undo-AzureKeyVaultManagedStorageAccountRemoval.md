---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: a8e8bb9a4a006c30275f1de959181ad640a04f88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719119"
---
# <span data-ttu-id="13e95-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="13e95-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="13e95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13e95-102">SYNOPSIS</span></span>
<span data-ttu-id="13e95-103">Odkrycie poprzednio usuniętego konta magazynu zarządzanego przez magazyny.</span><span class="sxs-lookup"><span data-stu-id="13e95-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13e95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13e95-104">SYNTAX</span></span>

### <span data-ttu-id="13e95-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="13e95-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13e95-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="13e95-106">InputObject</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval
 [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13e95-107">Opis</span><span class="sxs-lookup"><span data-stu-id="13e95-107">DESCRIPTION</span></span>
<span data-ttu-id="13e95-108">Polecenie **Cofnij — AzureKeyVaultManagedStorageAccountRemoval** powoduje odzyskanie uprzednio usuniętego zarządzanego konta magazynu, pod warunkiem że dla tego magazynu jest włączona funkcja usuwania nietrwałego, a próba odzyskania następuje w trakcie interwału odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="13e95-108">The **Undo-AzureKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="13e95-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13e95-109">EXAMPLES</span></span>

### <span data-ttu-id="13e95-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13e95-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzureKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

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

<span data-ttu-id="13e95-111">Ta sekwencja poleceń określa, czy określone konto magazynu istnieje w magazynie w stanie usunięcia. następne polecenie przywraca usunięte konto magazynu, przywracając je w stanie aktywnym.</span><span class="sxs-lookup"><span data-stu-id="13e95-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="13e95-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13e95-112">PARAMETERS</span></span>

### <span data-ttu-id="13e95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13e95-113">-DefaultProfile</span></span>
<span data-ttu-id="13e95-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13e95-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13e95-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="13e95-115">-InputObject</span></span>
<span data-ttu-id="13e95-116">Usunięto obiekt zarządzanego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="13e95-116">Deleted Managed Storage Account object</span></span>

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

### <span data-ttu-id="13e95-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13e95-117">-Name</span></span>
<span data-ttu-id="13e95-118">Nazwa konta magazynu zarządzanego w magazynie.</span><span class="sxs-lookup"><span data-stu-id="13e95-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="13e95-119">Polecenie cmdlet tworzy nazwę FQDN elementu docelowego na podstawie nazwy magazynu, obecnie wybranego środowiska i nazwy zarządzanego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="13e95-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

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

### <span data-ttu-id="13e95-120">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="13e95-120">-VaultName</span></span>
<span data-ttu-id="13e95-121">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="13e95-121">Vault name.</span></span>
<span data-ttu-id="13e95-122">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="13e95-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="13e95-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13e95-123">-Confirm</span></span>
<span data-ttu-id="13e95-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13e95-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13e95-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13e95-125">-WhatIf</span></span>
<span data-ttu-id="13e95-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13e95-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13e95-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13e95-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13e95-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e95-128">CommonParameters</span></span>
<span data-ttu-id="13e95-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13e95-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e95-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13e95-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e95-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13e95-131">INPUTS</span></span>

### <span data-ttu-id="13e95-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="13e95-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="13e95-133">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13e95-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="13e95-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13e95-134">OUTPUTS</span></span>

### <span data-ttu-id="13e95-135">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="13e95-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="13e95-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13e95-136">NOTES</span></span>

## <span data-ttu-id="13e95-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13e95-137">RELATED LINKS</span></span>
