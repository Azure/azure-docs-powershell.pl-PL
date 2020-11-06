---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
ms.openlocfilehash: d517ca49f0be3b6add58d151b3b2f79dad17611c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524121"
---
# <span data-ttu-id="eb9d2-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb9d2-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="eb9d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb9d2-102">SYNOPSIS</span></span>
<span data-ttu-id="eb9d2-103">Ustawia zasady dostępu przechowywane dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="eb9d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb9d2-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb9d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eb9d2-105">DESCRIPTION</span></span>
<span data-ttu-id="eb9d2-106">Polecenie cmdlet **Set-AzureStorageTableStoredAccessPolicy** ustawia zasady dostępu przechowywane dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="eb9d2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb9d2-107">EXAMPLES</span></span>

### <span data-ttu-id="eb9d2-108">Przykład 1: Ustawianie zasad dostępu przechowywanych w tabeli z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="eb9d2-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08"
```

<span data-ttu-id="eb9d2-109">To polecenie ustawia zasady dostępu o nazwie Policy08 dla tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="eb9d2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb9d2-110">PARAMETERS</span></span>

### <span data-ttu-id="eb9d2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="eb9d2-111">-Context</span></span>
<span data-ttu-id="eb9d2-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="eb9d2-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="eb9d2-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="eb9d2-114">-ExpiryTime</span></span>
<span data-ttu-id="eb9d2-115">Określa godzinę wygaśnięcia przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-115">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="eb9d2-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="eb9d2-116">-NoExpiryTime</span></span>
<span data-ttu-id="eb9d2-117">Wskazuje, że zasady dostępu nie mają daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="eb9d2-118">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="eb9d2-118">-NoStartTime</span></span>
<span data-ttu-id="eb9d2-119">Wskazuje, że godzina rozpoczęcia jest ustawiona na $Null.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="eb9d2-120">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="eb9d2-120">-Permission</span></span>
<span data-ttu-id="eb9d2-121">Określa poziom dostępu publicznego do tej tabeli magazynu.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-121">Specifies the level of public access to this storage table.</span></span>

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

### <span data-ttu-id="eb9d2-122">-Policy</span><span class="sxs-lookup"><span data-stu-id="eb9d2-122">-Policy</span></span>
<span data-ttu-id="eb9d2-123">Określa zapisane zasady dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="eb9d2-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="eb9d2-124">-StartTime</span></span>
<span data-ttu-id="eb9d2-125">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-125">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="eb9d2-126">-Table</span><span class="sxs-lookup"><span data-stu-id="eb9d2-126">-Table</span></span>
<span data-ttu-id="eb9d2-127">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-127">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="eb9d2-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eb9d2-128">-Confirm</span></span>
<span data-ttu-id="eb9d2-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb9d2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb9d2-130">-WhatIf</span></span>
<span data-ttu-id="eb9d2-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb9d2-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb9d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb9d2-133">CommonParameters</span></span>
<span data-ttu-id="eb9d2-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb9d2-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb9d2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb9d2-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb9d2-136">INPUTS</span></span>

## <span data-ttu-id="eb9d2-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb9d2-137">OUTPUTS</span></span>

## <span data-ttu-id="eb9d2-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb9d2-138">NOTES</span></span>

## <span data-ttu-id="eb9d2-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb9d2-139">RELATED LINKS</span></span>

[<span data-ttu-id="eb9d2-140">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb9d2-140">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="eb9d2-141">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="eb9d2-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="eb9d2-142">Nowe — AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb9d2-142">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="eb9d2-143">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb9d2-143">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
