---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: b1e7f305b571c5b40c12dacadf520f9637e076f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241874"
---
# <span data-ttu-id="01e7b-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="01e7b-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="01e7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="01e7b-103">Pobiera zasady lub zasady dostępu przechowywanego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="01e7b-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="01e7b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="01e7b-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01e7b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="01e7b-105">DESCRIPTION</span></span>
<span data-ttu-id="01e7b-106">Polecenie **cmdlet Get-AzStorageQueueStoredAccessPolicy** zawiera listę zasad dostępu przechowywanych dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="01e7b-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="01e7b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="01e7b-107">EXAMPLES</span></span>

### <span data-ttu-id="01e7b-108">Przykład 1. Uzyskiwanie zasad dostępu przechowywanego w kolejce</span><span class="sxs-lookup"><span data-stu-id="01e7b-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="01e7b-109">To polecenie pobiera zasady dostępu o nazwie Zasady12 w kolejce magazynu o nazwie Moje kolejkowanie.</span><span class="sxs-lookup"><span data-stu-id="01e7b-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="01e7b-110">Przykład 2. Uzyskiwanie wszystkich przechowywanych zasad dostępu w kolejce</span><span class="sxs-lookup"><span data-stu-id="01e7b-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="01e7b-111">To polecenie pobiera wszystkie zasady dostępu przechowywane w kolejce o nazwie Moje kolejkowanie.</span><span class="sxs-lookup"><span data-stu-id="01e7b-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="01e7b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01e7b-112">PARAMETERS</span></span>

### <span data-ttu-id="01e7b-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="01e7b-113">-Context</span></span>
<span data-ttu-id="01e7b-114">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="01e7b-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="01e7b-115">Aby uzyskać kontekst magazynowania, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01e7b-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="01e7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e7b-116">-DefaultProfile</span></span>
<span data-ttu-id="01e7b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="01e7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01e7b-118">— Zasady</span><span class="sxs-lookup"><span data-stu-id="01e7b-118">-Policy</span></span>
<span data-ttu-id="01e7b-119">Określa zasady przechowywanego dostępu, które zawierają uprawnienia do tego tokenu SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="01e7b-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="01e7b-120">— Kolejka</span><span class="sxs-lookup"><span data-stu-id="01e7b-120">-Queue</span></span>
<span data-ttu-id="01e7b-121">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="01e7b-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="01e7b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e7b-122">CommonParameters</span></span>
<span data-ttu-id="01e7b-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01e7b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e7b-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01e7b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e7b-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01e7b-125">INPUTS</span></span>

### <span data-ttu-id="01e7b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="01e7b-126">System.String</span></span>

### <span data-ttu-id="01e7b-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="01e7b-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="01e7b-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01e7b-128">OUTPUTS</span></span>

### <span data-ttu-id="01e7b-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="01e7b-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="01e7b-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="01e7b-130">NOTES</span></span>

## <span data-ttu-id="01e7b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01e7b-131">RELATED LINKS</span></span>

[<span data-ttu-id="01e7b-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="01e7b-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="01e7b-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="01e7b-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="01e7b-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="01e7b-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="01e7b-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="01e7b-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


