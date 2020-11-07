---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: afae707fd66da5a54933d59bf63619145349e90b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707537"
---
# <span data-ttu-id="0d831-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0d831-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="0d831-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d831-102">SYNOPSIS</span></span>
<span data-ttu-id="0d831-103">Usuwa zapisane zasady dostępu z kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0d831-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="0d831-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d831-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d831-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0d831-105">DESCRIPTION</span></span>
<span data-ttu-id="0d831-106">Polecenie cmdlet **Remove-AzStorageContainerStoredAccessPolicy** usuwa zapisane zasady dostępu z kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0d831-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="0d831-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d831-107">EXAMPLES</span></span>

### <span data-ttu-id="0d831-108">Przykład 1: usuwanie zapisanych zasad dostępu z kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="0d831-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="0d831-109">To polecenie usuwa zasady dostępu o nazwie Policy03 z kontenera przechowywanego o nazwie.</span><span class="sxs-lookup"><span data-stu-id="0d831-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="0d831-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d831-110">PARAMETERS</span></span>

### <span data-ttu-id="0d831-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0d831-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0d831-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="0d831-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0d831-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="0d831-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0d831-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="0d831-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0d831-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0d831-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0d831-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="0d831-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0d831-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="0d831-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0d831-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="0d831-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0d831-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="0d831-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0d831-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="0d831-120">The default value is 10.</span></span>

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

### <span data-ttu-id="0d831-121">-Kontener</span><span class="sxs-lookup"><span data-stu-id="0d831-121">-Container</span></span>
<span data-ttu-id="0d831-122">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0d831-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d831-123">-Context</span><span class="sxs-lookup"><span data-stu-id="0d831-123">-Context</span></span>
<span data-ttu-id="0d831-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="0d831-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0d831-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0d831-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0d831-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d831-126">-DefaultProfile</span></span>
<span data-ttu-id="0d831-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d831-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d831-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d831-128">-PassThru</span></span>
<span data-ttu-id="0d831-129">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="0d831-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="0d831-130">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="0d831-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="0d831-131">-Policy</span><span class="sxs-lookup"><span data-stu-id="0d831-131">-Policy</span></span>
<span data-ttu-id="0d831-132">Określa nazwę zasad dostępu przechowywanych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d831-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d831-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0d831-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0d831-134">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="0d831-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0d831-135">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="0d831-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0d831-136">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="0d831-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0d831-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d831-137">-Confirm</span></span>
<span data-ttu-id="0d831-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d831-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d831-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d831-139">-WhatIf</span></span>
<span data-ttu-id="0d831-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d831-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d831-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0d831-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d831-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d831-142">CommonParameters</span></span>
<span data-ttu-id="0d831-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d831-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d831-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d831-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d831-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d831-145">INPUTS</span></span>

### <span data-ttu-id="0d831-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0d831-146">System.String</span></span>

### <span data-ttu-id="0d831-147">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0d831-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0d831-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d831-148">OUTPUTS</span></span>

### <span data-ttu-id="0d831-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d831-149">System.Boolean</span></span>

## <span data-ttu-id="0d831-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d831-150">NOTES</span></span>

## <span data-ttu-id="0d831-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d831-151">RELATED LINKS</span></span>

[<span data-ttu-id="0d831-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0d831-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="0d831-153">Nowe — AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0d831-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="0d831-154">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0d831-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0d831-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0d831-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
