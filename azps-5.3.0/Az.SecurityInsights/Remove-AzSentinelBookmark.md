---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: 544c019fd52c0cb5723cbeafb5a82df072ac284e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502959"
---
# <span data-ttu-id="d4618-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="d4618-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="d4618-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4618-102">SYNOPSIS</span></span>
<span data-ttu-id="d4618-103">Usuwanie zakładki.</span><span class="sxs-lookup"><span data-stu-id="d4618-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="d4618-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4618-104">SYNTAX</span></span>

### <span data-ttu-id="d4618-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="d4618-105">BookmarkId.</span></span> <span data-ttu-id="d4618-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="d4618-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4618-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4618-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4618-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d4618-108">DESCRIPTION</span></span>
<span data-ttu-id="d4618-109">Polecenie cmdlet **Remove-AzSentinelBookmark** powoduje trwałe usunięcie zakładki z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d4618-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="d4618-110">Obiekt **Bookmark** można przekazać przy użyciu operatora potoku lub można też określić parametry wymagane.</span><span class="sxs-lookup"><span data-stu-id="d4618-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="d4618-111">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d4618-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="d4618-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4618-112">EXAMPLES</span></span>

### <span data-ttu-id="d4618-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d4618-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="d4618-114">To polecenie umożliwia usunięcie zakładki z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d4618-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="d4618-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4618-115">PARAMETERS</span></span>

### <span data-ttu-id="d4618-116">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="d4618-116">-BookmarkId</span></span>
<span data-ttu-id="d4618-117">Identyfikator zakładki,</span><span class="sxs-lookup"><span data-stu-id="d4618-117">Bookmark Id,</span></span>

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

### <span data-ttu-id="d4618-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4618-118">-DefaultProfile</span></span>
<span data-ttu-id="d4618-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4618-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4618-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4618-120">-InputObject</span></span>
<span data-ttu-id="d4618-121">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="d4618-121">InputObject.</span></span>

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

### <span data-ttu-id="d4618-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4618-122">-PassThru</span></span>
<span data-ttu-id="d4618-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="d4618-123">PassThru</span></span>

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

### <span data-ttu-id="d4618-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4618-124">-ResourceGroupName</span></span>
<span data-ttu-id="d4618-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4618-125">Resource group name.</span></span>

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

### <span data-ttu-id="d4618-126">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="d4618-126">-WorkspaceName</span></span>
<span data-ttu-id="d4618-127">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d4618-127">Workspace Name.</span></span>

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

### <span data-ttu-id="d4618-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4618-128">-Confirm</span></span>
<span data-ttu-id="d4618-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4618-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4618-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4618-130">-WhatIf</span></span>
<span data-ttu-id="d4618-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4618-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4618-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4618-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4618-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4618-133">CommonParameters</span></span>
<span data-ttu-id="d4618-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4618-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4618-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4618-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4618-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4618-136">INPUTS</span></span>

### <span data-ttu-id="d4618-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d4618-137">System.String</span></span>
### <span data-ttu-id="d4618-138">Microsoft. Azure. Commands. SecurityInsights. models. zakładki. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="d4618-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="d4618-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4618-139">OUTPUTS</span></span>

### <span data-ttu-id="d4618-140">Microsoft. Azure. Commands. SecurityInsights. models. zakładki. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="d4618-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="d4618-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4618-141">NOTES</span></span>

## <span data-ttu-id="d4618-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4618-142">RELATED LINKS</span></span>
