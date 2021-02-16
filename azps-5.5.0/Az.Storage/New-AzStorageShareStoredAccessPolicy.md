---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 52f1e3ce96133d0dc2e389f8eabcb18c6c7790c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197538"
---
# <span data-ttu-id="72665-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="72665-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="72665-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72665-102">SYNOPSIS</span></span>
<span data-ttu-id="72665-103">Tworzy przechowywane zasady dostępu dla udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="72665-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="72665-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="72665-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="72665-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="72665-105">DESCRIPTION</span></span>
<span data-ttu-id="72665-106">Polecenie **cmdlet New-AzStorageShareStoredAccessPolicy** tworzy przechowywane zasady dostępu dla udziału magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="72665-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="72665-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="72665-107">EXAMPLES</span></span>

### <span data-ttu-id="72665-108">Przykład 1. Tworzenie przechowywanych zasad dostępu w udostępnij</span><span class="sxs-lookup"><span data-stu-id="72665-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="72665-109">To polecenie tworzy przechowywane zasady dostępu, które mają pełne uprawnienia w udostępniniu.</span><span class="sxs-lookup"><span data-stu-id="72665-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="72665-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72665-110">PARAMETERS</span></span>

### <span data-ttu-id="72665-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="72665-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="72665-112">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="72665-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="72665-113">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="72665-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="72665-114">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="72665-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="72665-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="72665-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="72665-116">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="72665-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="72665-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="72665-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="72665-118">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="72665-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="72665-119">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="72665-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="72665-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="72665-120">The default value is 10.</span></span>

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

### <span data-ttu-id="72665-121">— kontekst</span><span class="sxs-lookup"><span data-stu-id="72665-121">-Context</span></span>
<span data-ttu-id="72665-122">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="72665-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="72665-123">Aby uzyskać kontekst magazynowania, użyj polecenia cmdlet [New-azStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="72665-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="72665-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72665-124">-DefaultProfile</span></span>
<span data-ttu-id="72665-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="72665-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72665-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="72665-126">-ExpiryTime</span></span>
<span data-ttu-id="72665-127">Określa czas, w którym przechowywane zasady dostępu stają się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="72665-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="72665-128">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="72665-128">-Permission</span></span>
<span data-ttu-id="72665-129">Określa uprawnienia w zasadach dostępu przechowywanego do uzyskiwania dostępu do udziału magazynu lub plików w tej chmurze.</span><span class="sxs-lookup"><span data-stu-id="72665-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="72665-130">Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).</span><span class="sxs-lookup"><span data-stu-id="72665-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="72665-131">— Zasady</span><span class="sxs-lookup"><span data-stu-id="72665-131">-Policy</span></span>
<span data-ttu-id="72665-132">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="72665-132">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="72665-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="72665-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="72665-134">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="72665-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="72665-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="72665-135">-ShareName</span></span>
<span data-ttu-id="72665-136">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="72665-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="72665-137">— StartTime</span><span class="sxs-lookup"><span data-stu-id="72665-137">-StartTime</span></span>
<span data-ttu-id="72665-138">Określa czas, w którym przechowywane zasady dostępu stają się prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="72665-138">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="72665-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72665-139">CommonParameters</span></span>
<span data-ttu-id="72665-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72665-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72665-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72665-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72665-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72665-142">INPUTS</span></span>

### <span data-ttu-id="72665-143">System.String</span><span class="sxs-lookup"><span data-stu-id="72665-143">System.String</span></span>

### <span data-ttu-id="72665-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="72665-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="72665-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="72665-145">OUTPUTS</span></span>

### <span data-ttu-id="72665-146">System.String</span><span class="sxs-lookup"><span data-stu-id="72665-146">System.String</span></span>

## <span data-ttu-id="72665-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="72665-147">NOTES</span></span>

## <span data-ttu-id="72665-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72665-148">RELATED LINKS</span></span>

[<span data-ttu-id="72665-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="72665-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="72665-150">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="72665-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="72665-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="72665-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="72665-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="72665-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
