---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
ms.openlocfilehash: b332ed4ec47e5baaa07f579e6ccdbc867b64608e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547768"
---
# <span data-ttu-id="0a11a-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a11a-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="0a11a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a11a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a11a-103">Umożliwia utworzenie udziału plików.</span><span class="sxs-lookup"><span data-stu-id="0a11a-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a11a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a11a-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a11a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0a11a-105">DESCRIPTION</span></span>
<span data-ttu-id="0a11a-106">Polecenie cmdlet **New-AzureStorageShare** umożliwia utworzenie udziału plików.</span><span class="sxs-lookup"><span data-stu-id="0a11a-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="0a11a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a11a-107">EXAMPLES</span></span>

### <span data-ttu-id="0a11a-108">Przykład 1. Tworzenie udziału plików</span><span class="sxs-lookup"><span data-stu-id="0a11a-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="0a11a-109">To polecenie tworzy udział plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="0a11a-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="0a11a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a11a-110">PARAMETERS</span></span>

### <span data-ttu-id="0a11a-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0a11a-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0a11a-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="0a11a-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0a11a-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="0a11a-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0a11a-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="0a11a-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a11a-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0a11a-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0a11a-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="0a11a-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0a11a-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="0a11a-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0a11a-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="0a11a-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0a11a-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="0a11a-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0a11a-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="0a11a-120">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a11a-121">-Context</span><span class="sxs-lookup"><span data-stu-id="0a11a-121">-Context</span></span>
<span data-ttu-id="0a11a-122">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="0a11a-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0a11a-123">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="0a11a-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="0a11a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a11a-124">-DefaultProfile</span></span>
<span data-ttu-id="0a11a-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a11a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a11a-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0a11a-126">-Name</span></span>
<span data-ttu-id="0a11a-127">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="0a11a-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="0a11a-128">To polecenie cmdlet powoduje utworzenie udziału plików o nazwie określającej ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0a11a-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a11a-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0a11a-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0a11a-130">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="0a11a-130">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a11a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a11a-131">CommonParameters</span></span>
<span data-ttu-id="0a11a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a11a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a11a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a11a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a11a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a11a-134">INPUTS</span></span>

### <span data-ttu-id="0a11a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0a11a-135">System.String</span></span>

### <span data-ttu-id="0a11a-136">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a11a-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0a11a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a11a-137">OUTPUTS</span></span>

### <span data-ttu-id="0a11a-138">Microsoft. platformy windowsazure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="0a11a-138">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="0a11a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a11a-139">NOTES</span></span>

## <span data-ttu-id="0a11a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a11a-140">RELATED LINKS</span></span>

[<span data-ttu-id="0a11a-141">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a11a-141">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="0a11a-142">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a11a-142">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="0a11a-143">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a11a-143">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)