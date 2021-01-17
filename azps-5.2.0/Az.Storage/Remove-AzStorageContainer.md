---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: a6ea7a2686d084b241e1ba3ff5c513c0d03128c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348529"
---
# <span data-ttu-id="f8676-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f8676-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="f8676-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8676-102">SYNOPSIS</span></span>
<span data-ttu-id="f8676-103">Usuwa określony kontener magazynu.</span><span class="sxs-lookup"><span data-stu-id="f8676-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="f8676-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8676-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8676-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f8676-105">DESCRIPTION</span></span>
<span data-ttu-id="f8676-106">Polecenie cmdlet **Remove-AzStorageContainer** usuwa określony kontener magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f8676-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="f8676-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8676-107">EXAMPLES</span></span>

### <span data-ttu-id="f8676-108">Przykład 1. Usuń kontener</span><span class="sxs-lookup"><span data-stu-id="f8676-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="f8676-109">W tym przykładzie usunięto kontener o nazwie MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="f8676-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="f8676-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8676-110">PARAMETERS</span></span>

### <span data-ttu-id="f8676-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f8676-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f8676-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="f8676-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f8676-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="f8676-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f8676-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="f8676-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f8676-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f8676-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f8676-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="f8676-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f8676-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="f8676-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f8676-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="f8676-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f8676-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="f8676-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f8676-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="f8676-120">The default value is 10.</span></span>

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

### <span data-ttu-id="f8676-121">-Context</span><span class="sxs-lookup"><span data-stu-id="f8676-121">-Context</span></span>
<span data-ttu-id="f8676-122">Określa kontekst kontenera, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="f8676-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="f8676-123">Za pomocą polecenia cmdlet New-AzStorageContext możesz je utworzyć.</span><span class="sxs-lookup"><span data-stu-id="f8676-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="f8676-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8676-124">-DefaultProfile</span></span>
<span data-ttu-id="f8676-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8676-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8676-126">-Force</span><span class="sxs-lookup"><span data-stu-id="f8676-126">-Force</span></span>
<span data-ttu-id="f8676-127">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f8676-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f8676-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8676-128">-Name</span></span>
<span data-ttu-id="f8676-129">Określa nazwę kontenera do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f8676-129">Specifies the name of the container to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8676-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8676-130">-PassThru</span></span>
<span data-ttu-id="f8676-131">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="f8676-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f8676-132">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="f8676-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f8676-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f8676-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f8676-134">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="f8676-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="f8676-135">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="f8676-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="f8676-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8676-136">-Confirm</span></span>
<span data-ttu-id="f8676-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8676-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8676-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8676-138">-WhatIf</span></span>
<span data-ttu-id="f8676-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8676-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8676-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f8676-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8676-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8676-141">CommonParameters</span></span>
<span data-ttu-id="f8676-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8676-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8676-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8676-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8676-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8676-144">INPUTS</span></span>

### <span data-ttu-id="f8676-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f8676-145">System.String</span></span>

### <span data-ttu-id="f8676-146">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f8676-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f8676-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8676-147">OUTPUTS</span></span>

### <span data-ttu-id="f8676-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8676-148">System.Boolean</span></span>

## <span data-ttu-id="f8676-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8676-149">NOTES</span></span>

## <span data-ttu-id="f8676-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8676-150">RELATED LINKS</span></span>

[<span data-ttu-id="f8676-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f8676-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="f8676-152">Nowe — AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f8676-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
