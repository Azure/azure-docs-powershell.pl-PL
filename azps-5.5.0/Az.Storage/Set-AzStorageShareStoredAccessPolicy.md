---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 5159e09d4e56b45e9b7ce61bae3e9d8e5fd115c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183154"
---
# <span data-ttu-id="a1a74-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a1a74-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="a1a74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1a74-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a74-103">Aktualizuje przechowywane zasady dostępu dla udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="a1a74-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="a1a74-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1a74-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1a74-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1a74-105">DESCRIPTION</span></span>
<span data-ttu-id="a1a74-106">Aktualizacje polecenia cmdlet **Set-AzStorageShareStoredAccessPolicy** przechowywane w zasadach dostępu w magazynie platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a74-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="a1a74-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1a74-107">EXAMPLES</span></span>

### <span data-ttu-id="a1a74-108">Przykład 1. Aktualizowanie zasad dostępu przechowywanego w magazynie</span><span class="sxs-lookup"><span data-stu-id="a1a74-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="a1a74-109">To polecenie aktualizuje przechowywane zasady dostępu, które mają pełne uprawnienia do udziału.</span><span class="sxs-lookup"><span data-stu-id="a1a74-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="a1a74-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1a74-110">PARAMETERS</span></span>

### <span data-ttu-id="a1a74-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a1a74-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a1a74-112">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="a1a74-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a1a74-113">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="a1a74-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a1a74-114">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="a1a74-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a1a74-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a1a74-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a1a74-116">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="a1a74-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a1a74-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="a1a74-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a1a74-118">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="a1a74-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a1a74-119">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="a1a74-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a1a74-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="a1a74-120">The default value is 10.</span></span>

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

### <span data-ttu-id="a1a74-121">— kontekst</span><span class="sxs-lookup"><span data-stu-id="a1a74-121">-Context</span></span>
<span data-ttu-id="a1a74-122">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a74-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a1a74-123">Aby uzyskać kontekst magazynowania, użyj polecenia cmdlet [New-azStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="a1a74-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a1a74-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a74-124">-DefaultProfile</span></span>
<span data-ttu-id="a1a74-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a74-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1a74-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a1a74-126">-ExpiryTime</span></span>
<span data-ttu-id="a1a74-127">Określa czas, w którym przechowywane zasady dostępu stają się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="a1a74-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="a1a74-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a1a74-128">-NoExpiryTime</span></span>
<span data-ttu-id="a1a74-129">Wskazuje, że to polecenie cmdlet wyczyści właściwość **ExpiryTime** w przechowywanych zasadach dostępu.</span><span class="sxs-lookup"><span data-stu-id="a1a74-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="a1a74-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="a1a74-130">-NoStartTime</span></span>
<span data-ttu-id="a1a74-131">Wskazuje, że to polecenie cmdlet wyczyści właściwość **StartTime** w przechowywanych zasadach dostępu.</span><span class="sxs-lookup"><span data-stu-id="a1a74-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="a1a74-132">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="a1a74-132">-Permission</span></span>
<span data-ttu-id="a1a74-133">Określa uprawnienia w przechowywanych zasadach dostępu do uzyskiwania dostępu do udziału lub plików w jej obszarze.</span><span class="sxs-lookup"><span data-stu-id="a1a74-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="a1a74-134">Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).</span><span class="sxs-lookup"><span data-stu-id="a1a74-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="a1a74-135">— Zasady</span><span class="sxs-lookup"><span data-stu-id="a1a74-135">-Policy</span></span>
<span data-ttu-id="a1a74-136">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="a1a74-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="a1a74-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a1a74-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a1a74-138">Określa długość okresu, przez który uchybnia część żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="a1a74-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a1a74-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a1a74-139">-ShareName</span></span>
<span data-ttu-id="a1a74-140">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="a1a74-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="a1a74-141">— StartTime</span><span class="sxs-lookup"><span data-stu-id="a1a74-141">-StartTime</span></span>
<span data-ttu-id="a1a74-142">Określa czas, w którym przechowywane zasady dostępu stają się prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="a1a74-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="a1a74-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1a74-143">-Confirm</span></span>
<span data-ttu-id="a1a74-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a1a74-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a74-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1a74-145">-WhatIf</span></span>
<span data-ttu-id="a1a74-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1a74-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1a74-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a1a74-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a74-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a74-148">CommonParameters</span></span>
<span data-ttu-id="a1a74-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1a74-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a74-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1a74-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a74-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1a74-151">INPUTS</span></span>

### <span data-ttu-id="a1a74-152">System.String</span><span class="sxs-lookup"><span data-stu-id="a1a74-152">System.String</span></span>

### <span data-ttu-id="a1a74-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a1a74-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a1a74-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1a74-154">OUTPUTS</span></span>

### <span data-ttu-id="a1a74-155">System.String</span><span class="sxs-lookup"><span data-stu-id="a1a74-155">System.String</span></span>

## <span data-ttu-id="a1a74-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1a74-156">NOTES</span></span>

## <span data-ttu-id="a1a74-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1a74-157">RELATED LINKS</span></span>

[<span data-ttu-id="a1a74-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a1a74-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="a1a74-159">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a1a74-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="a1a74-160">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a1a74-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="a1a74-161">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a1a74-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)
