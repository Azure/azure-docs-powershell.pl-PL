---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524022"
---
# <span data-ttu-id="82349-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="82349-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="82349-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82349-102">SYNOPSIS</span></span>
<span data-ttu-id="82349-103">Zawiera listę kolejek przechowywania.</span><span class="sxs-lookup"><span data-stu-id="82349-103">Lists storage queues.</span></span>

## <span data-ttu-id="82349-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82349-104">SYNTAX</span></span>

### <span data-ttu-id="82349-105">QueueName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="82349-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="82349-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="82349-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="82349-107">Opis</span><span class="sxs-lookup"><span data-stu-id="82349-107">DESCRIPTION</span></span>
<span data-ttu-id="82349-108">Polecenie cmdlet **Get-AzureStorageQueue** zawiera listę kolejek magazynowania skojarzonych z kontem usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="82349-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="82349-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82349-109">EXAMPLES</span></span>

### <span data-ttu-id="82349-110">Przykład 1. Lista wszystkich kolejek w usłudze Azure Storage</span><span class="sxs-lookup"><span data-stu-id="82349-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="82349-111">To polecenie powoduje wyświetlenie listy wszystkich kolejek magazynu dla bieżącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="82349-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="82349-112">Przykład 2: Wyświetlanie listy kolejek magazynu platformy Azure przy użyciu znaku wieloznacznego</span><span class="sxs-lookup"><span data-stu-id="82349-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="82349-113">To polecenie używa symbolu wieloznacznego w celu uzyskania listy kolejek przechowywania, których nazwy zaczynają się od kolejki.</span><span class="sxs-lookup"><span data-stu-id="82349-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="82349-114">Przykład 3: Wyświetlanie listy kolejek magazynu platformy Azure przy użyciu prefiksu nazwy kolejki</span><span class="sxs-lookup"><span data-stu-id="82349-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="82349-115">W tym przykładzie użyto parametru *prefix* , aby uzyskać listę kolejek przechowywania, których nazwy zaczynają się od kolejki.</span><span class="sxs-lookup"><span data-stu-id="82349-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="82349-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82349-116">PARAMETERS</span></span>

### <span data-ttu-id="82349-117">-Context</span><span class="sxs-lookup"><span data-stu-id="82349-117">-Context</span></span>
<span data-ttu-id="82349-118">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="82349-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="82349-119">Możesz ją utworzyć przy użyciu polecenia cmdlet **New-AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="82349-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="82349-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82349-120">-Name</span></span>
<span data-ttu-id="82349-121">Określa nazwę.</span><span class="sxs-lookup"><span data-stu-id="82349-121">Specifies a name.</span></span>
<span data-ttu-id="82349-122">Jeśli nie podano nazwy, polecenie cmdlet powoduje wyświetlenie listy wszystkich kolejek.</span><span class="sxs-lookup"><span data-stu-id="82349-122">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="82349-123">Jeśli jest określona pełna lub częściowa nazwa, polecenie cmdlet pobiera wszystkie kolejki zgodne ze wzorcem nazwy.</span><span class="sxs-lookup"><span data-stu-id="82349-123">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82349-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="82349-124">-Prefix</span></span>
<span data-ttu-id="82349-125">Określa prefiks, którego nazwy są używane w nazwach kolejek, które chcesz pobrać.</span><span class="sxs-lookup"><span data-stu-id="82349-125">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82349-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82349-126">CommonParameters</span></span>
<span data-ttu-id="82349-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82349-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82349-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82349-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82349-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82349-129">INPUTS</span></span>

## <span data-ttu-id="82349-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82349-130">OUTPUTS</span></span>

## <span data-ttu-id="82349-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82349-131">NOTES</span></span>

## <span data-ttu-id="82349-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82349-132">RELATED LINKS</span></span>

[<span data-ttu-id="82349-133">Nowe — AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="82349-133">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="82349-134">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="82349-134">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


