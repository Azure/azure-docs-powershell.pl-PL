---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 44ad4fadb86b84b5eacb82a15bf92b7b1d831b70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002826"
---
# <span data-ttu-id="972a2-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="972a2-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="972a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="972a2-102">SYNOPSIS</span></span>
<span data-ttu-id="972a2-103">Pobiera lub wyświetla udziały plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="972a2-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="972a2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="972a2-104">SYNTAX</span></span>

### <span data-ttu-id="972a2-105">AccountNameSingle (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="972a2-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="972a2-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="972a2-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="972a2-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="972a2-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="972a2-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="972a2-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="972a2-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="972a2-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="972a2-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="972a2-110">DESCRIPTION</span></span>
<span data-ttu-id="972a2-111">Polecenie **cmdlet Get-AzRmStorageShare** pobiera lub wyświetla udziały plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="972a2-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="972a2-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="972a2-112">EXAMPLES</span></span>

### <span data-ttu-id="972a2-113">Przykład 1. Uzyskiwanie udziału plików magazynu z nazwą konta magazynu i nazwą udostępniania</span><span class="sxs-lookup"><span data-stu-id="972a2-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="972a2-114">To polecenie pobiera udział plików magazynu z nazwą konta magazynu i nazwą udostępniania.</span><span class="sxs-lookup"><span data-stu-id="972a2-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="972a2-115">Przykład 2. Lista wszystkich udziałów plików magazynu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="972a2-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="972a2-116">To polecenie wyświetla listę wszystkich udziałów plików magazynu dla konta magazynu z nazwą konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="972a2-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="972a2-117">Przykład 3. Pobierz kontener obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="972a2-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="972a2-118">To polecenie pobiera kontener obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="972a2-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="972a2-119">Przykład 4. Uzyskiwanie udziału pliku magazynu ze współużytkowaniem w bajtach</span><span class="sxs-lookup"><span data-stu-id="972a2-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="972a2-120">To polecenie pobiera udział plików magazynu z nazwą konta magazynu i nazwą udziału, a także uwzględnia użycie udziału w bajtach.</span><span class="sxs-lookup"><span data-stu-id="972a2-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="972a2-121">Przykład 5. Lista wszystkich udziałów plików magazynu konta magazynu z uwzględnieniem usuniętych udziałów</span><span class="sxs-lookup"><span data-stu-id="972a2-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="972a2-122">To polecenie zawiera listę wszystkich udziałów plików magazynu, w których są uwzględnione usunięte udziały konta magazynu z nazwą konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="972a2-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="972a2-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="972a2-123">PARAMETERS</span></span>

### <span data-ttu-id="972a2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="972a2-124">-DefaultProfile</span></span>
<span data-ttu-id="972a2-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="972a2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="972a2-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="972a2-126">-GetShareUsage</span></span>
<span data-ttu-id="972a2-127">Określ ten parametr, aby uzyskać użycie udostępniania w bajtach.</span><span class="sxs-lookup"><span data-stu-id="972a2-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameSingle, AccountObjectSingle, ShareResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972a2-128">- IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="972a2-128">-IncludeDeleted</span></span>
<span data-ttu-id="972a2-129">Uwzględnianie usuniętych udziałów, domyślnie udziały listy nie będą uwzględniać usuniętych udziałów</span><span class="sxs-lookup"><span data-stu-id="972a2-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972a2-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="972a2-130">-Name</span></span>
<span data-ttu-id="972a2-131">Nazwa udostępniania</span><span class="sxs-lookup"><span data-stu-id="972a2-131">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, ShareResourceId
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountObjectSingle
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972a2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="972a2-132">-ResourceGroupName</span></span>
<span data-ttu-id="972a2-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="972a2-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972a2-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="972a2-134">-ResourceId</span></span>
<span data-ttu-id="972a2-135">Wprowadź identyfikator zasobu udziału plików.</span><span class="sxs-lookup"><span data-stu-id="972a2-135">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="972a2-136">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="972a2-136">-StorageAccount</span></span>
<span data-ttu-id="972a2-137">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="972a2-137">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectSingle, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="972a2-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="972a2-138">-StorageAccountName</span></span>
<span data-ttu-id="972a2-139">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="972a2-139">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972a2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="972a2-140">CommonParameters</span></span>
<span data-ttu-id="972a2-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="972a2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="972a2-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="972a2-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="972a2-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="972a2-143">INPUTS</span></span>

### <span data-ttu-id="972a2-144">System.String</span><span class="sxs-lookup"><span data-stu-id="972a2-144">System.String</span></span>

### <span data-ttu-id="972a2-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="972a2-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="972a2-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="972a2-146">OUTPUTS</span></span>

### <span data-ttu-id="972a2-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="972a2-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="972a2-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="972a2-148">NOTES</span></span>

## <span data-ttu-id="972a2-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="972a2-149">RELATED LINKS</span></span>
