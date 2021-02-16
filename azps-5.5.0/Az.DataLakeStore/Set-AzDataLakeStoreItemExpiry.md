---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: ff769801c7a3496ab094e5c9877e0b53fb64fbfd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243851"
---
# <span data-ttu-id="115fd-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="115fd-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="115fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="115fd-102">SYNOPSIS</span></span>
<span data-ttu-id="115fd-103">Ustawia lub usuwa czas wygaśnięcia pliku na koncie usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="115fd-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="115fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="115fd-104">SYNTAX</span></span>

### <span data-ttu-id="115fd-105">SetAbsoluteNeverExpireExpiry (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="115fd-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="115fd-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="115fd-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="115fd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="115fd-107">DESCRIPTION</span></span>
<span data-ttu-id="115fd-108">Polecenie **cmdlet Set-AzDataLakeStoreItemExpiry** ustawia lub usuwa czas wygaśnięcia pliku na koncie usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="115fd-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="115fd-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="115fd-109">EXAMPLES</span></span>

### <span data-ttu-id="115fd-110">Przykład 1. Ustawianie czasu wygaśnięcia pliku</span><span class="sxs-lookup"><span data-stu-id="115fd-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="115fd-111">Ustawia datę wygaśnięcia pliku w myfile.txt konta ContosoADL na dwie godziny.</span><span class="sxs-lookup"><span data-stu-id="115fd-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="115fd-112">Spowoduje to wygaśnięcie pliku (oznaczonego do usunięcia) w ciągu dwóch godzin.</span><span class="sxs-lookup"><span data-stu-id="115fd-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="115fd-113">Przykład 2. Usunięcie wygaśnięcia pliku</span><span class="sxs-lookup"><span data-stu-id="115fd-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="115fd-114">Usuwa wszelkie wygaśnięcia ustawione wcześniej dla pliku "myfile.txt" na koncie "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="115fd-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="115fd-115">Oznacza to, że plik nie wygaśnie automatycznie (zostanie oznaczony do usunięcia) i będzie trzeba go usunąć ręcznie lub ustawić do wygaśnięcia ponownie.</span><span class="sxs-lookup"><span data-stu-id="115fd-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="115fd-116">Przykład 3. Ustawianie czasu wygaśnięcia pliku względem teraz</span><span class="sxs-lookup"><span data-stu-id="115fd-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="115fd-117">Pierwsze polecenie ustawia czas wygaśnięcia pliku /myfile.txt 240 sekund względem bieżącego czasu na serwerze.</span><span class="sxs-lookup"><span data-stu-id="115fd-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="115fd-118">Drugie polecenie ustawia czas wygaśnięcia pliku /myfile.txt 240 sekund względem czasu utworzenia pliku na serwerze.</span><span class="sxs-lookup"><span data-stu-id="115fd-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="115fd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="115fd-119">PARAMETERS</span></span>

### <span data-ttu-id="115fd-120">— Konto</span><span class="sxs-lookup"><span data-stu-id="115fd-120">-Account</span></span>
<span data-ttu-id="115fd-121">Określa nazwę konta w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="115fd-121">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115fd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="115fd-122">-DefaultProfile</span></span>
<span data-ttu-id="115fd-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="115fd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115fd-124">— wygasanie</span><span class="sxs-lookup"><span data-stu-id="115fd-124">-Expiration</span></span>
<span data-ttu-id="115fd-125">Bezwzględny czas wygaśnięcia dla określonego pliku.</span><span class="sxs-lookup"><span data-stu-id="115fd-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="115fd-126">Jeśli nie ma żadnej wartości lub nie ustawiono wartości MaxValue, plik nigdy nie wygaśnie.</span><span class="sxs-lookup"><span data-stu-id="115fd-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115fd-127">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="115fd-127">-Path</span></span>
<span data-ttu-id="115fd-128">Określa ścieżkę magazynu jeziora Data Lake Store elementu pliku, dla którego ma być ustawiana lub usuwana data wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="115fd-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115fd-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="115fd-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="115fd-130">Względne opcje wygasania.</span><span class="sxs-lookup"><span data-stu-id="115fd-130">Relative expiry options.</span></span> <span data-ttu-id="115fd-131">RelativeToNow lub RelativeToCreationDate to bieżące opcje</span><span class="sxs-lookup"><span data-stu-id="115fd-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115fd-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="115fd-132">-RelativeTime</span></span>
<span data-ttu-id="115fd-133">Względny czas (w milisekundach) względem czasu teraz lub czasu utworzenia</span><span class="sxs-lookup"><span data-stu-id="115fd-133">The relative time in milliseconds with respect to now or creation time</span></span>

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115fd-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="115fd-134">-Confirm</span></span>
<span data-ttu-id="115fd-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="115fd-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115fd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="115fd-136">-WhatIf</span></span>
<span data-ttu-id="115fd-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="115fd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="115fd-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="115fd-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115fd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="115fd-139">CommonParameters</span></span>
<span data-ttu-id="115fd-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="115fd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="115fd-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="115fd-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="115fd-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="115fd-142">INPUTS</span></span>

### <span data-ttu-id="115fd-143">System.String</span><span class="sxs-lookup"><span data-stu-id="115fd-143">System.String</span></span>

### <span data-ttu-id="115fd-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="115fd-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="115fd-145">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="115fd-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="115fd-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="115fd-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="115fd-147">System.Int64</span><span class="sxs-lookup"><span data-stu-id="115fd-147">System.Int64</span></span>

## <span data-ttu-id="115fd-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="115fd-148">OUTPUTS</span></span>

### <span data-ttu-id="115fd-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="115fd-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="115fd-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="115fd-150">NOTES</span></span>
<span data-ttu-id="115fd-151">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="115fd-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="115fd-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="115fd-152">RELATED LINKS</span></span>

[<span data-ttu-id="115fd-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="115fd-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

