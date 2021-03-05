---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 6e7230ad6cb2bd3f58ebd3328aa20fe3c1bf2bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002497"
---
# <span data-ttu-id="fcd2a-101">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fcd2a-101">New-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="fcd2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcd2a-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd2a-103">Tworzy przechowywane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="fcd2a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fcd2a-104">SYNTAX</span></span>

```
New-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fcd2a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fcd2a-105">DESCRIPTION</span></span>
<span data-ttu-id="fcd2a-106">Polecenie **cmdlet New-AzStorageContainerStoredAccessPolicy** tworzy przechowywane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-106">The **New-AzStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="fcd2a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fcd2a-107">EXAMPLES</span></span>

### <span data-ttu-id="fcd2a-108">Przykład 1. Tworzenie przechowywanych zasad dostępu w kontenerze magazynu</span><span class="sxs-lookup"><span data-stu-id="fcd2a-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="fcd2a-109">To polecenie tworzy zasady dostępu o nazwie Zasady01 w kontenerze magazynu o nazwie MyContainer.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="fcd2a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcd2a-110">PARAMETERS</span></span>

### <span data-ttu-id="fcd2a-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fcd2a-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fcd2a-112">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fcd2a-113">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fcd2a-114">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fcd2a-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fcd2a-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fcd2a-116">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fcd2a-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fcd2a-118">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fcd2a-119">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fcd2a-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-120">The default value is 10.</span></span>

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

### <span data-ttu-id="fcd2a-121">— Kontener</span><span class="sxs-lookup"><span data-stu-id="fcd2a-121">-Container</span></span>
<span data-ttu-id="fcd2a-122">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="fcd2a-123">— kontekst</span><span class="sxs-lookup"><span data-stu-id="fcd2a-123">-Context</span></span>
<span data-ttu-id="fcd2a-124">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fcd2a-125">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fcd2a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcd2a-126">-DefaultProfile</span></span>
<span data-ttu-id="fcd2a-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcd2a-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fcd2a-128">-ExpiryTime</span></span>
<span data-ttu-id="fcd2a-129">Określa czas, w którym przechowywane zasady dostępu stają się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="fcd2a-130">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="fcd2a-130">-Permission</span></span>
<span data-ttu-id="fcd2a-131">Określa uprawnienia w przechowywanych zasadach dostępu do uzyskiwania dostępu do kontenera.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="fcd2a-132">Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).</span><span class="sxs-lookup"><span data-stu-id="fcd2a-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="fcd2a-133">— Zasady</span><span class="sxs-lookup"><span data-stu-id="fcd2a-133">-Policy</span></span>
<span data-ttu-id="fcd2a-134">Określa zasady przechowywanego dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="fcd2a-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fcd2a-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fcd2a-136">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fcd2a-137">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fcd2a-138">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fcd2a-139">— StartTime</span><span class="sxs-lookup"><span data-stu-id="fcd2a-139">-StartTime</span></span>
<span data-ttu-id="fcd2a-140">Określa czas, w którym przechowywane zasady dostępu stają się prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="fcd2a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd2a-141">CommonParameters</span></span>
<span data-ttu-id="fcd2a-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcd2a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd2a-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcd2a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd2a-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcd2a-144">INPUTS</span></span>

### <span data-ttu-id="fcd2a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="fcd2a-145">System.String</span></span>

### <span data-ttu-id="fcd2a-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fcd2a-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fcd2a-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcd2a-147">OUTPUTS</span></span>

### <span data-ttu-id="fcd2a-148">System.String</span><span class="sxs-lookup"><span data-stu-id="fcd2a-148">System.String</span></span>

## <span data-ttu-id="fcd2a-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fcd2a-149">NOTES</span></span>

## <span data-ttu-id="fcd2a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcd2a-150">RELATED LINKS</span></span>

[<span data-ttu-id="fcd2a-151">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fcd2a-151">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="fcd2a-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fcd2a-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="fcd2a-153">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fcd2a-153">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="fcd2a-154">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fcd2a-154">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


