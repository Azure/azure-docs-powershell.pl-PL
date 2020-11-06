---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 6363b8030571d6cf3e89b30229395b16cdb5f44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545887"
---
# <span data-ttu-id="a3f36-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a3f36-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="a3f36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3f36-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f36-103">Umożliwia utworzenie kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="a3f36-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3f36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3f36-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="a3f36-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a3f36-105">DESCRIPTION</span></span>
<span data-ttu-id="a3f36-106">Polecenie cmdlet **New-AzureStorageQueue** tworzy kolejkę magazynowania na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a3f36-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="a3f36-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3f36-107">EXAMPLES</span></span>

### <span data-ttu-id="a3f36-108">Przykład 1. Tworzenie kolejki magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a3f36-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="a3f36-109">W tym przykładzie jest tworzona Kolejka magazynu o nazwie queueabc.</span><span class="sxs-lookup"><span data-stu-id="a3f36-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="a3f36-110">Przykład 2: Tworzenie wielu kolejek magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a3f36-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="a3f36-111">W tym przykładzie przedstawiono tworzenie wielu kolejek magazynowych.</span><span class="sxs-lookup"><span data-stu-id="a3f36-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="a3f36-112">Używa metody Split klasy String programu .NET, a następnie przekazuje imiona i nazwiska w potoku.</span><span class="sxs-lookup"><span data-stu-id="a3f36-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="a3f36-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3f36-113">PARAMETERS</span></span>

### <span data-ttu-id="a3f36-114">-Context</span><span class="sxs-lookup"><span data-stu-id="a3f36-114">-Context</span></span>
<span data-ttu-id="a3f36-115">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a3f36-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a3f36-116">Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a3f36-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f36-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3f36-117">-Name</span></span>
<span data-ttu-id="a3f36-118">Określa nazwę kolejki.</span><span class="sxs-lookup"><span data-stu-id="a3f36-118">Specifies a name for the queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f36-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f36-119">CommonParameters</span></span>
<span data-ttu-id="a3f36-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3f36-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f36-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3f36-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f36-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3f36-122">INPUTS</span></span>

### <span data-ttu-id="a3f36-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a3f36-123">IStorageContext</span></span>

<span data-ttu-id="a3f36-124">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="a3f36-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="a3f36-125">Ciąg</span><span class="sxs-lookup"><span data-stu-id="a3f36-125">String</span></span>

<span data-ttu-id="a3f36-126">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="a3f36-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a3f36-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3f36-127">OUTPUTS</span></span>

### <span data-ttu-id="a3f36-128">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a3f36-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="a3f36-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3f36-129">NOTES</span></span>

## <span data-ttu-id="a3f36-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3f36-130">RELATED LINKS</span></span>

[<span data-ttu-id="a3f36-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a3f36-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="a3f36-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a3f36-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


