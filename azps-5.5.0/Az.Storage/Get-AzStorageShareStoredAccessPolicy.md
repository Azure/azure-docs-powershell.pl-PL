---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2e444fba12f0ffebfd3d6679293cac31fc574e93
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190890"
---
# <span data-ttu-id="f786c-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f786c-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="f786c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f786c-102">SYNOPSIS</span></span>
<span data-ttu-id="f786c-103">Pobiera zasady dostępu przechowywane dla udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="f786c-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="f786c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f786c-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f786c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f786c-105">DESCRIPTION</span></span>
<span data-ttu-id="f786c-106">Polecenie **cmdlet Get-AzStorageShareStoredAccessPolicy** pobiera zasady dostępu przechowywane dla udziału magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f786c-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="f786c-107">Aby uzyskać określone zasady, określ je według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f786c-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="f786c-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f786c-108">EXAMPLES</span></span>

### <span data-ttu-id="f786c-109">Przykład 1. Uzyskiwanie przechowywanych zasad dostępu w udostępnij</span><span class="sxs-lookup"><span data-stu-id="f786c-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="f786c-110">To polecenie pobiera przechowywane zasady dostępu o nazwie GeneralPolicy w programie ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="f786c-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="f786c-111">Przykład 2. Uzyskiwanie wszystkich przechowywanych zasad dostępu w programie Share</span><span class="sxs-lookup"><span data-stu-id="f786c-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="f786c-112">To polecenie pobiera wszystkie przechowywane zasady dostępu w użytce ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="f786c-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="f786c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f786c-113">PARAMETERS</span></span>

### <span data-ttu-id="f786c-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f786c-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f786c-115">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="f786c-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f786c-116">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="f786c-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f786c-117">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="f786c-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f786c-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f786c-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f786c-119">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="f786c-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f786c-120">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="f786c-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f786c-121">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="f786c-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f786c-122">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="f786c-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f786c-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="f786c-123">The default value is 10.</span></span>

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

### <span data-ttu-id="f786c-124">— kontekst</span><span class="sxs-lookup"><span data-stu-id="f786c-124">-Context</span></span>
<span data-ttu-id="f786c-125">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f786c-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="f786c-126">Aby uzyskać kontekst, użyj polecenia cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="f786c-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f786c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f786c-127">-DefaultProfile</span></span>
<span data-ttu-id="f786c-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f786c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f786c-129">— Zasady</span><span class="sxs-lookup"><span data-stu-id="f786c-129">-Policy</span></span>
<span data-ttu-id="f786c-130">Określa nazwę przechowywanych zasad dostępu, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f786c-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f786c-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f786c-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f786c-132">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="f786c-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f786c-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f786c-133">-ShareName</span></span>
<span data-ttu-id="f786c-134">Określa nazwę udziału magazynu, dla którego to polecenie cmdlet otrzymuje zasady.</span><span class="sxs-lookup"><span data-stu-id="f786c-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="f786c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f786c-135">CommonParameters</span></span>
<span data-ttu-id="f786c-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f786c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f786c-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f786c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f786c-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f786c-138">INPUTS</span></span>

### <span data-ttu-id="f786c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f786c-139">System.String</span></span>

### <span data-ttu-id="f786c-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f786c-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f786c-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f786c-141">OUTPUTS</span></span>

### <span data-ttu-id="f786c-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="f786c-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="f786c-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f786c-143">NOTES</span></span>

## <span data-ttu-id="f786c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f786c-144">RELATED LINKS</span></span>

[<span data-ttu-id="f786c-145">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f786c-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f786c-146">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f786c-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="f786c-147">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f786c-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="f786c-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f786c-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
