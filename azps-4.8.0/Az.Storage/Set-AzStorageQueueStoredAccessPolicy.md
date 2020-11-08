---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 0f8d9860f04112c197b91907a7622683069c3589
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219727"
---
# <span data-ttu-id="6ee2b-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ee2b-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="6ee2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ee2b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee2b-103">Ustawia zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="6ee2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ee2b-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ee2b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ee2b-105">DESCRIPTION</span></span>
<span data-ttu-id="6ee2b-106">Polecenie cmdlet **Set-AzStorageQueueStoredAccessPolicy** ustawia zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="6ee2b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ee2b-107">EXAMPLES</span></span>

### <span data-ttu-id="6ee2b-108">Przykład 1: Ustawianie zasad dostępu przechowywanych w kolejce z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="6ee2b-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="6ee2b-109">To polecenie ustawia zasady dostępu o nazwie Policy07 dla kolejki magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="6ee2b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ee2b-110">PARAMETERS</span></span>

### <span data-ttu-id="6ee2b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6ee2b-111">-Context</span></span>
<span data-ttu-id="6ee2b-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6ee2b-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6ee2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee2b-114">-DefaultProfile</span></span>
<span data-ttu-id="6ee2b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ee2b-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6ee2b-116">-ExpiryTime</span></span>
<span data-ttu-id="6ee2b-117">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ee2b-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6ee2b-118">-NoExpiryTime</span></span>
<span data-ttu-id="6ee2b-119">Wskazuje, że zasady dostępu nie mają daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="6ee2b-120">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="6ee2b-120">-NoStartTime</span></span>
<span data-ttu-id="6ee2b-121">Wskazuje, że to polecenie cmdlet ustawia czas rozpoczęcia $Null.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="6ee2b-122">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="6ee2b-122">-Permission</span></span>
<span data-ttu-id="6ee2b-123">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="6ee2b-124">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="6ee2b-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="6ee2b-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="6ee2b-125">-Policy</span></span>
<span data-ttu-id="6ee2b-126">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-126">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ee2b-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="6ee2b-127">-Queue</span></span>
<span data-ttu-id="6ee2b-128">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-128">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee2b-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6ee2b-129">-StartTime</span></span>
<span data-ttu-id="6ee2b-130">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-130">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ee2b-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ee2b-131">-Confirm</span></span>
<span data-ttu-id="6ee2b-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ee2b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ee2b-133">-WhatIf</span></span>
<span data-ttu-id="6ee2b-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ee2b-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ee2b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee2b-136">CommonParameters</span></span>
<span data-ttu-id="6ee2b-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ee2b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee2b-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ee2b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee2b-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ee2b-139">INPUTS</span></span>

### <span data-ttu-id="6ee2b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6ee2b-140">System.String</span></span>

### <span data-ttu-id="6ee2b-141">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6ee2b-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6ee2b-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ee2b-142">OUTPUTS</span></span>

### <span data-ttu-id="6ee2b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6ee2b-143">System.String</span></span>

## <span data-ttu-id="6ee2b-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ee2b-144">NOTES</span></span>

## <span data-ttu-id="6ee2b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ee2b-145">RELATED LINKS</span></span>

[<span data-ttu-id="6ee2b-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ee2b-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6ee2b-147">Nowe — AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ee2b-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6ee2b-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ee2b-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
