---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 80ff79e71498cc76479592b65207da09fabed6a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976938"
---
# <span data-ttu-id="eb299-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="eb299-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="eb299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb299-102">SYNOPSIS</span></span>
<span data-ttu-id="eb299-103">Ponowne generowanie określonego klucza zarządzanego konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eb299-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="eb299-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eb299-104">SYNTAX</span></span>

### <span data-ttu-id="eb299-105">ByDefinitionName (Default)</span><span class="sxs-lookup"><span data-stu-id="eb299-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb299-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eb299-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb299-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="eb299-107">DESCRIPTION</span></span>
<span data-ttu-id="eb299-108">Ponownie generuje określony klucz zarządzanego konta magazynu platformy Azure i ustawia klucz jako klucz aktywny.</span><span class="sxs-lookup"><span data-stu-id="eb299-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="eb299-109">Magazyn kluczy przejmuje wywołanie do usługi Azure Resource Manager w celu ponownego wygenerowania klucza.</span><span class="sxs-lookup"><span data-stu-id="eb299-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="eb299-110">Wywołujący musi posiadać uprawnienia, aby ponownie wygenerować klucze na danym koncie magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eb299-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="eb299-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eb299-111">EXAMPLES</span></span>

### <span data-ttu-id="eb299-112">Przykład 1. Ponowne generowanie klucza</span><span class="sxs-lookup"><span data-stu-id="eb299-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="eb299-113">Ponownie generuje "klucz1" konta "mystorageaccount" i ustawia "key1" jako aktywne konto magazynu kluczy zarządzanego przez usługę Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="eb299-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="eb299-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb299-114">PARAMETERS</span></span>

### <span data-ttu-id="eb299-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eb299-115">-AccountName</span></span>
<span data-ttu-id="eb299-116">Nazwa konta magazynu zarządzanego przez magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="eb299-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="eb299-117">Polecenie cmdlet konstruuje nazwę FQDN zarządzanego konta magazynu z nazwy magazynu, obecnie wybranego środowiska i nazwy konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="eb299-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb299-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb299-118">-DefaultProfile</span></span>
<span data-ttu-id="eb299-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="eb299-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb299-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="eb299-120">-Force</span></span>
<span data-ttu-id="eb299-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="eb299-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eb299-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb299-122">-InputObject</span></span>
<span data-ttu-id="eb299-123">Obiekt ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="eb299-123">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb299-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="eb299-124">-KeyName</span></span>
<span data-ttu-id="eb299-125">Nazwa klucza konta magazynu do ponownego wygenerowania i aktywnego działania.</span><span class="sxs-lookup"><span data-stu-id="eb299-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb299-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb299-126">-PassThru</span></span>
<span data-ttu-id="eb299-127">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="eb299-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="eb299-128">Jeśli ten przełącznik zostanie określony, polecenie cmdlet zwróci usunięte konto magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="eb299-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="eb299-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="eb299-129">-VaultName</span></span>
<span data-ttu-id="eb299-130">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="eb299-130">Vault name.</span></span>
<span data-ttu-id="eb299-131">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="eb299-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="eb299-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eb299-132">-Confirm</span></span>
<span data-ttu-id="eb299-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="eb299-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb299-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb299-134">-WhatIf</span></span>
<span data-ttu-id="eb299-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb299-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb299-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="eb299-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb299-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb299-137">CommonParameters</span></span>
<span data-ttu-id="eb299-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb299-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb299-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb299-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb299-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb299-140">INPUTS</span></span>

### <span data-ttu-id="eb299-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="eb299-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="eb299-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb299-142">OUTPUTS</span></span>

### <span data-ttu-id="eb299-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eb299-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="eb299-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eb299-144">NOTES</span></span>

## <span data-ttu-id="eb299-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb299-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

