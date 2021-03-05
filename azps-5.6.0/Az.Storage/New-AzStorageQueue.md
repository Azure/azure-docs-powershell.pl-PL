---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 55cee15e3b5327fa0a10def6e2090a77b68b207e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002417"
---
# <span data-ttu-id="d1205-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d1205-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="d1205-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1205-102">SYNOPSIS</span></span>
<span data-ttu-id="d1205-103">Tworzy kolejkę magazynu.</span><span class="sxs-lookup"><span data-stu-id="d1205-103">Creates a storage queue.</span></span>

## <span data-ttu-id="d1205-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d1205-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1205-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d1205-105">DESCRIPTION</span></span>
<span data-ttu-id="d1205-106">Polecenie **cmdlet New-AzStorageQueue** tworzy kolejkę magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d1205-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="d1205-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d1205-107">EXAMPLES</span></span>

### <span data-ttu-id="d1205-108">Przykład 1. Tworzenie kolejki magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d1205-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="d1205-109">W tym przykładzie jest tworzyna kolejka magazynu o nazwie queueabc.</span><span class="sxs-lookup"><span data-stu-id="d1205-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="d1205-110">Przykład 2. Tworzenie wielu kolejek magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d1205-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="d1205-111">W tym przykładzie jest tworzenie wielu kolejek magazynu.</span><span class="sxs-lookup"><span data-stu-id="d1205-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="d1205-112">Używa metody Split klasy .NET String, a następnie przekazuje nazwy w potoku.</span><span class="sxs-lookup"><span data-stu-id="d1205-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="d1205-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1205-113">PARAMETERS</span></span>

### <span data-ttu-id="d1205-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="d1205-114">-Context</span></span>
<span data-ttu-id="d1205-115">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d1205-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d1205-116">Możesz go utworzyć za pomocą polecenia cmdlet New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1205-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d1205-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1205-117">-DefaultProfile</span></span>
<span data-ttu-id="d1205-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1205-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1205-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d1205-119">-Name</span></span>
<span data-ttu-id="d1205-120">Określa nazwę kolejki.</span><span class="sxs-lookup"><span data-stu-id="d1205-120">Specifies a name for the queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1205-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1205-121">CommonParameters</span></span>
<span data-ttu-id="d1205-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1205-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1205-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1205-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1205-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1205-124">INPUTS</span></span>

### <span data-ttu-id="d1205-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d1205-125">System.String</span></span>

### <span data-ttu-id="d1205-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1205-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d1205-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1205-127">OUTPUTS</span></span>

### <span data-ttu-id="d1205-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d1205-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="d1205-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d1205-129">NOTES</span></span>

## <span data-ttu-id="d1205-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1205-130">RELATED LINKS</span></span>

[<span data-ttu-id="d1205-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d1205-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="d1205-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d1205-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


