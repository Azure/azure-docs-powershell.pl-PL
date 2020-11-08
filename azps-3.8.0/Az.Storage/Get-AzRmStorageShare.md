---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 2ef5ddb4a260f4749d6ccca6fa964f5e205c4b4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051268"
---
# <span data-ttu-id="68e9c-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="68e9c-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="68e9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="68e9c-103">Pobiera lub wyświetla udziały plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="68e9c-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="68e9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68e9c-104">SYNTAX</span></span>

### <span data-ttu-id="68e9c-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="68e9c-105">AccountName (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68e9c-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="68e9c-106">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68e9c-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="68e9c-107">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68e9c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="68e9c-108">DESCRIPTION</span></span>
<span data-ttu-id="68e9c-109">Polecenie cmdlet **Get-AzRmStorageShare** Pobiera lub wyświetla udziały plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="68e9c-109">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="68e9c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68e9c-110">EXAMPLES</span></span>

### <span data-ttu-id="68e9c-111">Przykład 1: pobieranie udziału plików magazynu przy użyciu nazwy konta magazynu i nazwy udziału</span><span class="sxs-lookup"><span data-stu-id="68e9c-111">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="68e9c-112">To polecenie pobiera udział plików magazynu z nazwą konta magazynu i nazwą udziału.</span><span class="sxs-lookup"><span data-stu-id="68e9c-112">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="68e9c-113">Przykład 2: wyświetlanie wszystkich udziałów plików magazynu na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="68e9c-113">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
share2   myStorageAccount   myResourceGroup   "0x8D6FF862774FE57" 5120     2019-07-03 07:14:57Z
```

<span data-ttu-id="68e9c-114">To polecenie wyświetla wszystkie udziały plików magazynu konta magazynu z nazwą konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="68e9c-114">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="68e9c-115">Przykład 3: Pobierz kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="68e9c-115">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Get-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="68e9c-116">To polecenie pobiera kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="68e9c-116">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="68e9c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68e9c-117">PARAMETERS</span></span>

### <span data-ttu-id="68e9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e9c-118">-DefaultProfile</span></span>
<span data-ttu-id="68e9c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68e9c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68e9c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68e9c-120">-Name</span></span>
<span data-ttu-id="68e9c-121">Nazwa udziału</span><span class="sxs-lookup"><span data-stu-id="68e9c-121">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68e9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="68e9c-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="68e9c-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e9c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68e9c-124">-ResourceId</span></span>
<span data-ttu-id="68e9c-125">Wprowadź identyfikator zasobu udziału pliku.</span><span class="sxs-lookup"><span data-stu-id="68e9c-125">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="68e9c-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="68e9c-126">-StorageAccount</span></span>
<span data-ttu-id="68e9c-127">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="68e9c-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68e9c-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="68e9c-128">-StorageAccountName</span></span>
<span data-ttu-id="68e9c-129">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="68e9c-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e9c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e9c-130">CommonParameters</span></span>
<span data-ttu-id="68e9c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68e9c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e9c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e9c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e9c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68e9c-133">INPUTS</span></span>

### <span data-ttu-id="68e9c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="68e9c-134">System.String</span></span>

### <span data-ttu-id="68e9c-135">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68e9c-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="68e9c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68e9c-136">OUTPUTS</span></span>

### <span data-ttu-id="68e9c-137">Microsoft. Azure. Commands. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="68e9c-137">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="68e9c-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68e9c-138">NOTES</span></span>

## <span data-ttu-id="68e9c-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68e9c-139">RELATED LINKS</span></span>
