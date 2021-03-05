---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 9a6702b59bbe2e0305966cd9a1323edc120e86c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961242"
---
# <span data-ttu-id="f7344-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f7344-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="f7344-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7344-102">SYNOPSIS</span></span>
<span data-ttu-id="f7344-103">Usuwa przechowywane zasady dostępu z udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="f7344-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="f7344-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f7344-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7344-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f7344-105">DESCRIPTION</span></span>
<span data-ttu-id="f7344-106">Polecenie **cmdlet Remove-AzStorageShareStoredAccessPolicy** usuwa przechowywane zasady dostępu z udziału magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f7344-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="f7344-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f7344-107">EXAMPLES</span></span>

### <span data-ttu-id="f7344-108">Przykład 1. Usuwanie przechowywanych zasad dostępu z udziału magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f7344-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="f7344-109">To polecenie usuwa przechowywane zasady dostępu o nazwie GeneralPolicy z programu ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="f7344-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="f7344-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7344-110">PARAMETERS</span></span>

### <span data-ttu-id="f7344-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f7344-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f7344-112">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="f7344-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f7344-113">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="f7344-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f7344-114">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="f7344-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f7344-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f7344-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f7344-116">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="f7344-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f7344-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="f7344-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f7344-118">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="f7344-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f7344-119">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="f7344-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f7344-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="f7344-120">The default value is 10.</span></span>

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

### <span data-ttu-id="f7344-121">— kontekst</span><span class="sxs-lookup"><span data-stu-id="f7344-121">-Context</span></span>
<span data-ttu-id="f7344-122">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f7344-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f7344-123">Aby uzyskać kontekst przechowywania, użyj polecenia cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="f7344-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f7344-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7344-124">-DefaultProfile</span></span>
<span data-ttu-id="f7344-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7344-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7344-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7344-126">-PassThru</span></span>
<span data-ttu-id="f7344-127">Wskazuje, że to polecenie cmdlet zwraca **wartość** logiczną, która odzwierciedla sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="f7344-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f7344-128">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="f7344-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f7344-129">— Zasady</span><span class="sxs-lookup"><span data-stu-id="f7344-129">-Policy</span></span>
<span data-ttu-id="f7344-130">Określa nazwę przechowywanych zasad dostępu usuwanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7344-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f7344-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f7344-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f7344-132">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="f7344-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f7344-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f7344-133">-ShareName</span></span>
<span data-ttu-id="f7344-134">Określa nazwę udziału magazynu, dla którego to polecenie cmdlet usuwa zasady.</span><span class="sxs-lookup"><span data-stu-id="f7344-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="f7344-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7344-135">-Confirm</span></span>
<span data-ttu-id="f7344-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f7344-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7344-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7344-137">-WhatIf</span></span>
<span data-ttu-id="f7344-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7344-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7344-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f7344-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7344-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7344-140">CommonParameters</span></span>
<span data-ttu-id="f7344-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7344-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7344-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7344-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7344-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7344-143">INPUTS</span></span>

### <span data-ttu-id="f7344-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f7344-144">System.String</span></span>

### <span data-ttu-id="f7344-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f7344-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f7344-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7344-146">OUTPUTS</span></span>

### <span data-ttu-id="f7344-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f7344-147">System.Boolean</span></span>

## <span data-ttu-id="f7344-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f7344-148">NOTES</span></span>

## <span data-ttu-id="f7344-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7344-149">RELATED LINKS</span></span>

[<span data-ttu-id="f7344-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f7344-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="f7344-151">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f7344-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="f7344-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f7344-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f7344-153">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f7344-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
