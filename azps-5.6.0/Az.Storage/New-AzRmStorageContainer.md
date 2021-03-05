---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: c85b482ff077263d20ae770e6ec6d91b497153e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994757"
---
# <span data-ttu-id="fb257-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fb257-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="fb257-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb257-102">SYNOPSIS</span></span>
<span data-ttu-id="fb257-103">Tworzy kontener obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="fb257-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="fb257-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fb257-104">SYNTAX</span></span>

### <span data-ttu-id="fb257-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="fb257-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb257-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="fb257-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb257-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fb257-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb257-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="fb257-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb257-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="fb257-109">DESCRIPTION</span></span>
<span data-ttu-id="fb257-110">Polecenie **cmdlet New-AzRmStorageContainer** tworzy kontener obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="fb257-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="fb257-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fb257-111">EXAMPLES</span></span>

### <span data-ttu-id="fb257-112">Przykład 1. Tworzenie kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera z metadanymi</span><span class="sxs-lookup"><span data-stu-id="fb257-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="fb257-113">To polecenie tworzy kontener obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera z metadanymi.</span><span class="sxs-lookup"><span data-stu-id="fb257-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="fb257-114">Przykład 2. Tworzenie kontenera obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera z dostępem publicznym jako obiektem blob</span><span class="sxs-lookup"><span data-stu-id="fb257-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="fb257-115">To polecenie tworzy kontener obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera, z dostępem publicznym jako obiektem blob.</span><span class="sxs-lookup"><span data-stu-id="fb257-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="fb257-116">Przykład 3. Tworzenie kontenera magazynu przy użyciu ustawienia EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="fb257-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
```
PS C:\> $c = New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name testcontainer -DefaultEncryptionScope "testscope" -PreventEncryptionScopeOverride $true

PS C:\> $c

   ResourceGroupName: myResourceGroup, StorageAccountName: myStorageAccount

Name          PublicAccess LastModified HasLegalHold HasImmutabilityPolicy
----          ------------ ------------ ------------ ---------------------
testcontainer                           False        False                

PS C:\> $c.DefaultEncryptionScope
testscope

PS C:\> $c.DenyEncryptionScopeOverride
True
```

<span data-ttu-id="fb257-117">To polecenie tworzy kontener magazynu z algorytmem szyfrowania defaltu i blokuje zakres szyfrowania z domyślnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="fb257-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="fb257-118">Następnie pokaż powiązane właściwości kontenera.</span><span class="sxs-lookup"><span data-stu-id="fb257-118">Then show the related container properties.</span></span>

## <span data-ttu-id="fb257-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb257-119">PARAMETERS</span></span>

### <span data-ttu-id="fb257-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="fb257-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="fb257-121">Domyślny kontener do stosowania określonego zakresu szyfrowania dla wszystkich zapisów.</span><span class="sxs-lookup"><span data-stu-id="fb257-121">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb257-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb257-122">-DefaultProfile</span></span>
<span data-ttu-id="fb257-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb257-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb257-124">— Metadane</span><span class="sxs-lookup"><span data-stu-id="fb257-124">-Metadata</span></span>
<span data-ttu-id="fb257-125">Metadane kontenera</span><span class="sxs-lookup"><span data-stu-id="fb257-125">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb257-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fb257-126">-Name</span></span>
<span data-ttu-id="fb257-127">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="fb257-127">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb257-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="fb257-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="fb257-129">Blokowanie zastępowania zakresu szyfrowania z domyślnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="fb257-129">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb257-130">- PublicAccess</span><span class="sxs-lookup"><span data-stu-id="fb257-130">-PublicAccess</span></span>
<span data-ttu-id="fb257-131">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="fb257-131">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb257-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb257-132">-ResourceGroupName</span></span>
<span data-ttu-id="fb257-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb257-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb257-134">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb257-134">-StorageAccount</span></span>
<span data-ttu-id="fb257-135">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="fb257-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb257-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fb257-136">-StorageAccountName</span></span>
<span data-ttu-id="fb257-137">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fb257-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb257-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb257-138">-Confirm</span></span>
<span data-ttu-id="fb257-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fb257-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb257-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb257-140">-WhatIf</span></span>
<span data-ttu-id="fb257-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb257-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb257-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fb257-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb257-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb257-143">CommonParameters</span></span>
<span data-ttu-id="fb257-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb257-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb257-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb257-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb257-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb257-146">INPUTS</span></span>

### <span data-ttu-id="fb257-147">System.String</span><span class="sxs-lookup"><span data-stu-id="fb257-147">System.String</span></span>

### <span data-ttu-id="fb257-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb257-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="fb257-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb257-149">OUTPUTS</span></span>

### <span data-ttu-id="fb257-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="fb257-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="fb257-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fb257-151">NOTES</span></span>

## <span data-ttu-id="fb257-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb257-152">RELATED LINKS</span></span>
