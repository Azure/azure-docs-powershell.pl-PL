---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: 88655ed408242794c6f23a7b170dc007a11ced50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005041"
---
# <span data-ttu-id="0c651-101">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="0c651-101">Get-AzStorageShare</span></span>

## <span data-ttu-id="0c651-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c651-102">SYNOPSIS</span></span>
<span data-ttu-id="0c651-103">Pobiera listę udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="0c651-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="0c651-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0c651-104">SYNTAX</span></span>

### <span data-ttu-id="0c651-105">MatchingPrefix (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0c651-105">MatchingPrefix (Default)</span></span>
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c651-106">Określone</span><span class="sxs-lookup"><span data-stu-id="0c651-106">Specific</span></span>
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0c651-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0c651-107">DESCRIPTION</span></span>
<span data-ttu-id="0c651-108">Polecenie **cmdlet Get-AzStorageShare** otrzymuje listę udziałów plików dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="0c651-108">The **Get-AzStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="0c651-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0c651-109">EXAMPLES</span></span>

### <span data-ttu-id="0c651-110">Przykład 1. Uzyskiwanie udziału plików</span><span class="sxs-lookup"><span data-stu-id="0c651-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="0c651-111">To polecenie pobiera udział plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="0c651-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="0c651-112">Przykład 2. Uzyskiwanie wszystkich udziałów plików zaczynanych od ciągu</span><span class="sxs-lookup"><span data-stu-id="0c651-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

<span data-ttu-id="0c651-113">To polecenie pobiera wszystkie udziały plików, których nazwy zaczynają się od nazwy Contoso.</span><span class="sxs-lookup"><span data-stu-id="0c651-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="0c651-114">Przykład 3. Uzyskiwanie wszystkich udziałów plików w określonym kontekście</span><span class="sxs-lookup"><span data-stu-id="0c651-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

<span data-ttu-id="0c651-115">Pierwsze polecenie używa polecenia cmdlet **New-AzStorageContext** w celu utworzenia kontekstu przy użyciu parametru *Local,* a następnie przechowuje ten obiekt kontekstowy w $Context danych.</span><span class="sxs-lookup"><span data-stu-id="0c651-115">The first command uses the **New-AzStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="0c651-116">Drugie polecenie pobiera udziały plików dla obiektu kontekstowego przechowywanego w $Context.</span><span class="sxs-lookup"><span data-stu-id="0c651-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="0c651-117">Przykład 4. Uzyskiwanie migawki udziału plików z określoną nazwą udostępniania i migawką czasu</span><span class="sxs-lookup"><span data-stu-id="0c651-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="0c651-118">To polecenie pobiera migawkę udziału plików z określoną nazwą udostępniania i migawką czasu.</span><span class="sxs-lookup"><span data-stu-id="0c651-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="0c651-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c651-119">PARAMETERS</span></span>

### <span data-ttu-id="0c651-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c651-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0c651-121">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="0c651-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0c651-122">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="0c651-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0c651-123">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="0c651-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0c651-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0c651-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0c651-125">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="0c651-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0c651-126">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="0c651-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0c651-127">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="0c651-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0c651-128">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="0c651-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0c651-129">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="0c651-129">The default value is 10.</span></span>

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

### <span data-ttu-id="0c651-130">— kontekst</span><span class="sxs-lookup"><span data-stu-id="0c651-130">-Context</span></span>
<span data-ttu-id="0c651-131">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0c651-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="0c651-132">Aby uzyskać kontekst, użyj polecenia cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="0c651-132">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="0c651-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c651-133">-DefaultProfile</span></span>
<span data-ttu-id="0c651-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c651-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c651-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0c651-135">-Name</span></span>
<span data-ttu-id="0c651-136">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="0c651-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="0c651-137">To polecenie cmdlet pobiera udział plików określony przez ten parametr lub nic, jeśli określisz nazwę nieistniecego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="0c651-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c651-138">—Prefiks</span><span class="sxs-lookup"><span data-stu-id="0c651-138">-Prefix</span></span>
<span data-ttu-id="0c651-139">Określa prefiks udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="0c651-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="0c651-140">To polecenie cmdlet pobiera udziały plików zgodne z prefiksem określonym przez ten parametr lub żadne udziały plików, jeśli żadne udziały plików nie są zgodne z określonym prefiksem.</span><span class="sxs-lookup"><span data-stu-id="0c651-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c651-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c651-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0c651-142">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="0c651-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="0c651-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="0c651-143">-SnapshotTime</span></span>
<span data-ttu-id="0c651-144">Czas migawki obrazu udziału plików, który ma zostać odebrany.</span><span class="sxs-lookup"><span data-stu-id="0c651-144">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c651-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c651-145">CommonParameters</span></span>
<span data-ttu-id="0c651-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c651-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c651-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c651-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c651-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c651-148">INPUTS</span></span>

### <span data-ttu-id="0c651-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0c651-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0c651-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c651-150">OUTPUTS</span></span>

### <span data-ttu-id="0c651-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="0c651-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="0c651-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0c651-152">NOTES</span></span>

## <span data-ttu-id="0c651-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c651-153">RELATED LINKS</span></span>

[<span data-ttu-id="0c651-154">New-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="0c651-154">New-AzStorageShare</span></span>](./New-AzStorageShare.md)

[<span data-ttu-id="0c651-155">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="0c651-155">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
