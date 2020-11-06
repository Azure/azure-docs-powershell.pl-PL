---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: e20caedc23dcd4d06336f3dddf80fdaf4a84cbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547751"
---
# <span data-ttu-id="a42a4-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a42a4-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="a42a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a42a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a42a4-103">Ustawia zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a42a4-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a42a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a42a4-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a42a4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a42a4-105">DESCRIPTION</span></span>
<span data-ttu-id="a42a4-106">Polecenie cmdlet **Set-AzureStorageQueueStoredAccessPolicy** ustawia zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a42a4-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="a42a4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a42a4-107">EXAMPLES</span></span>

### <span data-ttu-id="a42a4-108">Przykład 1: Ustawianie zasad dostępu przechowywanych w kolejce z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="a42a4-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="a42a4-109">To polecenie ustawia zasady dostępu o nazwie Policy07 dla kolejki magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="a42a4-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="a42a4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a42a4-110">PARAMETERS</span></span>

### <span data-ttu-id="a42a4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a42a4-111">-Context</span></span>
<span data-ttu-id="a42a4-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a42a4-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a42a4-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a42a4-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a42a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a42a4-114">-DefaultProfile</span></span>
<span data-ttu-id="a42a4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a42a4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a42a4-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a42a4-116">-ExpiryTime</span></span>
<span data-ttu-id="a42a4-117">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="a42a4-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="a42a4-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a42a4-118">-NoExpiryTime</span></span>
<span data-ttu-id="a42a4-119">Wskazuje, że zasady dostępu nie mają daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="a42a4-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="a42a4-120">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="a42a4-120">-NoStartTime</span></span>
<span data-ttu-id="a42a4-121">Wskazuje, że to polecenie cmdlet ustawia czas rozpoczęcia $Null.</span><span class="sxs-lookup"><span data-stu-id="a42a4-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="a42a4-122">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="a42a4-122">-Permission</span></span>
<span data-ttu-id="a42a4-123">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="a42a4-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="a42a4-124">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="a42a4-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="a42a4-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="a42a4-125">-Policy</span></span>
<span data-ttu-id="a42a4-126">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="a42a4-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="a42a4-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="a42a4-127">-Queue</span></span>
<span data-ttu-id="a42a4-128">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a42a4-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="a42a4-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a42a4-129">-StartTime</span></span>
<span data-ttu-id="a42a4-130">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="a42a4-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="a42a4-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a42a4-131">-Confirm</span></span>
<span data-ttu-id="a42a4-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a42a4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a42a4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a42a4-133">-WhatIf</span></span>
<span data-ttu-id="a42a4-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a42a4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a42a4-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a42a4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a42a4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a42a4-136">CommonParameters</span></span>
<span data-ttu-id="a42a4-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a42a4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a42a4-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a42a4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a42a4-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a42a4-139">INPUTS</span></span>

### <span data-ttu-id="a42a4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a42a4-140">System.String</span></span>

### <span data-ttu-id="a42a4-141">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a42a4-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a42a4-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a42a4-142">OUTPUTS</span></span>

### <span data-ttu-id="a42a4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a42a4-143">System.String</span></span>

## <span data-ttu-id="a42a4-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a42a4-144">NOTES</span></span>

## <span data-ttu-id="a42a4-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a42a4-145">RELATED LINKS</span></span>

[<span data-ttu-id="a42a4-146">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a42a4-146">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a42a4-147">Nowe — AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a42a4-147">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a42a4-148">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a42a4-148">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
