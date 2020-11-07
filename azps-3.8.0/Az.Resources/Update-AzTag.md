---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: b41f7ca642d74a33c239f125d7dfe2ccdbad1b68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894978"
---
# <span data-ttu-id="e8280-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="e8280-101">Update-AzTag</span></span>

## <span data-ttu-id="e8280-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8280-102">SYNOPSIS</span></span>

<span data-ttu-id="e8280-103">Selektywne Aktualizowanie zestawu znaczników zasobu lub abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e8280-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="e8280-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8280-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOpeation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="e8280-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8280-105">DESCRIPTION</span></span>

<span data-ttu-id="e8280-106">Polecenie cmdlet **Update-AzTag** z identyfikatorem **zasobu umożliwia selektywne** Aktualizowanie zestawu tagów w zasobie lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e8280-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="e8280-107">Ta operacja umożliwia zamianę, scalanie lub selektywne usuwanie tagów określonego zasobu lub abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e8280-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="e8280-108">Na końcu operacji określona encja może zawierać maksymalnie 50 tagów.</span><span class="sxs-lookup"><span data-stu-id="e8280-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="e8280-109">Opcja "Zamień" powoduje zastąpienie całego zestawu istniejących znaczników nowym zestawem.</span><span class="sxs-lookup"><span data-stu-id="e8280-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="e8280-110">Opcja "Scal" umożliwia dodawanie tagów przy użyciu nowych nazw i aktualizowanie wartości znaczników przy użyciu istniejących nazw.</span><span class="sxs-lookup"><span data-stu-id="e8280-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="e8280-111">Opcja "Usuń" umożliwia wybiórcze Usuwanie tagów na podstawie podanych nazw lub par nazw/wartości.</span><span class="sxs-lookup"><span data-stu-id="e8280-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="e8280-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8280-112">EXAMPLES</span></span>

### <span data-ttu-id="e8280-113">Przykład 1. selektywne Aktualizowanie zestawu znaczników w subskrypcji za pomocą operacji scalania</span><span class="sxs-lookup"><span data-stu-id="e8280-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

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

<span data-ttu-id="e8280-114">To polecenie Scala zestaw tagów w subskrypcji z aplikacją {subId}.</span><span class="sxs-lookup"><span data-stu-id="e8280-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="e8280-115">Przykład 2: selektywne Aktualizowanie zestawu znaczników w subskrypcji przy użyciu operacji zamieniania</span><span class="sxs-lookup"><span data-stu-id="e8280-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

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

<span data-ttu-id="e8280-116">To polecenie Repalces zestaw tagów w subskrypcji przy użyciu funkcji {subId}.</span><span class="sxs-lookup"><span data-stu-id="e8280-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="e8280-117">Przykład 3: selektywne Aktualizowanie zestawu znaczników w subskrypcji za pomocą operacji usuwania</span><span class="sxs-lookup"><span data-stu-id="e8280-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

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

<span data-ttu-id="e8280-118">To polecenie usuwa zestaw tagów w subskrypcji przy użyciu programu {subId}.</span><span class="sxs-lookup"><span data-stu-id="e8280-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="e8280-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8280-119">PARAMETERS</span></span>

### <span data-ttu-id="e8280-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8280-120">-DefaultProfile</span></span>
<span data-ttu-id="e8280-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8280-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8280-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8280-122">-ResourceId</span></span>
<span data-ttu-id="e8280-123">Identyfikator zasobu oznakowanej jednostki.</span><span class="sxs-lookup"><span data-stu-id="e8280-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="e8280-124">Zasób, Grupa zasobów lub abonament mogą być oznakowane.</span><span class="sxs-lookup"><span data-stu-id="e8280-124">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8280-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8280-125">-Tag</span></span>
<span data-ttu-id="e8280-126">Zestaw tagów, które mają być używane do aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="e8280-126">The set of tags to use for update.</span></span>

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

### <span data-ttu-id="e8280-127">-Operation</span><span class="sxs-lookup"><span data-stu-id="e8280-127">-Operation</span></span>
<span data-ttu-id="e8280-128">Operacja aktualizowania.</span><span class="sxs-lookup"><span data-stu-id="e8280-128">The update operation.</span></span> <span data-ttu-id="e8280-129">Opcje są scalane, zamieniane i usuwane.</span><span class="sxs-lookup"><span data-stu-id="e8280-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8280-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8280-130">-Confirm</span></span>
<span data-ttu-id="e8280-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8280-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8280-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8280-132">-WhatIf</span></span>
<span data-ttu-id="e8280-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8280-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8280-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8280-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8280-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8280-135">CommonParameters</span></span>
<span data-ttu-id="e8280-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8280-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8280-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8280-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8280-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8280-138">INPUTS</span></span>

### <span data-ttu-id="e8280-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e8280-139">System.String</span></span>

### <span data-ttu-id="e8280-140">Microsoft. Azure. Commands. Tags. model. TagPatchOpeation</span><span class="sxs-lookup"><span data-stu-id="e8280-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation</span></span>

### <span data-ttu-id="e8280-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e8280-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e8280-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8280-142">OUTPUTS</span></span>

### <span data-ttu-id="e8280-143">Microsoft. Azure. Commands. Tags. model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="e8280-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="e8280-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8280-144">NOTES</span></span>

## <span data-ttu-id="e8280-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8280-145">RELATED LINKS</span></span>

[<span data-ttu-id="e8280-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="e8280-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="e8280-147">Nowe — AzTag</span><span class="sxs-lookup"><span data-stu-id="e8280-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="e8280-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="e8280-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
