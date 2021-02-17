---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: 544c019fd52c0cb5723cbeafb5a82df072ac284e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191210"
---
# <span data-ttu-id="6c0e2-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="6c0e2-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="6c0e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c0e2-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0e2-103">Usuwanie zakładki.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="6c0e2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6c0e2-104">SYNTAX</span></span>

### <span data-ttu-id="6c0e2-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-105">BookmarkId.</span></span> <span data-ttu-id="6c0e2-106">(Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6c0e2-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c0e2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6c0e2-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c0e2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6c0e2-108">DESCRIPTION</span></span>
<span data-ttu-id="6c0e2-109">Polecenie **cmdlet Remove-AzSentinelBookmark** trwale usuwa zakładkę z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="6c0e2-110">Obiekt zakładki **można przekazać** za pomocą operatora potoku lub ewentualnie określić wymagane parametry.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="6c0e2-111">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="6c0e2-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6c0e2-112">EXAMPLES</span></span>

### <span data-ttu-id="6c0e2-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c0e2-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="6c0e2-114">To polecenie usuwa zakładkę z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="6c0e2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c0e2-115">PARAMETERS</span></span>

### <span data-ttu-id="6c0e2-116">- BookmarkId</span><span class="sxs-lookup"><span data-stu-id="6c0e2-116">-BookmarkId</span></span>
<span data-ttu-id="6c0e2-117">Identyfikator zakładki</span><span class="sxs-lookup"><span data-stu-id="6c0e2-117">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c0e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c0e2-118">-DefaultProfile</span></span>
<span data-ttu-id="6c0e2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c0e2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c0e2-120">-InputObject</span></span>
<span data-ttu-id="6c0e2-121">InputObject.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-121">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c0e2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c0e2-122">-PassThru</span></span>
<span data-ttu-id="6c0e2-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="6c0e2-123">PassThru</span></span>

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

### <span data-ttu-id="6c0e2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c0e2-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c0e2-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c0e2-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6c0e2-126">-WorkspaceName</span></span>
<span data-ttu-id="6c0e2-127">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-127">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c0e2-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c0e2-128">-Confirm</span></span>
<span data-ttu-id="6c0e2-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c0e2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c0e2-130">-WhatIf</span></span>
<span data-ttu-id="6c0e2-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c0e2-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c0e2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0e2-133">CommonParameters</span></span>
<span data-ttu-id="6c0e2-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c0e2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0e2-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c0e2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0e2-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c0e2-136">INPUTS</span></span>

### <span data-ttu-id="6c0e2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6c0e2-137">System.String</span></span>
### <span data-ttu-id="6c0e2-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="6c0e2-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="6c0e2-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c0e2-139">OUTPUTS</span></span>

### <span data-ttu-id="6c0e2-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="6c0e2-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="6c0e2-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6c0e2-141">NOTES</span></span>

## <span data-ttu-id="6c0e2-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c0e2-142">RELATED LINKS</span></span>
