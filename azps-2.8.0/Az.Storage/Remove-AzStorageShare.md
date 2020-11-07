---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: 05cb1fcbad453704a5295b38c8f0be3b1614f237
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888225"
---
# <span data-ttu-id="c0696-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c0696-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="c0696-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0696-102">SYNOPSIS</span></span>
<span data-ttu-id="c0696-103">Usuwa udział plików.</span><span class="sxs-lookup"><span data-stu-id="c0696-103">Deletes a file share.</span></span>

## <span data-ttu-id="c0696-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0696-104">SYNTAX</span></span>

### <span data-ttu-id="c0696-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c0696-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0696-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="c0696-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0696-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c0696-107">DESCRIPTION</span></span>
<span data-ttu-id="c0696-108">Polecenie cmdlet **Remove-AzStorageShare** usuwa udział plików.</span><span class="sxs-lookup"><span data-stu-id="c0696-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="c0696-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0696-109">EXAMPLES</span></span>

### <span data-ttu-id="c0696-110">Przykład 1: usuwanie udziału plików</span><span class="sxs-lookup"><span data-stu-id="c0696-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="c0696-111">To polecenie usuwa udział plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="c0696-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="c0696-112">Przykład 2: usunięcie udziału plików i wszystkich jego migawek</span><span class="sxs-lookup"><span data-stu-id="c0696-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="c0696-113">To polecenie usuwa udział plików o nazwie ContosoShare06 oraz wszystkie jej migawki.</span><span class="sxs-lookup"><span data-stu-id="c0696-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="c0696-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0696-114">PARAMETERS</span></span>

### <span data-ttu-id="c0696-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0696-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c0696-116">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="c0696-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c0696-117">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="c0696-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c0696-118">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="c0696-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c0696-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c0696-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c0696-120">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c0696-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c0696-121">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c0696-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c0696-122">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="c0696-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c0696-123">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="c0696-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c0696-124">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="c0696-124">The default value is 10.</span></span>

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

### <span data-ttu-id="c0696-125">-Context</span><span class="sxs-lookup"><span data-stu-id="c0696-125">-Context</span></span>
<span data-ttu-id="c0696-126">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c0696-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c0696-127">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="c0696-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c0696-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0696-128">-DefaultProfile</span></span>
<span data-ttu-id="c0696-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0696-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0696-130">-Force</span><span class="sxs-lookup"><span data-stu-id="c0696-130">-Force</span></span>
<span data-ttu-id="c0696-131">Wymuś usunięcie udziału ze wszystkimi jego migawkami i całą zawartością.</span><span class="sxs-lookup"><span data-stu-id="c0696-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="c0696-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="c0696-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="c0696-133">Usuwanie udziału plików ze wszystkimi migawkami</span><span class="sxs-lookup"><span data-stu-id="c0696-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="c0696-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0696-134">-Name</span></span>
<span data-ttu-id="c0696-135">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="c0696-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="c0696-136">To polecenie cmdlet usuwa udział plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c0696-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0696-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0696-137">-PassThru</span></span>
<span data-ttu-id="c0696-138">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="c0696-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="c0696-139">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="c0696-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c0696-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0696-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c0696-141">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="c0696-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c0696-142">-Share</span><span class="sxs-lookup"><span data-stu-id="c0696-142">-Share</span></span>
<span data-ttu-id="c0696-143">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="c0696-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="c0696-144">To polecenie cmdlet usuwa obiekt, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c0696-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="c0696-145">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="c0696-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="c0696-146">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="c0696-146">This object contains the storage context.</span></span>
<span data-ttu-id="c0696-147">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="c0696-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="c0696-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0696-148">-Confirm</span></span>
<span data-ttu-id="c0696-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0696-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0696-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0696-150">-WhatIf</span></span>
<span data-ttu-id="c0696-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0696-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0696-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c0696-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0696-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0696-153">CommonParameters</span></span>
<span data-ttu-id="c0696-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0696-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0696-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0696-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0696-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0696-156">INPUTS</span></span>

### <span data-ttu-id="c0696-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c0696-157">System.String</span></span>

### <span data-ttu-id="c0696-158">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="c0696-158">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="c0696-159">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c0696-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c0696-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0696-160">OUTPUTS</span></span>

### <span data-ttu-id="c0696-161">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="c0696-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="c0696-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0696-162">NOTES</span></span>

## <span data-ttu-id="c0696-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0696-163">RELATED LINKS</span></span>

[<span data-ttu-id="c0696-164">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c0696-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="c0696-165">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c0696-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c0696-166">Nowe — AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c0696-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)
