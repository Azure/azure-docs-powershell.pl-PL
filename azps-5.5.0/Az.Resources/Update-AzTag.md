---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: 3423331e36fd9fbd636a1ae877275badd5912324
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178682"
---
# <span data-ttu-id="98485-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="98485-101">Update-AzTag</span></span>

## <span data-ttu-id="98485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98485-102">SYNOPSIS</span></span>

<span data-ttu-id="98485-103">Selektywnie aktualizuje zestaw tagów dla zasobu lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="98485-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="98485-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="98485-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOperation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="98485-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="98485-105">DESCRIPTION</span></span>

<span data-ttu-id="98485-106">Polecenie **cmdlet Update-AzTag** z idZasób selektywnie aktualizuje zestaw tagów dla zasobu lub subskrypcji. </span><span class="sxs-lookup"><span data-stu-id="98485-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="98485-107">Ta operacja umożliwia zastępowanie, scalanie lub selektywne usuwanie tagów dla określonego zasobu lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="98485-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="98485-108">Pod koniec operacji określona jednostka może mieć maksymalnie 50 tagów.</span><span class="sxs-lookup"><span data-stu-id="98485-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="98485-109">Opcja "zamień" zastępuje cały zestaw istniejących tagów nowym zestawem.</span><span class="sxs-lookup"><span data-stu-id="98485-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="98485-110">Opcja scalania umożliwia dodawanie tagów z nowymi nazwami i aktualizowanie wartości tagów przy użyciu istniejących nazw.</span><span class="sxs-lookup"><span data-stu-id="98485-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="98485-111">Opcja "usuń" umożliwia selektywne usuwanie tagów na podstawie podanych nazw lub par nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="98485-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="98485-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="98485-112">EXAMPLES</span></span>

### <span data-ttu-id="98485-113">Przykład 1. Selektywne aktualizacje zestawu tagów w subskrypcji przy użyciu operacji scalania</span><span class="sxs-lookup"><span data-stu-id="98485-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

<span data-ttu-id="98485-114">To polecenie scala zestaw tagów subskrypcji z {subId}.</span><span class="sxs-lookup"><span data-stu-id="98485-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="98485-115">Przykład 2. Selektywne aktualizacje zestawu tagów w subskrypcji za pomocą operacji "Zamień"</span><span class="sxs-lookup"><span data-stu-id="98485-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

<span data-ttu-id="98485-116">To polecenie ponowniepala zestaw tagów w subskrypcji za pomocą {subId}.</span><span class="sxs-lookup"><span data-stu-id="98485-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="98485-117">Przykład 3. Selektywne aktualizacje zestawu tagów w subskrypcji przy użyciu operacji "Usuń"</span><span class="sxs-lookup"><span data-stu-id="98485-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

<span data-ttu-id="98485-118">To polecenie usuwa zestaw tagów subskrypcji z {subId}.</span><span class="sxs-lookup"><span data-stu-id="98485-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="98485-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98485-119">PARAMETERS</span></span>

### <span data-ttu-id="98485-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98485-120">-DefaultProfile</span></span>
<span data-ttu-id="98485-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="98485-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98485-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98485-122">-ResourceId</span></span>
<span data-ttu-id="98485-123">Identyfikator zasobu dla otagowanego elementu.</span><span class="sxs-lookup"><span data-stu-id="98485-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="98485-124">Może zostać otagowany zasób, grupa zasobów lub subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="98485-124">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98485-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="98485-125">-Tag</span></span>
<span data-ttu-id="98485-126">Zestaw tagów do użycia w celu aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="98485-126">The set of tags to use for update.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98485-127">— Operacja</span><span class="sxs-lookup"><span data-stu-id="98485-127">-Operation</span></span>
<span data-ttu-id="98485-128">Operacja aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="98485-128">The update operation.</span></span> <span data-ttu-id="98485-129">Opcje to Scal, Zamień i Usuń.</span><span class="sxs-lookup"><span data-stu-id="98485-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOperation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98485-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98485-130">-Confirm</span></span>
<span data-ttu-id="98485-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="98485-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98485-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98485-132">-WhatIf</span></span>
<span data-ttu-id="98485-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98485-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98485-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="98485-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98485-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98485-135">CommonParameters</span></span>
<span data-ttu-id="98485-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98485-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98485-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98485-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98485-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98485-138">INPUTS</span></span>

### <span data-ttu-id="98485-139">System.String</span><span class="sxs-lookup"><span data-stu-id="98485-139">System.String</span></span>

### <span data-ttu-id="98485-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span><span class="sxs-lookup"><span data-stu-id="98485-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span></span>

### <span data-ttu-id="98485-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="98485-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="98485-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98485-142">OUTPUTS</span></span>

### <span data-ttu-id="98485-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="98485-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="98485-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="98485-144">NOTES</span></span>

## <span data-ttu-id="98485-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98485-145">RELATED LINKS</span></span>

[<span data-ttu-id="98485-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="98485-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="98485-147">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="98485-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="98485-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="98485-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
