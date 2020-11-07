---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 701b2dd3f2f0faef764cd8b1b64dd6cf88ef069b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707611"
---
# <span data-ttu-id="24420-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24420-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="24420-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24420-102">SYNOPSIS</span></span>
<span data-ttu-id="24420-103">Pobiera zasady dostępu do udziału w magazynie.</span><span class="sxs-lookup"><span data-stu-id="24420-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="24420-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24420-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="24420-105">Opis</span><span class="sxs-lookup"><span data-stu-id="24420-105">DESCRIPTION</span></span>
<span data-ttu-id="24420-106">Polecenie cmdlet **Get-AzStorageShareStoredAccessPolicy** pobiera zasady dostępu do udziału w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="24420-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="24420-107">Aby uzyskać określoną zasadę, określ ją według nazwy.</span><span class="sxs-lookup"><span data-stu-id="24420-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="24420-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24420-108">EXAMPLES</span></span>

### <span data-ttu-id="24420-109">Przykład 1: uzyskiwanie zapisanych zasad dostępu w udziale</span><span class="sxs-lookup"><span data-stu-id="24420-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="24420-110">To polecenie pobiera zapisane zasady dostępu o nazwie GeneralPolicy w ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="24420-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="24420-111">Przykład 2: uzyskiwanie wszystkich przechowywanych zasad dostępu w obszarze Udostępnianie</span><span class="sxs-lookup"><span data-stu-id="24420-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="24420-112">To polecenie pobiera wszystkie zapisane zasady dostępu w ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="24420-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="24420-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24420-113">PARAMETERS</span></span>

### <span data-ttu-id="24420-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="24420-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="24420-115">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="24420-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="24420-116">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="24420-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="24420-117">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="24420-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="24420-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="24420-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="24420-119">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="24420-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="24420-120">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="24420-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="24420-121">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="24420-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="24420-122">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="24420-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="24420-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="24420-123">The default value is 10.</span></span>

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

### <span data-ttu-id="24420-124">-Context</span><span class="sxs-lookup"><span data-stu-id="24420-124">-Context</span></span>
<span data-ttu-id="24420-125">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="24420-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="24420-126">Aby uzyskać kontekst, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="24420-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="24420-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24420-127">-DefaultProfile</span></span>
<span data-ttu-id="24420-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24420-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24420-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="24420-129">-Policy</span></span>
<span data-ttu-id="24420-130">Określa nazwę zasad dostępu przechowywanych w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24420-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24420-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="24420-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="24420-132">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="24420-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="24420-133">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="24420-133">-ShareName</span></span>
<span data-ttu-id="24420-134">Określa nazwę udziału w magazynie, dla którego to polecenie cmdlet pobiera zasady.</span><span class="sxs-lookup"><span data-stu-id="24420-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24420-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24420-135">CommonParameters</span></span>
<span data-ttu-id="24420-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24420-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24420-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24420-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24420-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24420-138">INPUTS</span></span>

### <span data-ttu-id="24420-139">System. String</span><span class="sxs-lookup"><span data-stu-id="24420-139">System.String</span></span>

### <span data-ttu-id="24420-140">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="24420-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="24420-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24420-141">OUTPUTS</span></span>

### <span data-ttu-id="24420-142">Microsoft. platformy windowsazure. Storage. File. SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="24420-142">Microsoft.WindowsAzure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="24420-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24420-143">NOTES</span></span>

## <span data-ttu-id="24420-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24420-144">RELATED LINKS</span></span>

[<span data-ttu-id="24420-145">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="24420-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="24420-146">Nowe — AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24420-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="24420-147">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24420-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="24420-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24420-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
