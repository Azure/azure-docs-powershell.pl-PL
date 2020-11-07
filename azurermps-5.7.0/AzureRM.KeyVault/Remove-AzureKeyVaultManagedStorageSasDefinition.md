---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 9859c6f17f393a5ca691c34e3ee144e24ab59fa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717327"
---
# <span data-ttu-id="23a43-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="23a43-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="23a43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23a43-102">SYNOPSIS</span></span>
<span data-ttu-id="23a43-103">Usuwa definicje SAS magazynu kluczy zarządzane w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="23a43-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23a43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23a43-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23a43-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23a43-105">DESCRIPTION</span></span>
<span data-ttu-id="23a43-106">Usuwa definicje SAS magazynu kluczy zarządzane w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="23a43-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="23a43-107">Spowoduje to również usunięcie klucza tajnego użytego do uzyskania tokenu SAS dla tej definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="23a43-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="23a43-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23a43-108">EXAMPLES</span></span>

### <span data-ttu-id="23a43-109">Przykład 1: usuwanie definicji skojarzeń SAS magazynu kluczy zarządzanych w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="23a43-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="23a43-110">Usuwa definicję SAS magazynu zarządzanego w magazynie kluczy "mysasdef" skojarzoną z kontem "mystorageaccount" w magazynie magazynu ".</span><span class="sxs-lookup"><span data-stu-id="23a43-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="23a43-111">Przykład 2: usuwanie definicji skojarzeń SAS magazynu kluczy zarządzanego w usłudze Azure bez potwierdzenia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="23a43-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="23a43-112">Usuwa definicję SAS magazynu zarządzanego w magazynie kluczy "mysasdef" skojarzoną z kontem "mystorageaccount" w magazynie magazynu ".</span><span class="sxs-lookup"><span data-stu-id="23a43-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="23a43-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23a43-113">PARAMETERS</span></span>

### <span data-ttu-id="23a43-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="23a43-114">-AccountName</span></span>
<span data-ttu-id="23a43-115">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="23a43-115">Storage account name.</span></span>
<span data-ttu-id="23a43-116">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranej nazwy konta środowiska i magazynu.</span><span class="sxs-lookup"><span data-stu-id="23a43-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a43-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a43-117">-DefaultProfile</span></span>
<span data-ttu-id="23a43-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="23a43-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23a43-119">-Force</span><span class="sxs-lookup"><span data-stu-id="23a43-119">-Force</span></span>
<span data-ttu-id="23a43-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="23a43-120">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23a43-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23a43-121">-Name</span></span>
<span data-ttu-id="23a43-122">Nazwa definicji SAS magazynu.</span><span class="sxs-lookup"><span data-stu-id="23a43-122">Storage sas definition name.</span></span>
<span data-ttu-id="23a43-123">Polecenie cmdlet tworzy nazwę FQDN definicji SAS magazynu danych na podstawie nazwy magazynu, obecnie wybranego środowiska, nazwy konta magazynu i nazwy definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="23a43-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a43-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23a43-124">-PassThru</span></span>
<span data-ttu-id="23a43-125">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="23a43-125">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="23a43-126">Jeśli ten przełącznik jest określony, polecenie cmdlet zwróci konto zarządzanego magazynu, które zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="23a43-126">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23a43-127">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="23a43-127">-VaultName</span></span>
<span data-ttu-id="23a43-128">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="23a43-128">Vault name.</span></span>
<span data-ttu-id="23a43-129">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="23a43-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a43-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23a43-130">-Confirm</span></span>
<span data-ttu-id="23a43-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23a43-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23a43-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23a43-132">-WhatIf</span></span>
<span data-ttu-id="23a43-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23a43-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23a43-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23a43-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23a43-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a43-135">CommonParameters</span></span>
<span data-ttu-id="23a43-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23a43-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a43-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23a43-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a43-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23a43-138">INPUTS</span></span>

### <span data-ttu-id="23a43-139">System. String</span><span class="sxs-lookup"><span data-stu-id="23a43-139">System.String</span></span>

## <span data-ttu-id="23a43-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23a43-140">OUTPUTS</span></span>

### <span data-ttu-id="23a43-141">Microsoft. Azure. Commands. platforming. models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="23a43-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="23a43-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23a43-142">NOTES</span></span>

## <span data-ttu-id="23a43-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23a43-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

