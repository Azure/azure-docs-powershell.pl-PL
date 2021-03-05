---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 31c9728a95e5cfc52b283a8dddc0e24ffffe1630
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976353"
---
# <span data-ttu-id="26557-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="26557-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="26557-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26557-102">SYNOPSIS</span></span>
<span data-ttu-id="26557-103">Tworzenie zakładki.</span><span class="sxs-lookup"><span data-stu-id="26557-103">Create a Bookmark.</span></span>

## <span data-ttu-id="26557-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="26557-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26557-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="26557-105">DESCRIPTION</span></span>
<span data-ttu-id="26557-106">Polecenie **cmdlet New-AzSentinelBookmark** tworzy zakładkę z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="26557-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="26557-107">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="26557-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="26557-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="26557-108">EXAMPLES</span></span>

### <span data-ttu-id="26557-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26557-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="26557-110">W tym przykładzie **zakładkę tworzy** się w określonym obszarze roboczym, a następnie zapisuje w $Bookmark danych.</span><span class="sxs-lookup"><span data-stu-id="26557-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="26557-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26557-111">PARAMETERS</span></span>

### <span data-ttu-id="26557-112">- BookmarkId</span><span class="sxs-lookup"><span data-stu-id="26557-112">-BookmarkId</span></span>
<span data-ttu-id="26557-113">Identyfikator zakładki</span><span class="sxs-lookup"><span data-stu-id="26557-113">Bookmark Id,</span></span>

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

### <span data-ttu-id="26557-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26557-114">-DefaultProfile</span></span>
<span data-ttu-id="26557-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="26557-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26557-116">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="26557-116">-DisplayName</span></span>
<span data-ttu-id="26557-117">Nazwa wyświetlana reguły zakładki.</span><span class="sxs-lookup"><span data-stu-id="26557-117">Bookmark Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26557-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="26557-118">-IncidentInfo</span></span>
<span data-ttu-id="26557-119">Informacje o zdarzeniu zakładki.</span><span class="sxs-lookup"><span data-stu-id="26557-119">Bookmark Incident Info.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26557-120">— Label</span><span class="sxs-lookup"><span data-stu-id="26557-120">-Label</span></span>
<span data-ttu-id="26557-121">Etykiety zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="26557-121">Incident Labels.</span></span>

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

### <span data-ttu-id="26557-122">— Notatki</span><span class="sxs-lookup"><span data-stu-id="26557-122">-Notes</span></span>
<span data-ttu-id="26557-123">Notatki zakładek.</span><span class="sxs-lookup"><span data-stu-id="26557-123">Bookmark Notes.</span></span>

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

### <span data-ttu-id="26557-124">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="26557-124">-Query</span></span>
<span data-ttu-id="26557-125">Zapytanie zakładki.</span><span class="sxs-lookup"><span data-stu-id="26557-125">Bookmark Query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26557-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="26557-126">-QueryResult</span></span>
<span data-ttu-id="26557-127">Wynik zapytania zakładki.</span><span class="sxs-lookup"><span data-stu-id="26557-127">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="26557-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26557-128">-ResourceGroupName</span></span>
<span data-ttu-id="26557-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26557-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26557-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="26557-130">-WorkspaceName</span></span>
<span data-ttu-id="26557-131">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="26557-131">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26557-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26557-132">-Confirm</span></span>
<span data-ttu-id="26557-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="26557-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26557-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26557-134">-WhatIf</span></span>
<span data-ttu-id="26557-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26557-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26557-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="26557-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26557-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26557-137">CommonParameters</span></span>
<span data-ttu-id="26557-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26557-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26557-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26557-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26557-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26557-140">INPUTS</span></span>

### <span data-ttu-id="26557-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="26557-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="26557-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26557-142">OUTPUTS</span></span>

### <span data-ttu-id="26557-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="26557-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="26557-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="26557-144">NOTES</span></span>

## <span data-ttu-id="26557-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26557-145">RELATED LINKS</span></span>
