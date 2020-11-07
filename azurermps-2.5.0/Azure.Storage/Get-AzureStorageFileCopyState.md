---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecopystate
schema: 2.0.0
ms.openlocfilehash: 61e633bc0890a8971b0be9d1b5950d990d32e8f4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898601"
---
# <span data-ttu-id="58eda-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="58eda-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="58eda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58eda-102">SYNOPSIS</span></span>
<span data-ttu-id="58eda-103">Pobiera stan operacji kopiowania.</span><span class="sxs-lookup"><span data-stu-id="58eda-103">Gets the state of a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58eda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58eda-104">SYNTAX</span></span>

### <span data-ttu-id="58eda-105">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="58eda-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="58eda-106">Plik</span><span class="sxs-lookup"><span data-stu-id="58eda-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="58eda-107">Opis</span><span class="sxs-lookup"><span data-stu-id="58eda-107">DESCRIPTION</span></span>
<span data-ttu-id="58eda-108">Polecenie cmdlet **Get-AzureStorageFileCopyState** Pobiera stan operacji kopiowania plików w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="58eda-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="58eda-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58eda-109">EXAMPLES</span></span>

### <span data-ttu-id="58eda-110">Przykład 1: pobieranie stanu kopiowania według nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="58eda-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="58eda-111">To polecenie pobiera stan operacji kopiowania pliku o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="58eda-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="58eda-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58eda-112">PARAMETERS</span></span>

### <span data-ttu-id="58eda-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="58eda-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="58eda-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="58eda-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="58eda-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="58eda-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="58eda-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="58eda-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="58eda-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="58eda-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="58eda-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="58eda-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="58eda-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="58eda-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="58eda-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="58eda-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="58eda-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="58eda-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="58eda-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="58eda-122">The default value is 10.</span></span>

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

### <span data-ttu-id="58eda-123">-Context</span><span class="sxs-lookup"><span data-stu-id="58eda-123">-Context</span></span>
<span data-ttu-id="58eda-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="58eda-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="58eda-125">Aby uzyskać kontekst, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="58eda-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="58eda-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58eda-126">-DefaultProfile</span></span>
<span data-ttu-id="58eda-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58eda-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58eda-128">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="58eda-128">-File</span></span>
<span data-ttu-id="58eda-129">Określa obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="58eda-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="58eda-130">Możesz utworzyć plik w chmurze lub uzyskać go za pomocą polecenia cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="58eda-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58eda-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="58eda-131">-FilePath</span></span>
<span data-ttu-id="58eda-132">Określa ścieżkę pliku względem udziału usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="58eda-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58eda-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="58eda-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="58eda-134">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="58eda-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="58eda-135">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="58eda-135">-ShareName</span></span>
<span data-ttu-id="58eda-136">Określa nazwę udziału.</span><span class="sxs-lookup"><span data-stu-id="58eda-136">Specifies the name of a share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58eda-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="58eda-137">-WaitForComplete</span></span>
<span data-ttu-id="58eda-138">Wskazuje, że to polecenie cmdlet oczekuje na zakończenie kopii.</span><span class="sxs-lookup"><span data-stu-id="58eda-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="58eda-139">Jeśli nie podano tego parametru, to polecenie cmdlet natychmiast zwraca wynik.</span><span class="sxs-lookup"><span data-stu-id="58eda-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58eda-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58eda-140">CommonParameters</span></span>
<span data-ttu-id="58eda-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58eda-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58eda-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58eda-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58eda-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58eda-143">INPUTS</span></span>

### <span data-ttu-id="58eda-144">Microsoft. platformy windowsazure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="58eda-144">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="58eda-145">Parametry: plik (ByValue)</span><span class="sxs-lookup"><span data-stu-id="58eda-145">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="58eda-146">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="58eda-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="58eda-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58eda-147">OUTPUTS</span></span>

### <span data-ttu-id="58eda-148">Microsoft. platformy windowsazure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="58eda-148">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="58eda-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58eda-149">NOTES</span></span>

## <span data-ttu-id="58eda-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58eda-150">RELATED LINKS</span></span>

[<span data-ttu-id="58eda-151">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="58eda-151">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="58eda-152">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="58eda-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="58eda-153">Start — AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="58eda-153">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="58eda-154">Zatrzymaj — AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="58eda-154">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
