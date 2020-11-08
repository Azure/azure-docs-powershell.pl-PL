---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 822781f6c46eeb76a953eaa66935c03cd76df737
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050480"
---
# <span data-ttu-id="10570-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="10570-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="10570-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10570-102">SYNOPSIS</span></span>
<span data-ttu-id="10570-103">Ustawia zasady dostępu przechowywane dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="10570-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="10570-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10570-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10570-105">Opis</span><span class="sxs-lookup"><span data-stu-id="10570-105">DESCRIPTION</span></span>
<span data-ttu-id="10570-106">Polecenie cmdlet **Set-AzStorageTableStoredAccessPolicy** ustawia zasady dostępu przechowywane dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="10570-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="10570-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10570-107">EXAMPLES</span></span>

### <span data-ttu-id="10570-108">Przykład 1: Ustawianie zasad dostępu przechowywanych w tabeli z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="10570-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="10570-109">To polecenie ustawia zasady dostępu o nazwie Policy08 dla tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="10570-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="10570-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10570-110">PARAMETERS</span></span>

### <span data-ttu-id="10570-111">-Context</span><span class="sxs-lookup"><span data-stu-id="10570-111">-Context</span></span>
<span data-ttu-id="10570-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="10570-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="10570-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="10570-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="10570-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10570-114">-DefaultProfile</span></span>
<span data-ttu-id="10570-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10570-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10570-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="10570-116">-ExpiryTime</span></span>
<span data-ttu-id="10570-117">Określa godzinę wygaśnięcia przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="10570-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="10570-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="10570-118">-NoExpiryTime</span></span>
<span data-ttu-id="10570-119">Wskazuje, że zasady dostępu nie mają daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="10570-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="10570-120">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="10570-120">-NoStartTime</span></span>
<span data-ttu-id="10570-121">Wskazuje, że godzina rozpoczęcia jest ustawiona na $Null.</span><span class="sxs-lookup"><span data-stu-id="10570-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="10570-122">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="10570-122">-Permission</span></span>
<span data-ttu-id="10570-123">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do tabeli magazynów.</span><span class="sxs-lookup"><span data-stu-id="10570-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="10570-124">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="10570-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="10570-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="10570-125">-Policy</span></span>
<span data-ttu-id="10570-126">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="10570-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="10570-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="10570-127">-StartTime</span></span>
<span data-ttu-id="10570-128">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="10570-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="10570-129">-Table</span><span class="sxs-lookup"><span data-stu-id="10570-129">-Table</span></span>
<span data-ttu-id="10570-130">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="10570-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="10570-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10570-131">-Confirm</span></span>
<span data-ttu-id="10570-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10570-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10570-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10570-133">-WhatIf</span></span>
<span data-ttu-id="10570-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10570-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10570-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="10570-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10570-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10570-136">CommonParameters</span></span>
<span data-ttu-id="10570-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10570-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10570-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10570-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10570-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10570-139">INPUTS</span></span>

### <span data-ttu-id="10570-140">System. String</span><span class="sxs-lookup"><span data-stu-id="10570-140">System.String</span></span>

### <span data-ttu-id="10570-141">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="10570-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="10570-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10570-142">OUTPUTS</span></span>

### <span data-ttu-id="10570-143">System. String</span><span class="sxs-lookup"><span data-stu-id="10570-143">System.String</span></span>

## <span data-ttu-id="10570-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10570-144">NOTES</span></span>

## <span data-ttu-id="10570-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10570-145">RELATED LINKS</span></span>

[<span data-ttu-id="10570-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="10570-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="10570-147">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="10570-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="10570-148">Nowe — AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="10570-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="10570-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="10570-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
