---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 69ec2307dfdf8525f892720281079c58c1e1bd55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552495"
---
# <span data-ttu-id="ca536-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca536-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ca536-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca536-102">SYNOPSIS</span></span>
<span data-ttu-id="ca536-103">Ustawia zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ca536-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca536-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca536-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca536-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ca536-105">DESCRIPTION</span></span>
<span data-ttu-id="ca536-106">Polecenie cmdlet **Set-AzureStorageQueueStoredAccessPolicy** ustawia zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ca536-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="ca536-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca536-107">EXAMPLES</span></span>

### <span data-ttu-id="ca536-108">Przykład 1: Ustawianie zasad dostępu przechowywanych w kolejce z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="ca536-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="ca536-109">To polecenie ustawia zasady dostępu o nazwie Policy07 dla kolejki magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="ca536-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="ca536-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca536-110">PARAMETERS</span></span>

### <span data-ttu-id="ca536-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ca536-111">-Context</span></span>
<span data-ttu-id="ca536-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ca536-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ca536-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ca536-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ca536-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ca536-114">-ExpiryTime</span></span>
<span data-ttu-id="ca536-115">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="ca536-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="ca536-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ca536-116">-NoExpiryTime</span></span>
<span data-ttu-id="ca536-117">Wskazuje, że zasady dostępu nie mają daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="ca536-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="ca536-118">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="ca536-118">-NoStartTime</span></span>
<span data-ttu-id="ca536-119">Wskazuje, że to polecenie cmdlet ustawia czas rozpoczęcia $Null.</span><span class="sxs-lookup"><span data-stu-id="ca536-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="ca536-120">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="ca536-120">-Permission</span></span>
<span data-ttu-id="ca536-121">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="ca536-121">Specifies permissions in the stored access policy to access the storage queue.</span></span>

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

### <span data-ttu-id="ca536-122">-Policy</span><span class="sxs-lookup"><span data-stu-id="ca536-122">-Policy</span></span>
<span data-ttu-id="ca536-123">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="ca536-123">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="ca536-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="ca536-124">-Queue</span></span>
<span data-ttu-id="ca536-125">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ca536-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="ca536-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ca536-126">-StartTime</span></span>
<span data-ttu-id="ca536-127">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="ca536-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="ca536-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca536-128">-Confirm</span></span>
<span data-ttu-id="ca536-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca536-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca536-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca536-130">-WhatIf</span></span>
<span data-ttu-id="ca536-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca536-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca536-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca536-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca536-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca536-133">CommonParameters</span></span>
<span data-ttu-id="ca536-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca536-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca536-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca536-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca536-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca536-136">INPUTS</span></span>

### <span data-ttu-id="ca536-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca536-137">IStorageContext</span></span>

<span data-ttu-id="ca536-138">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="ca536-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="ca536-139">Ciąg</span><span class="sxs-lookup"><span data-stu-id="ca536-139">String</span></span>

<span data-ttu-id="ca536-140">Parametr "queue" przyjmuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="ca536-140">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ca536-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca536-141">OUTPUTS</span></span>

### <span data-ttu-id="ca536-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ca536-142">System.String</span></span>

## <span data-ttu-id="ca536-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca536-143">NOTES</span></span>

## <span data-ttu-id="ca536-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca536-144">RELATED LINKS</span></span>

[<span data-ttu-id="ca536-145">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca536-145">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ca536-146">Nowe — AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca536-146">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ca536-147">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca536-147">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)