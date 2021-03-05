---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: ab2750bff8ccc3f53761671455bc50fe3ec154d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002458"
---
# <span data-ttu-id="23dad-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="23dad-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="23dad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23dad-102">SYNOPSIS</span></span>
<span data-ttu-id="23dad-103">Tworzy zakres szyfrowania dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="23dad-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="23dad-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="23dad-104">SYNTAX</span></span>

### <span data-ttu-id="23dad-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="23dad-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23dad-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="23dad-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23dad-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="23dad-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-RequireInfrastructureEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23dad-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="23dad-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23dad-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="23dad-109">DESCRIPTION</span></span>
<span data-ttu-id="23dad-110">Polecenie **cmdlet New-AzStorageEncryptionScope** tworzy zakres szyfrowania dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="23dad-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="23dad-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="23dad-111">EXAMPLES</span></span>

### <span data-ttu-id="23dad-112">Przykład 1. Tworzenie zakresu szyfrowania przy użyciu szyfrowania magazynu</span><span class="sxs-lookup"><span data-stu-id="23dad-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                         
----      -----    ------            -------------- -------------------------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="23dad-113">To polecenie tworzy zakres szyfrowania przy użyciu szyfrowania magazynu.</span><span class="sxs-lookup"><span data-stu-id="23dad-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="23dad-114">Przykład 2. Tworzenie zakresu szyfrowania przy użyciu szyfrowania Keyvault i requireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="23dad-114">Example 2: Create an encryption scope with Keyvault Encryption, and RequireInfrastructureEncryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" `
    -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57" `
    -RequireInfrastructureEncryption 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name         State   Source           KeyVaultKeyUri                                                                          RequireInfrastructureEncryption                                       
----         -----   ------             --------------                                                                        -------------------------------                                     
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57  True 
```

<span data-ttu-id="23dad-115">To polecenie tworzy zakres szyfrowania za pomocą szyfrowania Keyvault i requireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="23dad-115">This command creates an encryption scope with Keyvault Encryption and RequireInfrastructureEncryption.</span></span>
<span data-ttu-id="23dad-116">Konto magazynu, które jest potrzebne do tożsamości, ma uprawnienia get,wrapkey, unwrapkey do klucza keyvault.</span><span class="sxs-lookup"><span data-stu-id="23dad-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="23dad-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23dad-117">PARAMETERS</span></span>

### <span data-ttu-id="23dad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23dad-118">-DefaultProfile</span></span>
<span data-ttu-id="23dad-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="23dad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23dad-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="23dad-120">-EncryptionScopeName</span></span>
<span data-ttu-id="23dad-121">Nazwa szyfrowania magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="23dad-121">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23dad-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="23dad-122">-KeyUri</span></span>
<span data-ttu-id="23dad-123">Kluczowy Uri</span><span class="sxs-lookup"><span data-stu-id="23dad-123">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23dad-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="23dad-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="23dad-125">Tworzenie zakresu szyfrowania przy użyciu kluczaSource as Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="23dad-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23dad-126">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="23dad-126">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="23dad-127">Zakres szyfrowania zastosuje pomocniczą warstwę szyfrowania z kluczami zarządzanymi platformy dla danych w spoczynku.</span><span class="sxs-lookup"><span data-stu-id="23dad-127">The encryption scope will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="23dad-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23dad-128">-ResourceGroupName</span></span>
<span data-ttu-id="23dad-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23dad-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23dad-130">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="23dad-130">-StorageAccount</span></span>
<span data-ttu-id="23dad-131">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="23dad-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23dad-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="23dad-132">-StorageAccountName</span></span>
<span data-ttu-id="23dad-133">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="23dad-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23dad-134">- StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="23dad-134">-StorageEncryption</span></span>
<span data-ttu-id="23dad-135">Utwórz zakres szyfrowania za pomocą kluczaSource as Microsoft.Storage.</span><span class="sxs-lookup"><span data-stu-id="23dad-135">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23dad-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23dad-136">-Confirm</span></span>
<span data-ttu-id="23dad-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="23dad-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23dad-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23dad-138">-WhatIf</span></span>
<span data-ttu-id="23dad-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23dad-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23dad-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="23dad-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23dad-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23dad-141">CommonParameters</span></span>
<span data-ttu-id="23dad-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23dad-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23dad-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23dad-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23dad-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23dad-144">INPUTS</span></span>

### <span data-ttu-id="23dad-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23dad-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="23dad-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23dad-146">OUTPUTS</span></span>

### <span data-ttu-id="23dad-147">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="23dad-147">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="23dad-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="23dad-148">NOTES</span></span>

## <span data-ttu-id="23dad-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23dad-149">RELATED LINKS</span></span>
