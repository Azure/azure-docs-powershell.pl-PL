---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 90edd254eb77b03f4f4d26761020d71025960426
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374157"
---
# <span data-ttu-id="fa0b0-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fa0b0-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="fa0b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa0b0-102">SYNOPSIS</span></span>
<span data-ttu-id="fa0b0-103">Pobiera lub wyświetla udziały plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="fa0b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa0b0-104">SYNTAX</span></span>

### <span data-ttu-id="fa0b0-105">AccountNameSingle (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fa0b0-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa0b0-106">Konto</span><span class="sxs-lookup"><span data-stu-id="fa0b0-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa0b0-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="fa0b0-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa0b0-108">AccountName</span><span class="sxs-lookup"><span data-stu-id="fa0b0-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa0b0-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="fa0b0-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa0b0-110">Opis</span><span class="sxs-lookup"><span data-stu-id="fa0b0-110">DESCRIPTION</span></span>
<span data-ttu-id="fa0b0-111">Polecenie cmdlet **Get-AzRmStorageShare** Pobiera lub wyświetla udziały plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="fa0b0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa0b0-112">EXAMPLES</span></span>

### <span data-ttu-id="fa0b0-113">Przykład 1: pobieranie udziału plików magazynu przy użyciu nazwy konta magazynu i nazwy udziału</span><span class="sxs-lookup"><span data-stu-id="fa0b0-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="fa0b0-114">To polecenie pobiera udział plików magazynu z nazwą konta magazynu i nazwą udziału.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="fa0b0-115">Przykład 2: wyświetlanie wszystkich udziałów plików magazynu na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="fa0b0-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="fa0b0-116">To polecenie wyświetla wszystkie udziały plików magazynu konta magazynu z nazwą konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="fa0b0-117">Przykład 3: Pobierz kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="fa0b0-118">To polecenie pobiera kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="fa0b0-119">Przykład 4: pobieranie udziału plików magazynu z udziałem udostępniania w bajtach</span><span class="sxs-lookup"><span data-stu-id="fa0b0-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="fa0b0-120">To polecenie pobiera udział plików magazynu z nazwą konta magazynu i nazwą udziału oraz uwzględnia użycie udostępniania w bajtach.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="fa0b0-121">Przykład 5: wyświetlanie wszystkich udziałów plików magazynu na koncie magazynu z uwzględnieniem usuniętych udziałów</span><span class="sxs-lookup"><span data-stu-id="fa0b0-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="fa0b0-122">To polecenie wyświetla listę wszystkich udziałów plików magazynu obejmującą usunięte udziały konta magazynu z nazwą konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="fa0b0-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa0b0-123">PARAMETERS</span></span>

### <span data-ttu-id="fa0b0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa0b0-124">-DefaultProfile</span></span>
<span data-ttu-id="fa0b0-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa0b0-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="fa0b0-126">-GetShareUsage</span></span>
<span data-ttu-id="fa0b0-127">Określ ten parametr, aby uzyskać użycie udziałów w bajtach.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

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

### <span data-ttu-id="fa0b0-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="fa0b0-128">-IncludeDeleted</span></span>
<span data-ttu-id="fa0b0-129">Uwzględnij usunięte akcje, domyślnie udziały list nie będą obejmować akcji usuniętych</span><span class="sxs-lookup"><span data-stu-id="fa0b0-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

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

### <span data-ttu-id="fa0b0-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fa0b0-130">-Name</span></span>
<span data-ttu-id="fa0b0-131">Nazwa udziału</span><span class="sxs-lookup"><span data-stu-id="fa0b0-131">Share Name</span></span>

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

### <span data-ttu-id="fa0b0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa0b0-132">-ResourceGroupName</span></span>
<span data-ttu-id="fa0b0-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="fa0b0-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa0b0-134">-ResourceId</span></span>
<span data-ttu-id="fa0b0-135">Wprowadź identyfikator zasobu udziału pliku.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-135">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="fa0b0-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa0b0-136">-StorageAccount</span></span>
<span data-ttu-id="fa0b0-137">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="fa0b0-137">Storage account object</span></span>

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

### <span data-ttu-id="fa0b0-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fa0b0-138">-StorageAccountName</span></span>
<span data-ttu-id="fa0b0-139">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-139">Storage Account Name.</span></span>

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

### <span data-ttu-id="fa0b0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa0b0-140">CommonParameters</span></span>
<span data-ttu-id="fa0b0-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa0b0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa0b0-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa0b0-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa0b0-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa0b0-143">INPUTS</span></span>

### <span data-ttu-id="fa0b0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fa0b0-144">System.String</span></span>

### <span data-ttu-id="fa0b0-145">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa0b0-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="fa0b0-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa0b0-146">OUTPUTS</span></span>

### <span data-ttu-id="fa0b0-147">Microsoft. Azure. Commands. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="fa0b0-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="fa0b0-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa0b0-148">NOTES</span></span>

## <span data-ttu-id="fa0b0-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa0b0-149">RELATED LINKS</span></span>
