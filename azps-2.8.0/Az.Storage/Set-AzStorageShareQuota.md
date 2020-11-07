---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: 095d43d41ebc2bcccb770171e668cb737fb40834
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704800"
---
# <span data-ttu-id="bc65c-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="bc65c-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="bc65c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc65c-102">SYNOPSIS</span></span>
<span data-ttu-id="bc65c-103">Umożliwia ustawienie pojemności magazynowania dla udziału.</span><span class="sxs-lookup"><span data-stu-id="bc65c-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="bc65c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc65c-104">SYNTAX</span></span>

### <span data-ttu-id="bc65c-105">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="bc65c-105">ShareName</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="bc65c-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="bc65c-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc65c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bc65c-107">DESCRIPTION</span></span>
<span data-ttu-id="bc65c-108">Polecenie cmdlet **Set-AzStorageShareQuota** określa pojemność magazynowania określonego udziału.</span><span class="sxs-lookup"><span data-stu-id="bc65c-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="bc65c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc65c-109">EXAMPLES</span></span>

### <span data-ttu-id="bc65c-110">Przykład 1: Ustawianie pojemności miejsca do magazynowania dla udziału</span><span class="sxs-lookup"><span data-stu-id="bc65c-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="bc65c-111">To polecenie ustawia pojemność magazynowania dla udziału o nazwie 1024 ContosoShare01 GB.</span><span class="sxs-lookup"><span data-stu-id="bc65c-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="bc65c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc65c-112">PARAMETERS</span></span>

### <span data-ttu-id="bc65c-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bc65c-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bc65c-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="bc65c-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bc65c-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="bc65c-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bc65c-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="bc65c-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bc65c-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bc65c-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bc65c-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="bc65c-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bc65c-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="bc65c-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bc65c-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="bc65c-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bc65c-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="bc65c-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bc65c-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="bc65c-122">The default value is 10.</span></span>

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

### <span data-ttu-id="bc65c-123">-Context</span><span class="sxs-lookup"><span data-stu-id="bc65c-123">-Context</span></span>
<span data-ttu-id="bc65c-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bc65c-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bc65c-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="bc65c-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc65c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc65c-126">-DefaultProfile</span></span>
<span data-ttu-id="bc65c-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc65c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc65c-128">-Przydział</span><span class="sxs-lookup"><span data-stu-id="bc65c-128">-Quota</span></span>
<span data-ttu-id="bc65c-129">Określa wartość przydziału w gigabajtach (GB).</span><span class="sxs-lookup"><span data-stu-id="bc65c-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="bc65c-130">Zobacz ograniczenie przydziałów https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="bc65c-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc65c-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bc65c-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bc65c-132">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="bc65c-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="bc65c-133">-Share</span><span class="sxs-lookup"><span data-stu-id="bc65c-133">-Share</span></span>
<span data-ttu-id="bc65c-134">Określa obiekt **CloudFileShare** reprezentujący udział, dla którego to polecenie cmdlet ustawia przydział.</span><span class="sxs-lookup"><span data-stu-id="bc65c-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="bc65c-135">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="bc65c-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc65c-136">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="bc65c-136">-ShareName</span></span>
<span data-ttu-id="bc65c-137">Określa nazwę udziału pliku, dla którego ma zostać ustawiony przydział.</span><span class="sxs-lookup"><span data-stu-id="bc65c-137">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc65c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc65c-138">CommonParameters</span></span>
<span data-ttu-id="bc65c-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc65c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc65c-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc65c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc65c-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc65c-141">INPUTS</span></span>

### <span data-ttu-id="bc65c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="bc65c-142">System.String</span></span>

### <span data-ttu-id="bc65c-143">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="bc65c-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="bc65c-144">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bc65c-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bc65c-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc65c-145">OUTPUTS</span></span>

### <span data-ttu-id="bc65c-146">Microsoft. Azure. Storage. File. FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="bc65c-146">Microsoft.Azure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="bc65c-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc65c-147">NOTES</span></span>

## <span data-ttu-id="bc65c-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc65c-148">RELATED LINKS</span></span>

[<span data-ttu-id="bc65c-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bc65c-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="bc65c-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="bc65c-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="bc65c-151">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="bc65c-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
