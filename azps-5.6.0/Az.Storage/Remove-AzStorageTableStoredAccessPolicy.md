---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 7674b21e72d375665662272cb2ac1a585d266324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961217"
---
# <span data-ttu-id="6ed05-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ed05-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="6ed05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ed05-102">SYNOPSIS</span></span>
<span data-ttu-id="6ed05-103">Usuwa przechowywane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ed05-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="6ed05-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6ed05-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ed05-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6ed05-105">DESCRIPTION</span></span>
<span data-ttu-id="6ed05-106">Polecenie **cmdlet Remove-AzStorageTableStoredAccessPolicy** usuwa przechowywane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ed05-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="6ed05-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6ed05-107">EXAMPLES</span></span>

### <span data-ttu-id="6ed05-108">Przykład 1. Usuwanie przechowywanych zasad dostępu z tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="6ed05-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="6ed05-109">To polecenie usuwa zasady o nazwie Zasady05 z tabeli magazynu o nazwie Moja tabela.</span><span class="sxs-lookup"><span data-stu-id="6ed05-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="6ed05-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ed05-110">PARAMETERS</span></span>

### <span data-ttu-id="6ed05-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="6ed05-111">-Context</span></span>
<span data-ttu-id="6ed05-112">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ed05-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6ed05-113">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ed05-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6ed05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ed05-114">-DefaultProfile</span></span>
<span data-ttu-id="6ed05-115">komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ed05-115">communication with Azure.</span></span>

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

### <span data-ttu-id="6ed05-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ed05-116">-PassThru</span></span>
<span data-ttu-id="6ed05-117">Wskazuje, że to polecenie cmdlet zwraca **wartość** logiczną, która odzwierciedla sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="6ed05-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="6ed05-118">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="6ed05-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6ed05-119">— Zasady</span><span class="sxs-lookup"><span data-stu-id="6ed05-119">-Policy</span></span>
<span data-ttu-id="6ed05-120">Określa nazwę przechowywanych zasad dostępu usuwanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ed05-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ed05-121">— Tabela</span><span class="sxs-lookup"><span data-stu-id="6ed05-121">-Table</span></span>
<span data-ttu-id="6ed05-122">Określa nazwę tabeli platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ed05-122">Specifies the Azure table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ed05-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ed05-123">-Confirm</span></span>
<span data-ttu-id="6ed05-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6ed05-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ed05-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ed05-125">-WhatIf</span></span>
<span data-ttu-id="6ed05-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ed05-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ed05-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6ed05-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ed05-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ed05-128">CommonParameters</span></span>
<span data-ttu-id="6ed05-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ed05-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ed05-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ed05-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ed05-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ed05-131">INPUTS</span></span>

### <span data-ttu-id="6ed05-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6ed05-132">System.String</span></span>

### <span data-ttu-id="6ed05-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6ed05-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6ed05-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ed05-134">OUTPUTS</span></span>

### <span data-ttu-id="6ed05-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6ed05-135">System.Boolean</span></span>

## <span data-ttu-id="6ed05-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6ed05-136">NOTES</span></span>

## <span data-ttu-id="6ed05-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ed05-137">RELATED LINKS</span></span>

[<span data-ttu-id="6ed05-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ed05-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="6ed05-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6ed05-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="6ed05-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ed05-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="6ed05-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ed05-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
