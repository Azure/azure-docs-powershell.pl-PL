---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1c3f258f4aecbeb492e0e60e274c5e702ae1a3f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197546"
---
# <span data-ttu-id="28809-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="28809-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="28809-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28809-102">SYNOPSIS</span></span>
<span data-ttu-id="28809-103">Tworzy kolejkę magazynu.</span><span class="sxs-lookup"><span data-stu-id="28809-103">Creates a storage queue.</span></span>

## <span data-ttu-id="28809-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="28809-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28809-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="28809-105">DESCRIPTION</span></span>
<span data-ttu-id="28809-106">Polecenie **cmdlet New-AzStorageQueue** tworzy kolejkę magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="28809-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="28809-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="28809-107">EXAMPLES</span></span>

### <span data-ttu-id="28809-108">Przykład 1. Tworzenie kolejki magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="28809-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="28809-109">W tym przykładzie jest tworzyna kolejka magazynu o nazwie queueabc.</span><span class="sxs-lookup"><span data-stu-id="28809-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="28809-110">Przykład 2. Tworzenie wielu kolejek magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="28809-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="28809-111">W tym przykładzie jest tworzenie wielu kolejek magazynu.</span><span class="sxs-lookup"><span data-stu-id="28809-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="28809-112">Używa metody Split klasy .NET String, a następnie przekazuje nazwy w potoku.</span><span class="sxs-lookup"><span data-stu-id="28809-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="28809-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28809-113">PARAMETERS</span></span>

### <span data-ttu-id="28809-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="28809-114">-Context</span></span>
<span data-ttu-id="28809-115">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28809-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="28809-116">Możesz go utworzyć za pomocą polecenia cmdlet New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28809-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="28809-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28809-117">-DefaultProfile</span></span>
<span data-ttu-id="28809-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="28809-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28809-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="28809-119">-Name</span></span>
<span data-ttu-id="28809-120">Określa nazwę kolejki.</span><span class="sxs-lookup"><span data-stu-id="28809-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="28809-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28809-121">CommonParameters</span></span>
<span data-ttu-id="28809-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28809-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28809-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28809-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28809-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28809-124">INPUTS</span></span>

### <span data-ttu-id="28809-125">System.String</span><span class="sxs-lookup"><span data-stu-id="28809-125">System.String</span></span>

### <span data-ttu-id="28809-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="28809-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="28809-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="28809-127">OUTPUTS</span></span>

### <span data-ttu-id="28809-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="28809-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="28809-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="28809-129">NOTES</span></span>

## <span data-ttu-id="28809-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28809-130">RELATED LINKS</span></span>

[<span data-ttu-id="28809-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="28809-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="28809-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="28809-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


