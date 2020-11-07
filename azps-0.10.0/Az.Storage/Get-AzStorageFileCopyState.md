---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: 55a41e03d07cccc30f2cf8193749fcf4096c5179
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892226"
---
# <span data-ttu-id="98e8c-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="98e8c-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="98e8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="98e8c-103">Pobiera stan operacji kopiowania.</span><span class="sxs-lookup"><span data-stu-id="98e8c-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="98e8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98e8c-104">SYNTAX</span></span>

### <span data-ttu-id="98e8c-105">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="98e8c-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="98e8c-106">Plik</span><span class="sxs-lookup"><span data-stu-id="98e8c-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="98e8c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98e8c-107">DESCRIPTION</span></span>
<span data-ttu-id="98e8c-108">Polecenie cmdlet **Get-AzStorageFileCopyState** Pobiera stan operacji kopiowania plików w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="98e8c-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="98e8c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98e8c-109">EXAMPLES</span></span>

### <span data-ttu-id="98e8c-110">Przykład 1: pobieranie stanu kopiowania według nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="98e8c-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="98e8c-111">To polecenie pobiera stan operacji kopiowania pliku o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="98e8c-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="98e8c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98e8c-112">PARAMETERS</span></span>

### <span data-ttu-id="98e8c-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="98e8c-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="98e8c-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="98e8c-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="98e8c-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="98e8c-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="98e8c-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="98e8c-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="98e8c-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="98e8c-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="98e8c-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="98e8c-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="98e8c-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="98e8c-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="98e8c-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="98e8c-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="98e8c-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="98e8c-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="98e8c-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="98e8c-122">The default value is 10.</span></span>

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

### <span data-ttu-id="98e8c-123">-Context</span><span class="sxs-lookup"><span data-stu-id="98e8c-123">-Context</span></span>
<span data-ttu-id="98e8c-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="98e8c-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="98e8c-125">Aby uzyskać kontekst, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="98e8c-125">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="98e8c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e8c-126">-DefaultProfile</span></span>
<span data-ttu-id="98e8c-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98e8c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98e8c-128">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="98e8c-128">-File</span></span>
<span data-ttu-id="98e8c-129">Określa obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="98e8c-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="98e8c-130">Możesz utworzyć plik w chmurze lub uzyskać go za pomocą polecenia cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="98e8c-130">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="98e8c-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="98e8c-131">-FilePath</span></span>
<span data-ttu-id="98e8c-132">Określa ścieżkę pliku względem udziału usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="98e8c-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="98e8c-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="98e8c-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="98e8c-134">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="98e8c-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="98e8c-135">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="98e8c-135">-ShareName</span></span>
<span data-ttu-id="98e8c-136">Określa nazwę udziału.</span><span class="sxs-lookup"><span data-stu-id="98e8c-136">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="98e8c-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="98e8c-137">-WaitForComplete</span></span>
<span data-ttu-id="98e8c-138">Wskazuje, że to polecenie cmdlet oczekuje na zakończenie kopii.</span><span class="sxs-lookup"><span data-stu-id="98e8c-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="98e8c-139">Jeśli nie podano tego parametru, to polecenie cmdlet natychmiast zwraca wynik.</span><span class="sxs-lookup"><span data-stu-id="98e8c-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="98e8c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e8c-140">CommonParameters</span></span>
<span data-ttu-id="98e8c-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98e8c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e8c-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98e8c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e8c-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98e8c-143">INPUTS</span></span>

### <span data-ttu-id="98e8c-144">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="98e8c-144">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="98e8c-145">Parametry: plik (ByValue)</span><span class="sxs-lookup"><span data-stu-id="98e8c-145">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="98e8c-146">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="98e8c-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="98e8c-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98e8c-147">OUTPUTS</span></span>

### <span data-ttu-id="98e8c-148">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="98e8c-148">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>

## <span data-ttu-id="98e8c-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98e8c-149">NOTES</span></span>

## <span data-ttu-id="98e8c-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98e8c-150">RELATED LINKS</span></span>

[<span data-ttu-id="98e8c-151">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="98e8c-151">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="98e8c-152">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="98e8c-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="98e8c-153">Start — AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="98e8c-153">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="98e8c-154">Zatrzymaj — AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="98e8c-154">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
