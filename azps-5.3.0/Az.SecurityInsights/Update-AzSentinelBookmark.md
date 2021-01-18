---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: ebc0ffd78f653276e66b85d263db41803a48c356
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502951"
---
# <span data-ttu-id="bc259-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="bc259-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="bc259-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc259-102">SYNOPSIS</span></span>
<span data-ttu-id="bc259-103">Aktualizowanie zakładki.</span><span class="sxs-lookup"><span data-stu-id="bc259-103">Update a Bookmark.</span></span>

## <span data-ttu-id="bc259-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc259-104">SYNTAX</span></span>

### <span data-ttu-id="bc259-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="bc259-105">BookmarkId.</span></span> <span data-ttu-id="bc259-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="bc259-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc259-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="bc259-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc259-108">Zasobów</span><span class="sxs-lookup"><span data-stu-id="bc259-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc259-109">Opis</span><span class="sxs-lookup"><span data-stu-id="bc259-109">DESCRIPTION</span></span>
<span data-ttu-id="bc259-110">Polecenie cmdlet **Update-AzSentinelBookmark** umożliwia zaktualizowanie zakładki w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="bc259-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="bc259-111">Obiekt **Bookmark** można przekazać jako parametr lub za pomocą operatora potoku albo też określić wymagane parametry *BookmarkId* .</span><span class="sxs-lookup"><span data-stu-id="bc259-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="bc259-112">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bc259-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="bc259-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc259-113">EXAMPLES</span></span>

### <span data-ttu-id="bc259-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bc259-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="bc259-115">Polecenie aktualizuje zakładkę, ustawiając właściwość *notatki* .</span><span class="sxs-lookup"><span data-stu-id="bc259-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="bc259-116">Wszystkie inne propreties pozostają takie same.</span><span class="sxs-lookup"><span data-stu-id="bc259-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="bc259-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bc259-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="bc259-118">Pierwsze polecenie uzyskuje zakładkę według *BookmarkId* z określonego obszaru roboczego, a następnie zapisuje ją w zmiennej $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="bc259-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="bc259-119">Drugie polecenie aktualizuje właściwość notatki.</span><span class="sxs-lookup"><span data-stu-id="bc259-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="bc259-120">Wszystkie inne propreties pozostają takie same.</span><span class="sxs-lookup"><span data-stu-id="bc259-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="bc259-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc259-121">PARAMETERS</span></span>

### <span data-ttu-id="bc259-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="bc259-122">-BookmarkId</span></span>
<span data-ttu-id="bc259-123">Identyfikator zakładki,</span><span class="sxs-lookup"><span data-stu-id="bc259-123">Bookmark Id,</span></span>

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

### <span data-ttu-id="bc259-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc259-124">-DefaultProfile</span></span>
<span data-ttu-id="bc259-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc259-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc259-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bc259-126">-DisplayName</span></span>
<span data-ttu-id="bc259-127">Nazwa wyświetlana reguły zakładki.</span><span class="sxs-lookup"><span data-stu-id="bc259-127">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="bc259-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="bc259-128">-IncidentInfo</span></span>
<span data-ttu-id="bc259-129">Informacje o zdarzeniu zakładki.</span><span class="sxs-lookup"><span data-stu-id="bc259-129">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="bc259-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bc259-130">-InputObject</span></span>
<span data-ttu-id="bc259-131">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="bc259-131">InputObject.</span></span>

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

### <span data-ttu-id="bc259-132">-Label</span><span class="sxs-lookup"><span data-stu-id="bc259-132">-Label</span></span>
<span data-ttu-id="bc259-133">Etykiety zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="bc259-133">Incident Labels.</span></span>

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

### <span data-ttu-id="bc259-134">-Uwagi</span><span class="sxs-lookup"><span data-stu-id="bc259-134">-Notes</span></span>
<span data-ttu-id="bc259-135">Notatki z zakładkami.</span><span class="sxs-lookup"><span data-stu-id="bc259-135">Bookmark Notes.</span></span>

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

### <span data-ttu-id="bc259-136">-Query</span><span class="sxs-lookup"><span data-stu-id="bc259-136">-Query</span></span>
<span data-ttu-id="bc259-137">Kwerenda zakładki.</span><span class="sxs-lookup"><span data-stu-id="bc259-137">Bookmark Query.</span></span>

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

### <span data-ttu-id="bc259-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="bc259-138">-QueryResult</span></span>
<span data-ttu-id="bc259-139">Wynik kwerendy zakładki.</span><span class="sxs-lookup"><span data-stu-id="bc259-139">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="bc259-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc259-140">-ResourceGroupName</span></span>
<span data-ttu-id="bc259-141">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bc259-141">Resource group name.</span></span>

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

### <span data-ttu-id="bc259-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc259-142">-ResourceId</span></span>
<span data-ttu-id="bc259-143">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="bc259-143">Resource Id.</span></span>

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

### <span data-ttu-id="bc259-144">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="bc259-144">-WorkspaceName</span></span>
<span data-ttu-id="bc259-145">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="bc259-145">Workspace Name.</span></span>

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

### <span data-ttu-id="bc259-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc259-146">-Confirm</span></span>
<span data-ttu-id="bc259-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc259-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc259-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc259-148">-WhatIf</span></span>
<span data-ttu-id="bc259-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc259-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc259-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bc259-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc259-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc259-151">CommonParameters</span></span>
<span data-ttu-id="bc259-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc259-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc259-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc259-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc259-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc259-154">INPUTS</span></span>

### <span data-ttu-id="bc259-155">Microsoft. Azure. Commands. SecurityInsights. models. zakładki. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="bc259-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="bc259-156">System. String</span><span class="sxs-lookup"><span data-stu-id="bc259-156">System.String</span></span>

### <span data-ttu-id="bc259-157">Microsoft. Azure. Commands. SecurityInsights. models. zakładki. PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="bc259-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="bc259-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc259-158">OUTPUTS</span></span>

### <span data-ttu-id="bc259-159">Microsoft. Azure. Commands. SecurityInsights. models. zakładki. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="bc259-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="bc259-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc259-160">NOTES</span></span>

## <span data-ttu-id="bc259-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc259-161">RELATED LINKS</span></span>
