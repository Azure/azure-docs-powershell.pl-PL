---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageshare
schema: 2.0.0
ms.openlocfilehash: 07ab4071d89e1ba97d4c824bd98012fae70a79de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899163"
---
# <span data-ttu-id="3bbba-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="3bbba-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="3bbba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bbba-102">SYNOPSIS</span></span>
<span data-ttu-id="3bbba-103">Usuwa udział plików.</span><span class="sxs-lookup"><span data-stu-id="3bbba-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bbba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bbba-104">SYNTAX</span></span>

### <span data-ttu-id="3bbba-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3bbba-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bbba-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="3bbba-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3bbba-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3bbba-107">DESCRIPTION</span></span>
<span data-ttu-id="3bbba-108">Polecenie cmdlet **Remove-AzureStorageShare** usuwa udział plików.</span><span class="sxs-lookup"><span data-stu-id="3bbba-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="3bbba-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bbba-109">EXAMPLES</span></span>

### <span data-ttu-id="3bbba-110">Przykład 1: usuwanie udziału plików</span><span class="sxs-lookup"><span data-stu-id="3bbba-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="3bbba-111">To polecenie usuwa udział plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="3bbba-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="3bbba-112">Przykład 2: usunięcie udziału plików i wszystkich jego migawek</span><span class="sxs-lookup"><span data-stu-id="3bbba-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="3bbba-113">To polecenie usuwa udział plików o nazwie ContosoShare06 oraz wszystkie jej migawki.</span><span class="sxs-lookup"><span data-stu-id="3bbba-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="3bbba-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bbba-114">PARAMETERS</span></span>

### <span data-ttu-id="3bbba-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3bbba-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3bbba-116">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="3bbba-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3bbba-117">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="3bbba-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3bbba-118">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="3bbba-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3bbba-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3bbba-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3bbba-120">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3bbba-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3bbba-121">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3bbba-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3bbba-122">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="3bbba-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3bbba-123">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="3bbba-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3bbba-124">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="3bbba-124">The default value is 10.</span></span>

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

### <span data-ttu-id="3bbba-125">-Context</span><span class="sxs-lookup"><span data-stu-id="3bbba-125">-Context</span></span>
<span data-ttu-id="3bbba-126">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3bbba-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3bbba-127">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="3bbba-127">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="3bbba-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bbba-128">-DefaultProfile</span></span>
<span data-ttu-id="3bbba-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bbba-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bbba-130">-Force</span><span class="sxs-lookup"><span data-stu-id="3bbba-130">-Force</span></span>
<span data-ttu-id="3bbba-131">Wymuś usunięcie udziału ze wszystkimi jego migawkami i całą zawartością.</span><span class="sxs-lookup"><span data-stu-id="3bbba-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="3bbba-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="3bbba-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="3bbba-133">Usuwanie udziału plików ze wszystkimi migawkami</span><span class="sxs-lookup"><span data-stu-id="3bbba-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="3bbba-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3bbba-134">-Name</span></span>
<span data-ttu-id="3bbba-135">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="3bbba-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="3bbba-136">To polecenie cmdlet usuwa udział plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3bbba-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="3bbba-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bbba-137">-PassThru</span></span>
<span data-ttu-id="3bbba-138">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="3bbba-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3bbba-139">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="3bbba-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3bbba-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3bbba-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3bbba-141">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="3bbba-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3bbba-142">-Share</span><span class="sxs-lookup"><span data-stu-id="3bbba-142">-Share</span></span>
<span data-ttu-id="3bbba-143">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="3bbba-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="3bbba-144">To polecenie cmdlet usuwa obiekt, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3bbba-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="3bbba-145">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="3bbba-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="3bbba-146">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="3bbba-146">This object contains the storage context.</span></span>
<span data-ttu-id="3bbba-147">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="3bbba-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bbba-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3bbba-148">-Confirm</span></span>
<span data-ttu-id="3bbba-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bbba-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bbba-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bbba-150">-WhatIf</span></span>
<span data-ttu-id="3bbba-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bbba-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bbba-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3bbba-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bbba-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bbba-153">CommonParameters</span></span>
<span data-ttu-id="3bbba-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bbba-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bbba-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bbba-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bbba-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bbba-156">INPUTS</span></span>

### <span data-ttu-id="3bbba-157">System. String</span><span class="sxs-lookup"><span data-stu-id="3bbba-157">System.String</span></span>

### <span data-ttu-id="3bbba-158">Microsoft. platformy windowsazure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3bbba-158">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="3bbba-159">Parametry: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3bbba-159">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="3bbba-160">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3bbba-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3bbba-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bbba-161">OUTPUTS</span></span>

### <span data-ttu-id="3bbba-162">Microsoft. platformy windowsazure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3bbba-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="3bbba-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bbba-163">NOTES</span></span>

## <span data-ttu-id="3bbba-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bbba-164">RELATED LINKS</span></span>

[<span data-ttu-id="3bbba-165">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="3bbba-165">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="3bbba-166">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3bbba-166">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3bbba-167">Nowe — AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="3bbba-167">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
