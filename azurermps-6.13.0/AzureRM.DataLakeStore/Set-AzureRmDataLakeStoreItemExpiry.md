---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: 4aff82a2621a462f0af14fe2dce620f297011874
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543911"
---
# <span data-ttu-id="4c720-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="4c720-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="4c720-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c720-102">SYNOPSIS</span></span>
<span data-ttu-id="4c720-103">Ustawia lub usuwa czas wygaśnięcia pliku na koncie usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4c720-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c720-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c720-104">SYNTAX</span></span>

### <span data-ttu-id="4c720-105">SetAbsoluteNeverExpireExpiry (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4c720-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c720-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="4c720-106">SetRelativeExpiry</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c720-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4c720-107">DESCRIPTION</span></span>
<span data-ttu-id="4c720-108">Polecenie cmdlet **Set-AzureRmDataLakeStoreItemExpiry** ustawia lub usuwa czas wygaśnięcia pliku na koncie usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4c720-108">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="4c720-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c720-109">EXAMPLES</span></span>

### <span data-ttu-id="4c720-110">Przykład 1. Ustawianie czasu wygaśnięcia pliku</span><span class="sxs-lookup"><span data-stu-id="4c720-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="4c720-111">Umożliwia ustawienie daty wygaśnięcia dla pliku myfile.txt na koncie ContosoADL od razu do dwóch godzin.</span><span class="sxs-lookup"><span data-stu-id="4c720-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="4c720-112">Spowoduje to wygaśnięcie pliku (oznaczenie go do usunięcia) w ciągu dwóch godzin.</span><span class="sxs-lookup"><span data-stu-id="4c720-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="4c720-113">Przykład 2: usuwanie wygaśnięcia pliku</span><span class="sxs-lookup"><span data-stu-id="4c720-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="4c720-114">Usuwa wszystkie wygaśnięcia, które zostały wcześniej ustawione w pliku "myfile.txt" na koncie "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="4c720-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="4c720-115">Oznacza to, że plik nie zostanie automatycznie wygaśnie (oznaczony do usunięcia) i trzeba będzie ręcznie usunąć lub ponownie ustawić ważność.</span><span class="sxs-lookup"><span data-stu-id="4c720-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="4c720-116">Przykład 3: Ustawianie czasu wygaśnięcia dla pliku względem tej pory</span><span class="sxs-lookup"><span data-stu-id="4c720-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="4c720-117">Pierwsze polecenie ustawia czas wygaśnięcia pliku/myfile.txt 240 sekund względem bieżącego czasu na serwerze.</span><span class="sxs-lookup"><span data-stu-id="4c720-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="4c720-118">Drugie polecenie ustawia czas wygaśnięcia pliku/myfile.txt 240 sekund w odniesieniu do czasu utworzenia na serwerze.</span><span class="sxs-lookup"><span data-stu-id="4c720-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="4c720-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c720-119">PARAMETERS</span></span>

### <span data-ttu-id="4c720-120">— Konto</span><span class="sxs-lookup"><span data-stu-id="4c720-120">-Account</span></span>
<span data-ttu-id="4c720-121">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4c720-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="4c720-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c720-122">-DefaultProfile</span></span>
<span data-ttu-id="4c720-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c720-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c720-124">-Data wygaśnięcia</span><span class="sxs-lookup"><span data-stu-id="4c720-124">-Expiration</span></span>
<span data-ttu-id="4c720-125">Bezwzględny czas wygaśnięcia określonego pliku.</span><span class="sxs-lookup"><span data-stu-id="4c720-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="4c720-126">Jeśli nie ma wartości ani nie jest ustawiona wartość MaxValue, plik nigdy nie wygaśnie.</span><span class="sxs-lookup"><span data-stu-id="4c720-126">If no value or set to MaxValue, the file will never expire.</span></span>

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

### <span data-ttu-id="4c720-127">-Path</span><span class="sxs-lookup"><span data-stu-id="4c720-127">-Path</span></span>
<span data-ttu-id="4c720-128">Określa ścieżkę do usługi Data Lake Store dla elementu pliku, dla którego ma zostać ustawiony lub usunięty wygasanie.</span><span class="sxs-lookup"><span data-stu-id="4c720-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="4c720-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="4c720-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="4c720-130">Względne opcje wygasania.</span><span class="sxs-lookup"><span data-stu-id="4c720-130">Relative expiry options.</span></span> <span data-ttu-id="4c720-131">RelativeToNow lub RelativeToCreationDate to bieżące opcje</span><span class="sxs-lookup"><span data-stu-id="4c720-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

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

### <span data-ttu-id="4c720-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="4c720-132">-RelativeTime</span></span>
<span data-ttu-id="4c720-133">Względny czas (w milisekundach) dotyczący czasu teraz lub utworzenia</span><span class="sxs-lookup"><span data-stu-id="4c720-133">The relative time in milliseconds with respect to now or creation time</span></span>

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

### <span data-ttu-id="4c720-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c720-134">-Confirm</span></span>
<span data-ttu-id="4c720-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c720-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c720-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c720-136">-WhatIf</span></span>
<span data-ttu-id="4c720-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c720-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c720-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4c720-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c720-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c720-139">CommonParameters</span></span>
<span data-ttu-id="4c720-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c720-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c720-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c720-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c720-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c720-142">INPUTS</span></span>

### <span data-ttu-id="4c720-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4c720-143">System.String</span></span>

### <span data-ttu-id="4c720-144">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4c720-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4c720-145">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4c720-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="4c720-146">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreEnums + PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="4c720-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="4c720-147">System. Int64</span><span class="sxs-lookup"><span data-stu-id="4c720-147">System.Int64</span></span>

## <span data-ttu-id="4c720-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c720-148">OUTPUTS</span></span>

### <span data-ttu-id="4c720-149">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4c720-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="4c720-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c720-150">NOTES</span></span>
<span data-ttu-id="4c720-151">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="4c720-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="4c720-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c720-152">RELATED LINKS</span></span>

[<span data-ttu-id="4c720-153">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4c720-153">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)
