---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: d8c9e0e49ba7a5caa9cb93290ef5e96b60fd4430
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190754"
---
# <span data-ttu-id="9c10e-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9c10e-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="9c10e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c10e-102">SYNOPSIS</span></span>
<span data-ttu-id="9c10e-103">Usuwa przechowywane zasady dostępu z udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="9c10e-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="9c10e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9c10e-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c10e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9c10e-105">DESCRIPTION</span></span>
<span data-ttu-id="9c10e-106">Polecenie **cmdlet Remove-AzStorageShareStoredAccessPolicy** usuwa przechowywane zasady dostępu z udziału magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9c10e-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="9c10e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9c10e-107">EXAMPLES</span></span>

### <span data-ttu-id="9c10e-108">Przykład 1. Usuwanie przechowywanych zasad dostępu z udziału magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="9c10e-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="9c10e-109">To polecenie usuwa przechowywane zasady dostępu o nazwie GeneralPolicy z programu ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="9c10e-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="9c10e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c10e-110">PARAMETERS</span></span>

### <span data-ttu-id="9c10e-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9c10e-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9c10e-112">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="9c10e-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9c10e-113">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="9c10e-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9c10e-114">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="9c10e-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9c10e-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9c10e-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9c10e-116">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9c10e-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9c10e-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9c10e-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9c10e-118">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="9c10e-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9c10e-119">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="9c10e-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9c10e-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="9c10e-120">The default value is 10.</span></span>

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

### <span data-ttu-id="9c10e-121">— kontekst</span><span class="sxs-lookup"><span data-stu-id="9c10e-121">-Context</span></span>
<span data-ttu-id="9c10e-122">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9c10e-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9c10e-123">Aby uzyskać kontekst magazynowania, użyj polecenia cmdlet [New-azStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="9c10e-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="9c10e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c10e-124">-DefaultProfile</span></span>
<span data-ttu-id="9c10e-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c10e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c10e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c10e-126">-PassThru</span></span>
<span data-ttu-id="9c10e-127">Wskazuje, że to polecenie cmdlet zwraca **wartość** logiczną, która odzwierciedla sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="9c10e-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="9c10e-128">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="9c10e-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9c10e-129">— Zasady</span><span class="sxs-lookup"><span data-stu-id="9c10e-129">-Policy</span></span>
<span data-ttu-id="9c10e-130">Określa nazwę przechowywanych zasad dostępu usuwanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c10e-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9c10e-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9c10e-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9c10e-132">Określa długość okresu, przez który uchybnia część żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="9c10e-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9c10e-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9c10e-133">-ShareName</span></span>
<span data-ttu-id="9c10e-134">Określa nazwę udziału magazynu, dla którego to polecenie cmdlet usuwa zasady.</span><span class="sxs-lookup"><span data-stu-id="9c10e-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="9c10e-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c10e-135">-Confirm</span></span>
<span data-ttu-id="9c10e-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9c10e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c10e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c10e-137">-WhatIf</span></span>
<span data-ttu-id="9c10e-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c10e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c10e-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9c10e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c10e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c10e-140">CommonParameters</span></span>
<span data-ttu-id="9c10e-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c10e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c10e-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c10e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c10e-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c10e-143">INPUTS</span></span>

### <span data-ttu-id="9c10e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9c10e-144">System.String</span></span>

### <span data-ttu-id="9c10e-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9c10e-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9c10e-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c10e-146">OUTPUTS</span></span>

### <span data-ttu-id="9c10e-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9c10e-147">System.Boolean</span></span>

## <span data-ttu-id="9c10e-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9c10e-148">NOTES</span></span>

## <span data-ttu-id="9c10e-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c10e-149">RELATED LINKS</span></span>

[<span data-ttu-id="9c10e-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9c10e-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="9c10e-151">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9c10e-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="9c10e-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9c10e-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="9c10e-153">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9c10e-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
