---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 901061390c68853832bad14965620abad21817e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499325"
---
# <span data-ttu-id="f8954-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f8954-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="f8954-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8954-102">SYNOPSIS</span></span>
<span data-ttu-id="f8954-103">Tworzy kontener obiektu blob magazynu</span><span class="sxs-lookup"><span data-stu-id="f8954-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="f8954-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8954-104">SYNTAX</span></span>

### <span data-ttu-id="f8954-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f8954-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8954-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="f8954-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8954-107">AccountName</span><span class="sxs-lookup"><span data-stu-id="f8954-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8954-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="f8954-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8954-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f8954-109">DESCRIPTION</span></span>
<span data-ttu-id="f8954-110">Polecenie cmdlet **New-AzRmStorageContainer** tworzy kontener obiektu BLOB magazynowania</span><span class="sxs-lookup"><span data-stu-id="f8954-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="f8954-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8954-111">EXAMPLES</span></span>

### <span data-ttu-id="f8954-112">Przykład 1: Tworzenie kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera z metadanymi</span><span class="sxs-lookup"><span data-stu-id="f8954-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="f8954-113">To polecenie tworzy kontener obiektu BLOB przechowywania z nazwą konta magazynu i nazwą kontenera z metadanymi.</span><span class="sxs-lookup"><span data-stu-id="f8954-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="f8954-114">Przykład 2: Tworzenie kontenera obiektów BLOB magazynowania z obiektem konta magazynu i nazwą kontenera z dostępem publicznym jako obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="f8954-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="f8954-115">To polecenie tworzy kontener obiektu BLOB magazynowania z obiektem konta magazynu i nazwą kontenera z dostępem publicznym jako obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="f8954-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="f8954-116">Przykład 3: Tworzenie kontenera magazynu przy użyciu ustawienia EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="f8954-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
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

<span data-ttu-id="f8954-117">To polecenie tworzy kontener magazynu z defalt encryptionScope i blokuje zmianę zakresu szyfrowania z domyślnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="f8954-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="f8954-118">Następnie Pokaż powiązane właściwości kontenera.</span><span class="sxs-lookup"><span data-stu-id="f8954-118">Then show the related container properties.</span></span>

## <span data-ttu-id="f8954-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8954-119">PARAMETERS</span></span>

### <span data-ttu-id="f8954-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="f8954-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="f8954-121">Domyślnie kontener używający określonego zakresu szyfrowania dla wszystkich zapisów.</span><span class="sxs-lookup"><span data-stu-id="f8954-121">Default the container to use specified encryption scope for all writes.</span></span>

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

### <span data-ttu-id="f8954-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8954-122">-DefaultProfile</span></span>
<span data-ttu-id="f8954-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8954-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8954-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f8954-124">-Metadata</span></span>
<span data-ttu-id="f8954-125">Metadane kontenera</span><span class="sxs-lookup"><span data-stu-id="f8954-125">Container Metadata</span></span>

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

### <span data-ttu-id="f8954-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8954-126">-Name</span></span>
<span data-ttu-id="f8954-127">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="f8954-127">Container Name</span></span>

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

### <span data-ttu-id="f8954-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="f8954-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="f8954-129">Blokowanie przesłonięcia zakresu szyfrowania z domyślnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="f8954-129">Block override of encryption scope from the container default.</span></span>

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

### <span data-ttu-id="f8954-130">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="f8954-130">-PublicAccess</span></span>
<span data-ttu-id="f8954-131">Kontener PublicAccess</span><span class="sxs-lookup"><span data-stu-id="f8954-131">Container PublicAccess</span></span>

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

### <span data-ttu-id="f8954-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8954-132">-ResourceGroupName</span></span>
<span data-ttu-id="f8954-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f8954-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="f8954-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8954-134">-StorageAccount</span></span>
<span data-ttu-id="f8954-135">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="f8954-135">Storage account object</span></span>

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

### <span data-ttu-id="f8954-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f8954-136">-StorageAccountName</span></span>
<span data-ttu-id="f8954-137">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f8954-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="f8954-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8954-138">-Confirm</span></span>
<span data-ttu-id="f8954-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8954-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8954-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8954-140">-WhatIf</span></span>
<span data-ttu-id="f8954-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8954-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8954-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f8954-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8954-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8954-143">CommonParameters</span></span>
<span data-ttu-id="f8954-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8954-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8954-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8954-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8954-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8954-146">INPUTS</span></span>

### <span data-ttu-id="f8954-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f8954-147">System.String</span></span>

### <span data-ttu-id="f8954-148">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8954-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f8954-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8954-149">OUTPUTS</span></span>

### <span data-ttu-id="f8954-150">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="f8954-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="f8954-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8954-151">NOTES</span></span>

## <span data-ttu-id="f8954-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8954-152">RELATED LINKS</span></span>
