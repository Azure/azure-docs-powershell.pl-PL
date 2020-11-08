---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 4fa89a13f9b4124232d9459d7d3eff54a6f55a5c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219743"
---
# <span data-ttu-id="ace08-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="ace08-101">New-AzStorageShare</span></span>

## <span data-ttu-id="ace08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ace08-102">SYNOPSIS</span></span>
<span data-ttu-id="ace08-103">Umożliwia utworzenie udziału plików.</span><span class="sxs-lookup"><span data-stu-id="ace08-103">Creates a file share.</span></span>

## <span data-ttu-id="ace08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ace08-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="ace08-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ace08-105">DESCRIPTION</span></span>
<span data-ttu-id="ace08-106">Polecenie cmdlet **New-AzStorageShare** umożliwia utworzenie udziału plików.</span><span class="sxs-lookup"><span data-stu-id="ace08-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="ace08-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ace08-107">EXAMPLES</span></span>

### <span data-ttu-id="ace08-108">Przykład 1. Tworzenie udziału plików</span><span class="sxs-lookup"><span data-stu-id="ace08-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="ace08-109">To polecenie tworzy udział plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="ace08-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="ace08-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ace08-110">PARAMETERS</span></span>

### <span data-ttu-id="ace08-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ace08-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ace08-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="ace08-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ace08-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="ace08-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ace08-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="ace08-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ace08-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ace08-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ace08-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="ace08-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ace08-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="ace08-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ace08-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="ace08-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ace08-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="ace08-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ace08-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="ace08-120">The default value is 10.</span></span>

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

### <span data-ttu-id="ace08-121">-Context</span><span class="sxs-lookup"><span data-stu-id="ace08-121">-Context</span></span>
<span data-ttu-id="ace08-122">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ace08-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ace08-123">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="ace08-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="ace08-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace08-124">-DefaultProfile</span></span>
<span data-ttu-id="ace08-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ace08-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ace08-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ace08-126">-Name</span></span>
<span data-ttu-id="ace08-127">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="ace08-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="ace08-128">To polecenie cmdlet powoduje utworzenie udziału plików o nazwie określającej ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ace08-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="ace08-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ace08-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ace08-130">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="ace08-130">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ace08-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace08-131">CommonParameters</span></span>
<span data-ttu-id="ace08-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ace08-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace08-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace08-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace08-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ace08-134">INPUTS</span></span>

### <span data-ttu-id="ace08-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ace08-135">System.String</span></span>

### <span data-ttu-id="ace08-136">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ace08-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ace08-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ace08-137">OUTPUTS</span></span>

### <span data-ttu-id="ace08-138">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="ace08-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="ace08-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ace08-139">NOTES</span></span>

## <span data-ttu-id="ace08-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ace08-140">RELATED LINKS</span></span>

[<span data-ttu-id="ace08-141">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="ace08-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="ace08-142">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ace08-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ace08-143">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="ace08-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
