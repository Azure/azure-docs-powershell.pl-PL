---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: e2e88cc676fddd6da7ce460fbe0d9d770756c4c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974145"
---
# <span data-ttu-id="9a4d8-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9a4d8-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="9a4d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a4d8-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4d8-103">Ustawia zasady dostępu przechowywanego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="9a4d8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9a4d8-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a4d8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9a4d8-105">DESCRIPTION</span></span>
<span data-ttu-id="9a4d8-106">Polecenie **cmdlet Set-AzStorageQueueStoredAccessPolicy** ustawia zasady dostępu przechowywanego dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="9a4d8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9a4d8-107">EXAMPLES</span></span>

### <span data-ttu-id="9a4d8-108">Przykład 1. Ustawianie przechowywanych zasad dostępu w kolejce z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="9a4d8-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="9a4d8-109">To polecenie ustawia zasady dostępu o nazwie Zasady07 dla kolejki magazynu o nazwie Moje kolejkowanie.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="9a4d8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a4d8-110">PARAMETERS</span></span>

### <span data-ttu-id="9a4d8-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="9a4d8-111">-Context</span></span>
<span data-ttu-id="9a4d8-112">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9a4d8-113">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9a4d8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4d8-114">-DefaultProfile</span></span>
<span data-ttu-id="9a4d8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a4d8-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9a4d8-116">-ExpiryTime</span></span>
<span data-ttu-id="9a4d8-117">Określa czas, w którym przechowywane zasady dostępu stają się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="9a4d8-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9a4d8-118">-NoExpiryTime</span></span>
<span data-ttu-id="9a4d8-119">Oznacza, że zasady dostępu nie mają daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="9a4d8-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="9a4d8-120">-NoStartTime</span></span>
<span data-ttu-id="9a4d8-121">Wskazuje, że to polecenie cmdlet ustawia czas rozpoczęcia na $Null.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="9a4d8-122">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="9a4d8-122">-Permission</span></span>
<span data-ttu-id="9a4d8-123">Określa uprawnienia w zasadach dostępu przechowywanego do uzyskiwania dostępu do kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="9a4d8-124">Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).</span><span class="sxs-lookup"><span data-stu-id="9a4d8-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="9a4d8-125">— Zasady</span><span class="sxs-lookup"><span data-stu-id="9a4d8-125">-Policy</span></span>
<span data-ttu-id="9a4d8-126">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="9a4d8-127">— Kolejka</span><span class="sxs-lookup"><span data-stu-id="9a4d8-127">-Queue</span></span>
<span data-ttu-id="9a4d8-128">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="9a4d8-129">— StartTime</span><span class="sxs-lookup"><span data-stu-id="9a4d8-129">-StartTime</span></span>
<span data-ttu-id="9a4d8-130">Określa czas, w którym przechowywane zasady dostępu stają się prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="9a4d8-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a4d8-131">-Confirm</span></span>
<span data-ttu-id="9a4d8-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a4d8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a4d8-133">-WhatIf</span></span>
<span data-ttu-id="9a4d8-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a4d8-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a4d8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4d8-136">CommonParameters</span></span>
<span data-ttu-id="9a4d8-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a4d8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4d8-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a4d8-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4d8-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a4d8-139">INPUTS</span></span>

### <span data-ttu-id="9a4d8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9a4d8-140">System.String</span></span>

### <span data-ttu-id="9a4d8-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9a4d8-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9a4d8-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a4d8-142">OUTPUTS</span></span>

### <span data-ttu-id="9a4d8-143">System.String</span><span class="sxs-lookup"><span data-stu-id="9a4d8-143">System.String</span></span>

## <span data-ttu-id="9a4d8-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9a4d8-144">NOTES</span></span>

## <span data-ttu-id="9a4d8-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a4d8-145">RELATED LINKS</span></span>

[<span data-ttu-id="9a4d8-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9a4d8-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9a4d8-147">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9a4d8-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9a4d8-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9a4d8-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
