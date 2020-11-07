---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: d1db19d4b49815f5c4e9c6a413008e55707c291b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552483"
---
# <span data-ttu-id="cd099-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="cd099-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="cd099-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd099-102">SYNOPSIS</span></span>
<span data-ttu-id="cd099-103">Umożliwia ustawienie pojemności magazynowania dla udziału.</span><span class="sxs-lookup"><span data-stu-id="cd099-103">Sets the storage capacity for a share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd099-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd099-104">SYNTAX</span></span>

### <span data-ttu-id="cd099-105">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="cd099-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd099-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="cd099-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="cd099-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cd099-107">DESCRIPTION</span></span>
<span data-ttu-id="cd099-108">Polecenie cmdlet **Set-AzureStorageShareQuota** określa pojemność magazynowania określonego udziału.</span><span class="sxs-lookup"><span data-stu-id="cd099-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="cd099-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd099-109">EXAMPLES</span></span>

### <span data-ttu-id="cd099-110">Przykład 1: Ustawianie pojemności miejsca do magazynowania dla udziału</span><span class="sxs-lookup"><span data-stu-id="cd099-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="cd099-111">To polecenie ustawia pojemność magazynowania dla udziału o nazwie 1024 ContosoShare01 GB.</span><span class="sxs-lookup"><span data-stu-id="cd099-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="cd099-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd099-112">PARAMETERS</span></span>

### <span data-ttu-id="cd099-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cd099-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cd099-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="cd099-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cd099-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="cd099-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cd099-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="cd099-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd099-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cd099-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cd099-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="cd099-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cd099-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="cd099-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cd099-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="cd099-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cd099-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="cd099-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cd099-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="cd099-122">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd099-123">-Context</span><span class="sxs-lookup"><span data-stu-id="cd099-123">-Context</span></span>
<span data-ttu-id="cd099-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="cd099-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cd099-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="cd099-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd099-126">-Przydział</span><span class="sxs-lookup"><span data-stu-id="cd099-126">-Quota</span></span>
<span data-ttu-id="cd099-127">Określa wartość przydziału w gigabajtach (GB).</span><span class="sxs-lookup"><span data-stu-id="cd099-127">Specifies the quota value in gigabytes (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd099-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cd099-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cd099-129">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="cd099-129">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd099-130">-Share</span><span class="sxs-lookup"><span data-stu-id="cd099-130">-Share</span></span>
<span data-ttu-id="cd099-131">Określa obiekt **CloudFileShare** reprezentujący udział, dla którego to polecenie cmdlet ustawia przydział.</span><span class="sxs-lookup"><span data-stu-id="cd099-131">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="cd099-132">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="cd099-132">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd099-133">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="cd099-133">-ShareName</span></span>
<span data-ttu-id="cd099-134">Określa nazwę udziału pliku, dla którego ma zostać ustawiony przydział.</span><span class="sxs-lookup"><span data-stu-id="cd099-134">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd099-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd099-135">CommonParameters</span></span>
<span data-ttu-id="cd099-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd099-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd099-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd099-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd099-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd099-138">INPUTS</span></span>

### <span data-ttu-id="cd099-139">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd099-139">IStorageContext</span></span>

<span data-ttu-id="cd099-140">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="cd099-140">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="cd099-141">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="cd099-141">CloudFileShare</span></span>

<span data-ttu-id="cd099-142">Parametr "Udostępnij" akceptuje wartość typu "CloudFileShare" z procesu</span><span class="sxs-lookup"><span data-stu-id="cd099-142">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

### <span data-ttu-id="cd099-143">Ciąg</span><span class="sxs-lookup"><span data-stu-id="cd099-143">String</span></span>

<span data-ttu-id="cd099-144">Parametr "nazwa_udziału" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="cd099-144">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="cd099-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd099-145">OUTPUTS</span></span>

### <span data-ttu-id="cd099-146">Microsoft. platformy windowsazure. Storage. File. FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="cd099-146">Microsoft.WindowsAzure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="cd099-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd099-147">NOTES</span></span>

## <span data-ttu-id="cd099-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd099-148">RELATED LINKS</span></span>

[<span data-ttu-id="cd099-149">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cd099-149">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="cd099-150">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd099-150">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="cd099-151">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd099-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)