---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 5093f924f87f146550b13e3858f9a93b3f193ca0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005658"
---
# <span data-ttu-id="7a55f-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="7a55f-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="7a55f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a55f-102">SYNOPSIS</span></span>
<span data-ttu-id="7a55f-103">Pobierz zakładkę.</span><span class="sxs-lookup"><span data-stu-id="7a55f-103">Get a Bookmark.</span></span>

## <span data-ttu-id="7a55f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7a55f-104">SYNTAX</span></span>

### <span data-ttu-id="7a55f-105">WorkspaceScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7a55f-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a55f-106">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="7a55f-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a55f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a55f-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a55f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7a55f-108">DESCRIPTION</span></span>
<span data-ttu-id="7a55f-109">Polecenie **cmdlet Get-AzSentinelBookmark** pobiera zakładkę z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7a55f-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="7a55f-110">W przypadku określenia *parametru BookmarkId* jest zwracany pojedynczy obiekt **Bookmark.**</span><span class="sxs-lookup"><span data-stu-id="7a55f-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="7a55f-111">Jeśli parametr *BookmarkId* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie zakładki w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="7a55f-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="7a55f-112">Za pomocą obiektu **Zakładka** można zaktualizować zakładkę, na przykład można dodać **zakładkę Notatki.**</span><span class="sxs-lookup"><span data-stu-id="7a55f-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="7a55f-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7a55f-113">EXAMPLES</span></span>

### <span data-ttu-id="7a55f-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7a55f-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="7a55f-115">W tym przykładzie wszystkie **zakładki są przechowywane** w określonym obszarze roboczym i przechowywane w $Bookmarks danych.</span><span class="sxs-lookup"><span data-stu-id="7a55f-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="7a55f-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7a55f-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="7a55f-117">Ten przykład pobiera **zakładkę** w określonym obszarze roboczym, a następnie zapisuje ją w $Bookmark danych.</span><span class="sxs-lookup"><span data-stu-id="7a55f-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="7a55f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a55f-118">PARAMETERS</span></span>

### <span data-ttu-id="7a55f-119">- BookmarkId</span><span class="sxs-lookup"><span data-stu-id="7a55f-119">-BookmarkId</span></span>
<span data-ttu-id="7a55f-120">Identyfikator zakładki</span><span class="sxs-lookup"><span data-stu-id="7a55f-120">Bookmark Id,</span></span>

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

### <span data-ttu-id="7a55f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a55f-121">-DefaultProfile</span></span>
<span data-ttu-id="7a55f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a55f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a55f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a55f-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a55f-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a55f-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a55f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a55f-125">-ResourceId</span></span>
<span data-ttu-id="7a55f-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="7a55f-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a55f-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7a55f-127">-WorkspaceName</span></span>
<span data-ttu-id="7a55f-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7a55f-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a55f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a55f-129">CommonParameters</span></span>
<span data-ttu-id="7a55f-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a55f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a55f-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a55f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a55f-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a55f-132">INPUTS</span></span>

### <span data-ttu-id="7a55f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7a55f-133">System.String</span></span>
## <span data-ttu-id="7a55f-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a55f-134">OUTPUTS</span></span>

### <span data-ttu-id="7a55f-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="7a55f-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="7a55f-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7a55f-136">NOTES</span></span>

## <span data-ttu-id="7a55f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a55f-137">RELATED LINKS</span></span>
