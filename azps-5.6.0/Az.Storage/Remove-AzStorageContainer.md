---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: e2d408e54aa4b4e2de766d4f4e058d2edd22cb22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970145"
---
# <span data-ttu-id="a9ca2-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a9ca2-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="a9ca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ca2-103">Usuwa określony kontener magazynu.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="a9ca2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a9ca2-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9ca2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a9ca2-105">DESCRIPTION</span></span>
<span data-ttu-id="a9ca2-106">Polecenie **cmdlet Remove-AzStorageContainer** usuwa określony kontener magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="a9ca2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a9ca2-107">EXAMPLES</span></span>

### <span data-ttu-id="a9ca2-108">Przykład 1. Usuwanie kontenera</span><span class="sxs-lookup"><span data-stu-id="a9ca2-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="a9ca2-109">W tym przykładzie usuwany jest kontener o nazwie MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="a9ca2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9ca2-110">PARAMETERS</span></span>

### <span data-ttu-id="a9ca2-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a9ca2-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a9ca2-112">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a9ca2-113">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a9ca2-114">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a9ca2-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a9ca2-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a9ca2-116">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a9ca2-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a9ca2-118">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a9ca2-119">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a9ca2-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-120">The default value is 10.</span></span>

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

### <span data-ttu-id="a9ca2-121">— kontekst</span><span class="sxs-lookup"><span data-stu-id="a9ca2-121">-Context</span></span>
<span data-ttu-id="a9ca2-122">Określa kontekst kontenera, który chcesz usunąć.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="a9ca2-123">Aby utworzyć New-AzStorageContext cmdlet, możesz użyć polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="a9ca2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ca2-124">-DefaultProfile</span></span>
<span data-ttu-id="a9ca2-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9ca2-126">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a9ca2-126">-Force</span></span>
<span data-ttu-id="a9ca2-127">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a9ca2-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a9ca2-128">-Name</span></span>
<span data-ttu-id="a9ca2-129">Określa nazwę kontenera do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-129">Specifies the name of the container to remove.</span></span>

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

### <span data-ttu-id="a9ca2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9ca2-130">-PassThru</span></span>
<span data-ttu-id="a9ca2-131">Wskazuje, że to polecenie cmdlet zwraca **wartość** logiczną, która odzwierciedla sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a9ca2-132">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a9ca2-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a9ca2-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a9ca2-134">Określa interwał po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a9ca2-135">Jeśli określony interwał pominie się przed rozpoczęciem przetwarzania żądania przez usługę magazynu, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a9ca2-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9ca2-136">-Confirm</span></span>
<span data-ttu-id="a9ca2-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9ca2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9ca2-138">-WhatIf</span></span>
<span data-ttu-id="a9ca2-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9ca2-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9ca2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ca2-141">CommonParameters</span></span>
<span data-ttu-id="a9ca2-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9ca2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ca2-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9ca2-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ca2-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9ca2-144">INPUTS</span></span>

### <span data-ttu-id="a9ca2-145">System.String</span><span class="sxs-lookup"><span data-stu-id="a9ca2-145">System.String</span></span>

### <span data-ttu-id="a9ca2-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a9ca2-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a9ca2-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9ca2-147">OUTPUTS</span></span>

### <span data-ttu-id="a9ca2-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9ca2-148">System.Boolean</span></span>

## <span data-ttu-id="a9ca2-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a9ca2-149">NOTES</span></span>

## <span data-ttu-id="a9ca2-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9ca2-150">RELATED LINKS</span></span>

[<span data-ttu-id="a9ca2-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a9ca2-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="a9ca2-152">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a9ca2-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
