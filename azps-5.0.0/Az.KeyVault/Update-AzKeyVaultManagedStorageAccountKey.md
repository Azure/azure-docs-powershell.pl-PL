---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: b603cff68d2343a683718ca53e900aa5b667dc14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234661"
---
# <span data-ttu-id="33656-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="33656-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="33656-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33656-102">SYNOPSIS</span></span>
<span data-ttu-id="33656-103">Generuje ponownie określony klucz konta usługi Azure Storage zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="33656-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="33656-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33656-104">SYNTAX</span></span>

### <span data-ttu-id="33656-105">ByDefinitionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="33656-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33656-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="33656-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33656-107">Opis</span><span class="sxs-lookup"><span data-stu-id="33656-107">DESCRIPTION</span></span>
<span data-ttu-id="33656-108">Generuje ponownie określony klucz konta usługi Azure Storage zarządzanego magazynu kluczy i ustawia klucz jako aktywny.</span><span class="sxs-lookup"><span data-stu-id="33656-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="33656-109">Główne serwery proxy magazynu połączenie z Menedżerem zasobów Azure w celu ponownego wygenerowania klucza.</span><span class="sxs-lookup"><span data-stu-id="33656-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="33656-110">Osoba dzwoniąca musi posses uprawnienia do ponownego generowania kluczy na danym koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="33656-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="33656-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33656-111">EXAMPLES</span></span>

### <span data-ttu-id="33656-112">Przykład 1: ponowne wygenerowanie klucza</span><span class="sxs-lookup"><span data-stu-id="33656-112">Example 1: Regenerate a key</span></span>
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

<span data-ttu-id="33656-113">Generuje ponownie "KEY1" konta "mystorageaccount" i ustawia "KEY1" jako aktywną konto usługi Azure Storage z zarządzaniem magazynem kluczy.</span><span class="sxs-lookup"><span data-stu-id="33656-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="33656-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33656-114">PARAMETERS</span></span>

### <span data-ttu-id="33656-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="33656-115">-AccountName</span></span>
<span data-ttu-id="33656-116">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="33656-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="33656-117">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="33656-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="33656-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33656-118">-DefaultProfile</span></span>
<span data-ttu-id="33656-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="33656-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33656-120">-Force</span><span class="sxs-lookup"><span data-stu-id="33656-120">-Force</span></span>
<span data-ttu-id="33656-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="33656-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="33656-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="33656-122">-InputObject</span></span>
<span data-ttu-id="33656-123">Obiekt ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="33656-123">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="33656-124">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="33656-124">-KeyName</span></span>
<span data-ttu-id="33656-125">Nazwa klucza konta magazynu do ponownego wygenerowania i uaktywnienia.</span><span class="sxs-lookup"><span data-stu-id="33656-125">Name of storage account key to regenerate and make active.</span></span>

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

### <span data-ttu-id="33656-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33656-126">-PassThru</span></span>
<span data-ttu-id="33656-127">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="33656-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="33656-128">Jeśli ten przełącznik jest określony, polecenie cmdlet zwróci konto zarządzanego magazynu, które zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="33656-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="33656-129">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="33656-129">-VaultName</span></span>
<span data-ttu-id="33656-130">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="33656-130">Vault name.</span></span>
<span data-ttu-id="33656-131">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="33656-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="33656-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33656-132">-Confirm</span></span>
<span data-ttu-id="33656-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33656-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33656-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33656-134">-WhatIf</span></span>
<span data-ttu-id="33656-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33656-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33656-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="33656-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33656-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33656-137">CommonParameters</span></span>
<span data-ttu-id="33656-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33656-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33656-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33656-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33656-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33656-140">INPUTS</span></span>

### <span data-ttu-id="33656-141">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="33656-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="33656-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33656-142">OUTPUTS</span></span>

### <span data-ttu-id="33656-143">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="33656-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="33656-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33656-144">NOTES</span></span>

## <span data-ttu-id="33656-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33656-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

