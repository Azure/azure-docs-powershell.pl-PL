---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: b1e7f305b571c5b40c12dacadf520f9637e076f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489289"
---
# <span data-ttu-id="7a8b1-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7a8b1-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="7a8b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7a8b1-103">Pobiera zasady lub zasady dostępu do kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7a8b1-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="7a8b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a8b1-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a8b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a8b1-105">DESCRIPTION</span></span>
<span data-ttu-id="7a8b1-106">Polecenie cmdlet **Get-AzStorageQueueStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu lub zasad dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7a8b1-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="7a8b1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a8b1-107">EXAMPLES</span></span>

### <span data-ttu-id="7a8b1-108">Przykład 1: uzyskiwanie zapisanych zasad dostępu w kolejce</span><span class="sxs-lookup"><span data-stu-id="7a8b1-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="7a8b1-109">To polecenie pobiera zasady dostępu o nazwie Policy12 w kolejce magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="7a8b1-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="7a8b1-110">Przykład 2: pobieranie wszystkich przechowywanych zasad dostępu w kolejce</span><span class="sxs-lookup"><span data-stu-id="7a8b1-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="7a8b1-111">To polecenie pobiera wszystkie zapisane zasady dostępu w kolejce o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="7a8b1-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="7a8b1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a8b1-112">PARAMETERS</span></span>

### <span data-ttu-id="7a8b1-113">-Context</span><span class="sxs-lookup"><span data-stu-id="7a8b1-113">-Context</span></span>
<span data-ttu-id="7a8b1-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7a8b1-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="7a8b1-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7a8b1-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a8b1-116">-DefaultProfile</span></span>
<span data-ttu-id="7a8b1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a8b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8b1-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="7a8b1-118">-Policy</span></span>
<span data-ttu-id="7a8b1-119">Określa przechowywane zasady dostępu, które zawierają uprawnienia do tego tokenu współdzielonego podpisu dostępu (SAS).</span><span class="sxs-lookup"><span data-stu-id="7a8b1-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8b1-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="7a8b1-120">-Queue</span></span>
<span data-ttu-id="7a8b1-121">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7a8b1-121">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8b1-122">CommonParameters</span></span>
<span data-ttu-id="7a8b1-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a8b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8b1-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a8b1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8b1-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a8b1-125">INPUTS</span></span>

### <span data-ttu-id="7a8b1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7a8b1-126">System.String</span></span>

### <span data-ttu-id="7a8b1-127">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7a8b1-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7a8b1-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a8b1-128">OUTPUTS</span></span>

### <span data-ttu-id="7a8b1-129">Microsoft. Azure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="7a8b1-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="7a8b1-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a8b1-130">NOTES</span></span>

## <span data-ttu-id="7a8b1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a8b1-131">RELATED LINKS</span></span>

[<span data-ttu-id="7a8b1-132">Nowe — AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7a8b1-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="7a8b1-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7a8b1-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="7a8b1-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7a8b1-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="7a8b1-135">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7a8b1-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


