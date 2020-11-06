---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
ms.openlocfilehash: b273dbec3fda421574c8866a10eda0a8098513ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524130"
---
# <span data-ttu-id="1ed5f-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ed5f-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="1ed5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ed5f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed5f-103">Ustawia zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="1ed5f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ed5f-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ed5f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ed5f-105">DESCRIPTION</span></span>
<span data-ttu-id="1ed5f-106">Polecenie cmdlet **Set-AzureStorageQueueStoredAccessPolicy** ustawia zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="1ed5f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ed5f-107">EXAMPLES</span></span>

### <span data-ttu-id="1ed5f-108">Przykład 1: Ustawianie zasad dostępu przechowywanych w kolejce</span><span class="sxs-lookup"><span data-stu-id="1ed5f-108">Example 1: Set a stored access policy in the queue</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07"
```

<span data-ttu-id="1ed5f-109">To polecenie ustawia zasady dostępu o nazwie Policy07 dla kolejki magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="1ed5f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ed5f-110">PARAMETERS</span></span>

### <span data-ttu-id="1ed5f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1ed5f-111">-Context</span></span>
<span data-ttu-id="1ed5f-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1ed5f-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1ed5f-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1ed5f-114">-ExpiryTime</span></span>
<span data-ttu-id="1ed5f-115">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="1ed5f-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1ed5f-116">-NoExpiryTime</span></span>
<span data-ttu-id="1ed5f-117">Wskazuje, że zasady dostępu nie mają daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="1ed5f-118">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="1ed5f-118">-NoStartTime</span></span>
<span data-ttu-id="1ed5f-119">Wskazuje, że to polecenie cmdlet ustawia czas rozpoczęcia $Null.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="1ed5f-120">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="1ed5f-120">-Permission</span></span>
<span data-ttu-id="1ed5f-121">Określa poziom dostępu publicznego do tej kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-121">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="1ed5f-122">-Policy</span><span class="sxs-lookup"><span data-stu-id="1ed5f-122">-Policy</span></span>
<span data-ttu-id="1ed5f-123">Określa zapisane zasady dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="1ed5f-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="1ed5f-124">-Queue</span></span>
<span data-ttu-id="1ed5f-125">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="1ed5f-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1ed5f-126">-StartTime</span></span>
<span data-ttu-id="1ed5f-127">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="1ed5f-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ed5f-128">-Confirm</span></span>
<span data-ttu-id="1ed5f-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ed5f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ed5f-130">-WhatIf</span></span>
<span data-ttu-id="1ed5f-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ed5f-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ed5f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed5f-133">CommonParameters</span></span>
<span data-ttu-id="1ed5f-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed5f-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed5f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed5f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ed5f-136">INPUTS</span></span>

## <span data-ttu-id="1ed5f-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ed5f-137">OUTPUTS</span></span>

## <span data-ttu-id="1ed5f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ed5f-138">NOTES</span></span>

## <span data-ttu-id="1ed5f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ed5f-139">RELATED LINKS</span></span>

[<span data-ttu-id="1ed5f-140">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ed5f-140">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1ed5f-141">Nowe — AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ed5f-141">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1ed5f-142">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ed5f-142">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
