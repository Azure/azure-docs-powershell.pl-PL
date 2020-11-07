---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainer
schema: 2.0.0
ms.openlocfilehash: 24eba8b6aeedb2f240fbd7da16b1b7a76ee9d759
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899164"
---
# <span data-ttu-id="43847-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="43847-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="43847-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43847-102">SYNOPSIS</span></span>
<span data-ttu-id="43847-103">Usuwa określony kontener magazynu.</span><span class="sxs-lookup"><span data-stu-id="43847-103">Removes the specified storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43847-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43847-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43847-105">Opis</span><span class="sxs-lookup"><span data-stu-id="43847-105">DESCRIPTION</span></span>
<span data-ttu-id="43847-106">Polecenie cmdlet **Remove-AzureStorageContainer** usuwa określony kontener magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="43847-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="43847-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43847-107">EXAMPLES</span></span>

### <span data-ttu-id="43847-108">Przykład 1. Usuń kontener</span><span class="sxs-lookup"><span data-stu-id="43847-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="43847-109">W tym przykładzie usunięto kontener o nazwie MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="43847-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="43847-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43847-110">PARAMETERS</span></span>

### <span data-ttu-id="43847-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="43847-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="43847-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="43847-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="43847-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="43847-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="43847-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="43847-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="43847-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="43847-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="43847-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="43847-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="43847-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="43847-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="43847-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="43847-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="43847-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="43847-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="43847-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="43847-120">The default value is 10.</span></span>

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

### <span data-ttu-id="43847-121">-Context</span><span class="sxs-lookup"><span data-stu-id="43847-121">-Context</span></span>
<span data-ttu-id="43847-122">Określa kontekst kontenera, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="43847-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="43847-123">Za pomocą polecenia cmdlet New-AzureStorageContext możesz je utworzyć.</span><span class="sxs-lookup"><span data-stu-id="43847-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="43847-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43847-124">-DefaultProfile</span></span>
<span data-ttu-id="43847-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43847-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43847-126">-Force</span><span class="sxs-lookup"><span data-stu-id="43847-126">-Force</span></span>
<span data-ttu-id="43847-127">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="43847-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="43847-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43847-128">-Name</span></span>
<span data-ttu-id="43847-129">Określa nazwę kontenera do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="43847-129">Specifies the name of the container to remove.</span></span>

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

### <span data-ttu-id="43847-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43847-130">-PassThru</span></span>
<span data-ttu-id="43847-131">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="43847-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="43847-132">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="43847-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="43847-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="43847-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="43847-134">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="43847-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="43847-135">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="43847-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="43847-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43847-136">-Confirm</span></span>
<span data-ttu-id="43847-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43847-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43847-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43847-138">-WhatIf</span></span>
<span data-ttu-id="43847-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43847-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43847-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="43847-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43847-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43847-141">CommonParameters</span></span>
<span data-ttu-id="43847-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43847-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43847-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43847-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43847-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43847-144">INPUTS</span></span>

### <span data-ttu-id="43847-145">System. String</span><span class="sxs-lookup"><span data-stu-id="43847-145">System.String</span></span>

### <span data-ttu-id="43847-146">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="43847-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="43847-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43847-147">OUTPUTS</span></span>

### <span data-ttu-id="43847-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43847-148">System.Boolean</span></span>

## <span data-ttu-id="43847-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43847-149">NOTES</span></span>

## <span data-ttu-id="43847-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43847-150">RELATED LINKS</span></span>

[<span data-ttu-id="43847-151">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="43847-151">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="43847-152">Nowe — AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="43847-152">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)
