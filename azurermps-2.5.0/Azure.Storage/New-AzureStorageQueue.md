---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: a028d2528d74e9372bfca28ccfb085f119486ce7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898826"
---
# <span data-ttu-id="2d617-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2d617-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="2d617-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d617-102">SYNOPSIS</span></span>
<span data-ttu-id="2d617-103">Umożliwia utworzenie kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="2d617-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d617-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d617-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d617-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2d617-105">DESCRIPTION</span></span>
<span data-ttu-id="2d617-106">Polecenie cmdlet **New-AzureStorageQueue** tworzy kolejkę magazynowania na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2d617-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="2d617-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d617-107">EXAMPLES</span></span>

### <span data-ttu-id="2d617-108">Przykład 1. Tworzenie kolejki magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2d617-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="2d617-109">W tym przykładzie jest tworzona Kolejka magazynu o nazwie queueabc.</span><span class="sxs-lookup"><span data-stu-id="2d617-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="2d617-110">Przykład 2: Tworzenie wielu kolejek magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2d617-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="2d617-111">W tym przykładzie przedstawiono tworzenie wielu kolejek magazynowych.</span><span class="sxs-lookup"><span data-stu-id="2d617-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="2d617-112">Używa metody Split klasy String programu .NET, a następnie przekazuje imiona i nazwiska w potoku.</span><span class="sxs-lookup"><span data-stu-id="2d617-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="2d617-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d617-113">PARAMETERS</span></span>

### <span data-ttu-id="2d617-114">-Context</span><span class="sxs-lookup"><span data-stu-id="2d617-114">-Context</span></span>
<span data-ttu-id="2d617-115">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2d617-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2d617-116">Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2d617-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2d617-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d617-117">-DefaultProfile</span></span>
<span data-ttu-id="2d617-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d617-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d617-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2d617-119">-Name</span></span>
<span data-ttu-id="2d617-120">Określa nazwę kolejki.</span><span class="sxs-lookup"><span data-stu-id="2d617-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="2d617-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d617-121">CommonParameters</span></span>
<span data-ttu-id="2d617-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d617-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d617-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d617-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d617-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d617-124">INPUTS</span></span>

### <span data-ttu-id="2d617-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2d617-125">System.String</span></span>

### <span data-ttu-id="2d617-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2d617-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2d617-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d617-127">OUTPUTS</span></span>

### <span data-ttu-id="2d617-128">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2d617-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="2d617-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d617-129">NOTES</span></span>

## <span data-ttu-id="2d617-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d617-130">RELATED LINKS</span></span>

[<span data-ttu-id="2d617-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2d617-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="2d617-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2d617-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


