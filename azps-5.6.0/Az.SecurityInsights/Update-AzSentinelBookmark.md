---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: eccb0ce5a9a92eae956c11273bf6397f20473e39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953002"
---
# <span data-ttu-id="a4fdf-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="a4fdf-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="a4fdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="a4fdf-103">Aktualizowanie zakładki.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-103">Update a Bookmark.</span></span>

## <span data-ttu-id="a4fdf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a4fdf-104">SYNTAX</span></span>

### <span data-ttu-id="a4fdf-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-105">BookmarkId.</span></span> <span data-ttu-id="a4fdf-106">(Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a4fdf-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4fdf-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a4fdf-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4fdf-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4fdf-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4fdf-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a4fdf-109">DESCRIPTION</span></span>
<span data-ttu-id="a4fdf-110">Polecenie **cmdlet Update-AzSentinelBookmark** aktualizuje zakładkę w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="a4fdf-111">Obiekt Bookmark można **przekazać** jako parametr lub za pomocą operatora potoku, a także określić wymagane parametry *bookmarkId.*</span><span class="sxs-lookup"><span data-stu-id="a4fdf-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="a4fdf-112">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="a4fdf-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a4fdf-113">EXAMPLES</span></span>

### <span data-ttu-id="a4fdf-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4fdf-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="a4fdf-115">Polecenie aktualizuje zakładkę, ustawiając właściwość *Notatki.*</span><span class="sxs-lookup"><span data-stu-id="a4fdf-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="a4fdf-116">Wszystkie pozostałe proprety pozostają takie same.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="a4fdf-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a4fdf-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="a4fdf-118">Pierwsze polecenie pobiera pole Zakładka według *wartości BookmarkId* z określonego obszaru roboczego, a następnie zapisuje je w $Bookmark obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="a4fdf-119">Drugie polecenie aktualizuje właściwość Notatki.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="a4fdf-120">Wszystkie pozostałe proprety pozostają takie same.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="a4fdf-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4fdf-121">PARAMETERS</span></span>

### <span data-ttu-id="a4fdf-122">- BookmarkId</span><span class="sxs-lookup"><span data-stu-id="a4fdf-122">-BookmarkId</span></span>
<span data-ttu-id="a4fdf-123">Identyfikator zakładki</span><span class="sxs-lookup"><span data-stu-id="a4fdf-123">Bookmark Id,</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId., ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fdf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4fdf-124">-DefaultProfile</span></span>
<span data-ttu-id="a4fdf-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fdf-126">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="a4fdf-126">-DisplayName</span></span>
<span data-ttu-id="a4fdf-127">Nazwa wyświetlana reguły zakładki.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-127">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="a4fdf-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="a4fdf-128">-IncidentInfo</span></span>
<span data-ttu-id="a4fdf-129">Informacje o zdarzeniu zakładki.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-129">Bookmark Incident Info.</span></span>

```yaml
Type: PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fdf-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4fdf-130">-InputObject</span></span>
<span data-ttu-id="a4fdf-131">InputObject.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-131">InputObject.</span></span>

```yaml
Type: PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fdf-132">— Label</span><span class="sxs-lookup"><span data-stu-id="a4fdf-132">-Label</span></span>
<span data-ttu-id="a4fdf-133">Etykiety zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-133">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fdf-134">— Notatki</span><span class="sxs-lookup"><span data-stu-id="a4fdf-134">-Notes</span></span>
<span data-ttu-id="a4fdf-135">Notatki zakładek.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-135">Bookmark Notes.</span></span>

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

### <span data-ttu-id="a4fdf-136">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="a4fdf-136">-Query</span></span>
<span data-ttu-id="a4fdf-137">Zapytanie zakładki.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-137">Bookmark Query.</span></span>

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

### <span data-ttu-id="a4fdf-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="a4fdf-138">-QueryResult</span></span>
<span data-ttu-id="a4fdf-139">Wynik zapytania zakładki.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-139">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="a4fdf-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4fdf-140">-ResourceGroupName</span></span>
<span data-ttu-id="a4fdf-141">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-141">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fdf-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4fdf-142">-ResourceId</span></span>
<span data-ttu-id="a4fdf-143">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-143">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fdf-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a4fdf-144">-WorkspaceName</span></span>
<span data-ttu-id="a4fdf-145">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-145">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fdf-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4fdf-146">-Confirm</span></span>
<span data-ttu-id="a4fdf-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4fdf-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4fdf-148">-WhatIf</span></span>
<span data-ttu-id="a4fdf-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4fdf-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4fdf-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4fdf-151">CommonParameters</span></span>
<span data-ttu-id="a4fdf-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4fdf-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4fdf-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4fdf-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4fdf-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4fdf-154">INPUTS</span></span>

### <span data-ttu-id="a4fdf-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="a4fdf-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="a4fdf-156">System.String</span><span class="sxs-lookup"><span data-stu-id="a4fdf-156">System.String</span></span>

### <span data-ttu-id="a4fdf-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="a4fdf-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="a4fdf-158">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4fdf-158">OUTPUTS</span></span>

### <span data-ttu-id="a4fdf-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="a4fdf-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="a4fdf-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a4fdf-160">NOTES</span></span>

## <span data-ttu-id="a4fdf-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4fdf-161">RELATED LINKS</span></span>
