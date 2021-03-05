---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: b306b5820e55687c1116adc56b92e1ee5ebd4115
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960001"
---
# <span data-ttu-id="19ece-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="19ece-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="19ece-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19ece-102">SYNOPSIS</span></span>
<span data-ttu-id="19ece-103">Zatrzymuje operację kopiowania do określonego pliku docelowego.</span><span class="sxs-lookup"><span data-stu-id="19ece-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="19ece-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="19ece-104">SYNTAX</span></span>

### <span data-ttu-id="19ece-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="19ece-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19ece-106">Plik</span><span class="sxs-lookup"><span data-stu-id="19ece-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19ece-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="19ece-107">DESCRIPTION</span></span>
<span data-ttu-id="19ece-108">Polecenie **cmdlet Stop-AzStorageFileCopy** zatrzymuje kopiowanie pliku do pliku docelowego.</span><span class="sxs-lookup"><span data-stu-id="19ece-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="19ece-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="19ece-109">EXAMPLES</span></span>

### <span data-ttu-id="19ece-110">Przykład 1. Zatrzymywanie operacji kopiowania</span><span class="sxs-lookup"><span data-stu-id="19ece-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="19ece-111">To polecenie zatrzymuje kopiowanie pliku o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="19ece-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="19ece-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19ece-112">PARAMETERS</span></span>

### <span data-ttu-id="19ece-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="19ece-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="19ece-114">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="19ece-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="19ece-115">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="19ece-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="19ece-116">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="19ece-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="19ece-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="19ece-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="19ece-118">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="19ece-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="19ece-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="19ece-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="19ece-120">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="19ece-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="19ece-121">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="19ece-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="19ece-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="19ece-122">The default value is 10.</span></span>

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

### <span data-ttu-id="19ece-123">— kontekst</span><span class="sxs-lookup"><span data-stu-id="19ece-123">-Context</span></span>
<span data-ttu-id="19ece-124">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="19ece-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="19ece-125">Aby uzyskać kontekst przechowywania, użyj polecenia cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="19ece-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="19ece-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="19ece-126">-CopyId</span></span>
<span data-ttu-id="19ece-127">Określa identyfikator operacji kopiowania.</span><span class="sxs-lookup"><span data-stu-id="19ece-127">Specifies the ID of the copy operation.</span></span>

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

### <span data-ttu-id="19ece-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19ece-128">-DefaultProfile</span></span>
<span data-ttu-id="19ece-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="19ece-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19ece-130">— Plik</span><span class="sxs-lookup"><span data-stu-id="19ece-130">-File</span></span>
<span data-ttu-id="19ece-131">Określa obiekt **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="19ece-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="19ece-132">Możesz utworzyć plik w chmurze lub uzyskać go za pomocą Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19ece-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19ece-133">- FilePath</span><span class="sxs-lookup"><span data-stu-id="19ece-133">-FilePath</span></span>
<span data-ttu-id="19ece-134">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="19ece-134">Specifies the path of a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19ece-135">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="19ece-135">-Force</span></span>
<span data-ttu-id="19ece-136">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="19ece-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="19ece-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="19ece-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="19ece-138">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="19ece-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="19ece-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="19ece-139">-ShareName</span></span>
<span data-ttu-id="19ece-140">Określa nazwę udziału.</span><span class="sxs-lookup"><span data-stu-id="19ece-140">Specifies the name of a share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19ece-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19ece-141">-Confirm</span></span>
<span data-ttu-id="19ece-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="19ece-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19ece-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19ece-143">-WhatIf</span></span>
<span data-ttu-id="19ece-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19ece-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19ece-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="19ece-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19ece-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19ece-146">CommonParameters</span></span>
<span data-ttu-id="19ece-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19ece-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19ece-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19ece-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19ece-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19ece-149">INPUTS</span></span>

### <span data-ttu-id="19ece-150">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="19ece-150">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="19ece-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="19ece-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="19ece-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19ece-152">OUTPUTS</span></span>

### <span data-ttu-id="19ece-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="19ece-153">System.Void</span></span>

## <span data-ttu-id="19ece-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="19ece-154">NOTES</span></span>

## <span data-ttu-id="19ece-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19ece-155">RELATED LINKS</span></span>

[<span data-ttu-id="19ece-156">Get-AzstorageFile</span><span class="sxs-lookup"><span data-stu-id="19ece-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="19ece-157">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="19ece-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="19ece-158">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="19ece-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="19ece-159">Start-AzstorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="19ece-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
