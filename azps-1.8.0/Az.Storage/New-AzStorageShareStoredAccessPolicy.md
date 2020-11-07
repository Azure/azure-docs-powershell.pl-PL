---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 8754bc452e24462f113906b1aa9b82534d1ccbf8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707565"
---
# <span data-ttu-id="8d845-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d845-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="8d845-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d845-102">SYNOPSIS</span></span>
<span data-ttu-id="8d845-103">Tworzy zapisane zasady dostępu w udziale miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="8d845-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="8d845-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d845-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8d845-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8d845-105">DESCRIPTION</span></span>
<span data-ttu-id="8d845-106">Polecenie cmdlet **New-AzStorageShareStoredAccessPolicy** tworzy zapisane zasady dostępu w udziale magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8d845-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="8d845-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d845-107">EXAMPLES</span></span>

### <span data-ttu-id="8d845-108">Przykład 1. Tworzenie zapisanych zasad dostępu w udziale</span><span class="sxs-lookup"><span data-stu-id="8d845-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="8d845-109">To polecenie tworzy zapisane zasady dostępu, które mają pełne uprawnienia w udziale.</span><span class="sxs-lookup"><span data-stu-id="8d845-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="8d845-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d845-110">PARAMETERS</span></span>

### <span data-ttu-id="8d845-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8d845-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8d845-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="8d845-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8d845-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="8d845-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8d845-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="8d845-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8d845-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8d845-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8d845-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8d845-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8d845-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8d845-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8d845-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="8d845-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8d845-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="8d845-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8d845-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="8d845-120">The default value is 10.</span></span>

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

### <span data-ttu-id="8d845-121">-Context</span><span class="sxs-lookup"><span data-stu-id="8d845-121">-Context</span></span>
<span data-ttu-id="8d845-122">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8d845-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8d845-123">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="8d845-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8d845-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d845-124">-DefaultProfile</span></span>
<span data-ttu-id="8d845-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d845-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d845-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8d845-126">-ExpiryTime</span></span>
<span data-ttu-id="8d845-127">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="8d845-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d845-128">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="8d845-128">-Permission</span></span>
<span data-ttu-id="8d845-129">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskania dostępu do plików znajdujących się pod nim lub udostępnionych.</span><span class="sxs-lookup"><span data-stu-id="8d845-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="8d845-130">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="8d845-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d845-131">-Policy</span><span class="sxs-lookup"><span data-stu-id="8d845-131">-Policy</span></span>
<span data-ttu-id="8d845-132">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="8d845-132">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d845-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8d845-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8d845-134">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="8d845-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8d845-135">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="8d845-135">-ShareName</span></span>
<span data-ttu-id="8d845-136">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="8d845-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="8d845-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8d845-137">-StartTime</span></span>
<span data-ttu-id="8d845-138">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="8d845-138">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d845-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d845-139">CommonParameters</span></span>
<span data-ttu-id="8d845-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d845-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d845-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d845-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d845-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d845-142">INPUTS</span></span>

### <span data-ttu-id="8d845-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8d845-143">System.String</span></span>

### <span data-ttu-id="8d845-144">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d845-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8d845-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d845-145">OUTPUTS</span></span>

### <span data-ttu-id="8d845-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8d845-146">System.String</span></span>

## <span data-ttu-id="8d845-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d845-147">NOTES</span></span>

## <span data-ttu-id="8d845-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d845-148">RELATED LINKS</span></span>

[<span data-ttu-id="8d845-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d845-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="8d845-150">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d845-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="8d845-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d845-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="8d845-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d845-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)