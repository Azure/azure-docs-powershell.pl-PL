---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 576b347ad260fc95cdafe7c4a11e42246feb09ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971706"
---
# <span data-ttu-id="895cd-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="895cd-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="895cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="895cd-102">SYNOPSIS</span></span>
<span data-ttu-id="895cd-103">Ustawia zasady przechowywanego dostępu dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="895cd-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="895cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="895cd-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="895cd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="895cd-105">DESCRIPTION</span></span>
<span data-ttu-id="895cd-106">Polecenie **cmdlet Set-AzStorageTableStoredAccessPolicy** ustawia zasady dostępu przechowywanego dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="895cd-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="895cd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="895cd-107">EXAMPLES</span></span>

### <span data-ttu-id="895cd-108">Przykład 1. Ustawianie przechowywanych zasad dostępu w tabeli z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="895cd-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="895cd-109">To polecenie ustawia zasady dostępu o nazwie Zasady08 dla tabeli magazynu o nazwie Moja tabela.</span><span class="sxs-lookup"><span data-stu-id="895cd-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="895cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="895cd-110">PARAMETERS</span></span>

### <span data-ttu-id="895cd-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="895cd-111">-Context</span></span>
<span data-ttu-id="895cd-112">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="895cd-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="895cd-113">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="895cd-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="895cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="895cd-114">-DefaultProfile</span></span>
<span data-ttu-id="895cd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="895cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="895cd-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="895cd-116">-ExpiryTime</span></span>
<span data-ttu-id="895cd-117">Określa czas wygaśnięcia przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="895cd-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="895cd-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="895cd-118">-NoExpiryTime</span></span>
<span data-ttu-id="895cd-119">Oznacza, że zasady dostępu nie mają daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="895cd-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="895cd-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="895cd-120">-NoStartTime</span></span>
<span data-ttu-id="895cd-121">Wskazuje, że godzina rozpoczęcia jest ustawiona na $Null.</span><span class="sxs-lookup"><span data-stu-id="895cd-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="895cd-122">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="895cd-122">-Permission</span></span>
<span data-ttu-id="895cd-123">Określa uprawnienia w przechowywanych zasadach dostępu do uzyskiwania dostępu do tabeli magazynu.</span><span class="sxs-lookup"><span data-stu-id="895cd-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="895cd-124">Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).</span><span class="sxs-lookup"><span data-stu-id="895cd-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="895cd-125">— Zasady</span><span class="sxs-lookup"><span data-stu-id="895cd-125">-Policy</span></span>
<span data-ttu-id="895cd-126">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="895cd-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="895cd-127">— StartTime</span><span class="sxs-lookup"><span data-stu-id="895cd-127">-StartTime</span></span>
<span data-ttu-id="895cd-128">Określa czas, w którym przechowywane zasady dostępu stają się prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="895cd-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="895cd-129">— Tabela</span><span class="sxs-lookup"><span data-stu-id="895cd-129">-Table</span></span>
<span data-ttu-id="895cd-130">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="895cd-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="895cd-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="895cd-131">-Confirm</span></span>
<span data-ttu-id="895cd-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="895cd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="895cd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="895cd-133">-WhatIf</span></span>
<span data-ttu-id="895cd-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="895cd-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="895cd-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="895cd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="895cd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="895cd-136">CommonParameters</span></span>
<span data-ttu-id="895cd-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="895cd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="895cd-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="895cd-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="895cd-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="895cd-139">INPUTS</span></span>

### <span data-ttu-id="895cd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="895cd-140">System.String</span></span>

### <span data-ttu-id="895cd-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="895cd-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="895cd-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="895cd-142">OUTPUTS</span></span>

### <span data-ttu-id="895cd-143">System.String</span><span class="sxs-lookup"><span data-stu-id="895cd-143">System.String</span></span>

## <span data-ttu-id="895cd-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="895cd-144">NOTES</span></span>

## <span data-ttu-id="895cd-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="895cd-145">RELATED LINKS</span></span>

[<span data-ttu-id="895cd-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="895cd-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="895cd-147">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="895cd-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="895cd-148">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="895cd-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="895cd-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="895cd-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
