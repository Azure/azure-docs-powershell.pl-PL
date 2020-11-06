---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f4dfc77be9006229e2919dd1a4e0cdb1dd8c548e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548472"
---
# <span data-ttu-id="f3db6-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f3db6-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="f3db6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3db6-102">SYNOPSIS</span></span>
<span data-ttu-id="f3db6-103">Ustawia zasady dostępu przechowywane dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f3db6-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3db6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3db6-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3db6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f3db6-105">DESCRIPTION</span></span>
<span data-ttu-id="f3db6-106">Polecenie cmdlet **Set-AzureStorageTableStoredAccessPolicy** ustawia zasady dostępu przechowywane dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f3db6-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="f3db6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3db6-107">EXAMPLES</span></span>

### <span data-ttu-id="f3db6-108">Przykład 1: Ustawianie zasad dostępu przechowywanych w tabeli z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="f3db6-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="f3db6-109">To polecenie ustawia zasady dostępu o nazwie Policy08 dla tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="f3db6-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="f3db6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3db6-110">PARAMETERS</span></span>

### <span data-ttu-id="f3db6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f3db6-111">-Context</span></span>
<span data-ttu-id="f3db6-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="f3db6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f3db6-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f3db6-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3db6-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f3db6-114">-ExpiryTime</span></span>
<span data-ttu-id="f3db6-115">Określa godzinę wygaśnięcia przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="f3db6-115">Specifies the time at which the stored access policy expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3db6-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f3db6-116">-NoExpiryTime</span></span>
<span data-ttu-id="f3db6-117">Wskazuje, że zasady dostępu nie mają daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="f3db6-117">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3db6-118">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="f3db6-118">-NoStartTime</span></span>
<span data-ttu-id="f3db6-119">Wskazuje, że godzina rozpoczęcia jest ustawiona na $Null.</span><span class="sxs-lookup"><span data-stu-id="f3db6-119">Indicates that the start time is set to $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3db6-120">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="f3db6-120">-Permission</span></span>
<span data-ttu-id="f3db6-121">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do tabeli magazynów.</span><span class="sxs-lookup"><span data-stu-id="f3db6-121">Specifies permissions in the stored access policy to access the storage table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3db6-122">-Policy</span><span class="sxs-lookup"><span data-stu-id="f3db6-122">-Policy</span></span>
<span data-ttu-id="f3db6-123">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="f3db6-123">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3db6-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f3db6-124">-StartTime</span></span>
<span data-ttu-id="f3db6-125">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="f3db6-125">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3db6-126">-Table</span><span class="sxs-lookup"><span data-stu-id="f3db6-126">-Table</span></span>
<span data-ttu-id="f3db6-127">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f3db6-127">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3db6-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3db6-128">-Confirm</span></span>
<span data-ttu-id="f3db6-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3db6-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3db6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3db6-130">-WhatIf</span></span>
<span data-ttu-id="f3db6-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3db6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3db6-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f3db6-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3db6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3db6-133">CommonParameters</span></span>
<span data-ttu-id="f3db6-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3db6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3db6-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3db6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3db6-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3db6-136">INPUTS</span></span>

### <span data-ttu-id="f3db6-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f3db6-137">IStorageContext</span></span>

<span data-ttu-id="f3db6-138">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="f3db6-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="f3db6-139">Ciąg</span><span class="sxs-lookup"><span data-stu-id="f3db6-139">String</span></span>

<span data-ttu-id="f3db6-140">Parametr "Tabela" przyjmuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="f3db6-140">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f3db6-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3db6-141">OUTPUTS</span></span>

### <span data-ttu-id="f3db6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f3db6-142">System.String</span></span>

## <span data-ttu-id="f3db6-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3db6-143">NOTES</span></span>

## <span data-ttu-id="f3db6-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3db6-144">RELATED LINKS</span></span>

[<span data-ttu-id="f3db6-145">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f3db6-145">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f3db6-146">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f3db6-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="f3db6-147">Nowe — AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f3db6-147">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f3db6-148">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f3db6-148">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
