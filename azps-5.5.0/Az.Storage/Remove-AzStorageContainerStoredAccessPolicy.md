---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 1b8667d08e02c9294a18f4cbf84cb27085cbc118
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197515"
---
# <span data-ttu-id="fa07e-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa07e-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="fa07e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa07e-102">SYNOPSIS</span></span>
<span data-ttu-id="fa07e-103">Usuwa przechowywane zasady dostępu z kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fa07e-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="fa07e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fa07e-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa07e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fa07e-105">DESCRIPTION</span></span>
<span data-ttu-id="fa07e-106">Polecenie **cmdlet Remove-AzStorageContainerStoredAccessPolicy** usuwa przechowywane zasady dostępu z kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fa07e-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="fa07e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fa07e-107">EXAMPLES</span></span>

### <span data-ttu-id="fa07e-108">Przykład 1. Usuwanie przechowywanych zasad dostępu z kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="fa07e-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="fa07e-109">To polecenie usuwa zasady dostępu o nazwie Zasady03 z przechowywanego kontenera o nazwie MyContainer.</span><span class="sxs-lookup"><span data-stu-id="fa07e-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="fa07e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa07e-110">PARAMETERS</span></span>

### <span data-ttu-id="fa07e-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fa07e-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fa07e-112">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="fa07e-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fa07e-113">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="fa07e-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fa07e-114">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="fa07e-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fa07e-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fa07e-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fa07e-116">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="fa07e-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fa07e-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="fa07e-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fa07e-118">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="fa07e-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fa07e-119">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="fa07e-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fa07e-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="fa07e-120">The default value is 10.</span></span>

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

### <span data-ttu-id="fa07e-121">— Kontener</span><span class="sxs-lookup"><span data-stu-id="fa07e-121">-Container</span></span>
<span data-ttu-id="fa07e-122">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fa07e-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="fa07e-123">— kontekst</span><span class="sxs-lookup"><span data-stu-id="fa07e-123">-Context</span></span>
<span data-ttu-id="fa07e-124">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fa07e-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fa07e-125">Aby uzyskać kontekst magazynowania, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa07e-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fa07e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa07e-126">-DefaultProfile</span></span>
<span data-ttu-id="fa07e-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa07e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa07e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa07e-128">-PassThru</span></span>
<span data-ttu-id="fa07e-129">Wskazuje, że to polecenie cmdlet zwraca **wartość** logiczną, która odzwierciedla sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="fa07e-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="fa07e-130">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="fa07e-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="fa07e-131">— Zasady</span><span class="sxs-lookup"><span data-stu-id="fa07e-131">-Policy</span></span>
<span data-ttu-id="fa07e-132">Określa nazwę przechowywanych zasad dostępu usuwanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa07e-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fa07e-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fa07e-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fa07e-134">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="fa07e-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fa07e-135">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="fa07e-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fa07e-136">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="fa07e-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fa07e-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa07e-137">-Confirm</span></span>
<span data-ttu-id="fa07e-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fa07e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa07e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa07e-139">-WhatIf</span></span>
<span data-ttu-id="fa07e-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa07e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa07e-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fa07e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa07e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa07e-142">CommonParameters</span></span>
<span data-ttu-id="fa07e-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa07e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa07e-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa07e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa07e-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa07e-145">INPUTS</span></span>

### <span data-ttu-id="fa07e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="fa07e-146">System.String</span></span>

### <span data-ttu-id="fa07e-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fa07e-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fa07e-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa07e-148">OUTPUTS</span></span>

### <span data-ttu-id="fa07e-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa07e-149">System.Boolean</span></span>

## <span data-ttu-id="fa07e-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fa07e-150">NOTES</span></span>

## <span data-ttu-id="fa07e-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa07e-151">RELATED LINKS</span></span>

[<span data-ttu-id="fa07e-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa07e-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="fa07e-153">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa07e-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="fa07e-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fa07e-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="fa07e-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa07e-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
