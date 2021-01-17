---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 822781f6c46eeb76a953eaa66935c03cd76df737
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384377"
---
# <span data-ttu-id="40842-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="40842-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="40842-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40842-102">SYNOPSIS</span></span>
<span data-ttu-id="40842-103">Ustawia zasady dostępu przechowywane dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="40842-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="40842-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40842-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40842-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40842-105">DESCRIPTION</span></span>
<span data-ttu-id="40842-106">Polecenie cmdlet **Set-AzStorageTableStoredAccessPolicy** ustawia zasady dostępu przechowywane dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="40842-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="40842-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40842-107">EXAMPLES</span></span>

### <span data-ttu-id="40842-108">Przykład 1: Ustawianie zasad dostępu przechowywanych w tabeli z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="40842-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="40842-109">To polecenie ustawia zasady dostępu o nazwie Policy08 dla tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="40842-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="40842-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40842-110">PARAMETERS</span></span>

### <span data-ttu-id="40842-111">-Context</span><span class="sxs-lookup"><span data-stu-id="40842-111">-Context</span></span>
<span data-ttu-id="40842-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="40842-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="40842-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="40842-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="40842-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40842-114">-DefaultProfile</span></span>
<span data-ttu-id="40842-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40842-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40842-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="40842-116">-ExpiryTime</span></span>
<span data-ttu-id="40842-117">Określa godzinę wygaśnięcia przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="40842-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="40842-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="40842-118">-NoExpiryTime</span></span>
<span data-ttu-id="40842-119">Wskazuje, że zasady dostępu nie mają daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="40842-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="40842-120">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="40842-120">-NoStartTime</span></span>
<span data-ttu-id="40842-121">Wskazuje, że godzina rozpoczęcia jest ustawiona na $Null.</span><span class="sxs-lookup"><span data-stu-id="40842-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="40842-122">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="40842-122">-Permission</span></span>
<span data-ttu-id="40842-123">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do tabeli magazynów.</span><span class="sxs-lookup"><span data-stu-id="40842-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="40842-124">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="40842-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="40842-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="40842-125">-Policy</span></span>
<span data-ttu-id="40842-126">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="40842-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="40842-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="40842-127">-StartTime</span></span>
<span data-ttu-id="40842-128">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="40842-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="40842-129">-Table</span><span class="sxs-lookup"><span data-stu-id="40842-129">-Table</span></span>
<span data-ttu-id="40842-130">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="40842-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="40842-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40842-131">-Confirm</span></span>
<span data-ttu-id="40842-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40842-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40842-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40842-133">-WhatIf</span></span>
<span data-ttu-id="40842-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40842-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40842-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="40842-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40842-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40842-136">CommonParameters</span></span>
<span data-ttu-id="40842-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40842-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40842-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40842-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40842-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40842-139">INPUTS</span></span>

### <span data-ttu-id="40842-140">System. String</span><span class="sxs-lookup"><span data-stu-id="40842-140">System.String</span></span>

### <span data-ttu-id="40842-141">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="40842-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="40842-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40842-142">OUTPUTS</span></span>

### <span data-ttu-id="40842-143">System. String</span><span class="sxs-lookup"><span data-stu-id="40842-143">System.String</span></span>

## <span data-ttu-id="40842-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40842-144">NOTES</span></span>

## <span data-ttu-id="40842-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40842-145">RELATED LINKS</span></span>

[<span data-ttu-id="40842-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="40842-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="40842-147">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="40842-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="40842-148">Nowe — AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="40842-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="40842-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="40842-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
