---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523666"
---
# <span data-ttu-id="ec092-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ec092-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="ec092-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec092-102">SYNOPSIS</span></span>
<span data-ttu-id="ec092-103">Umożliwia utworzenie kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="ec092-103">Creates a storage queue.</span></span>

## <span data-ttu-id="ec092-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec092-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="ec092-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ec092-105">DESCRIPTION</span></span>
<span data-ttu-id="ec092-106">Polecenie cmdlet **New-AzureStorageQueue** tworzy kolejkę magazynowania na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ec092-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="ec092-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec092-107">EXAMPLES</span></span>

### <span data-ttu-id="ec092-108">Przykład 1. Tworzenie kolejki magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ec092-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="ec092-109">W tym przykładzie jest tworzona Kolejka magazynu o nazwie queueabc.</span><span class="sxs-lookup"><span data-stu-id="ec092-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="ec092-110">Przykład 2: Tworzenie wielu kolejek magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ec092-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="ec092-111">W tym przykładzie przedstawiono tworzenie wielu kolejek magazynowych.</span><span class="sxs-lookup"><span data-stu-id="ec092-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="ec092-112">Używa metody Split klasy String programu .NET, a następnie przekazuje imiona i nazwiska w potoku.</span><span class="sxs-lookup"><span data-stu-id="ec092-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="ec092-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec092-113">PARAMETERS</span></span>

### <span data-ttu-id="ec092-114">-Context</span><span class="sxs-lookup"><span data-stu-id="ec092-114">-Context</span></span>
<span data-ttu-id="ec092-115">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ec092-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ec092-116">Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ec092-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ec092-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ec092-117">-Name</span></span>
<span data-ttu-id="ec092-118">Określa nazwę kolejki.</span><span class="sxs-lookup"><span data-stu-id="ec092-118">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="ec092-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec092-119">CommonParameters</span></span>
<span data-ttu-id="ec092-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec092-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec092-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec092-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec092-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec092-122">INPUTS</span></span>

## <span data-ttu-id="ec092-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec092-123">OUTPUTS</span></span>

## <span data-ttu-id="ec092-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec092-124">NOTES</span></span>

## <span data-ttu-id="ec092-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec092-125">RELATED LINKS</span></span>

[<span data-ttu-id="ec092-126">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ec092-126">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="ec092-127">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ec092-127">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


