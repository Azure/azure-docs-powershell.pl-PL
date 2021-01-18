---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 3c30edd841eb2e773c5d813e798e63fc9858437d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502975"
---
# <span data-ttu-id="830e5-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="830e5-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="830e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="830e5-102">SYNOPSIS</span></span>
<span data-ttu-id="830e5-103">Utwórz zakładkę.</span><span class="sxs-lookup"><span data-stu-id="830e5-103">Create a Bookmark.</span></span>

## <span data-ttu-id="830e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="830e5-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="830e5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="830e5-105">DESCRIPTION</span></span>
<span data-ttu-id="830e5-106">Polecenie cmdlet **New-AzSentinelBookmark** umożliwia utworzenie zakładki na podstawie określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="830e5-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="830e5-107">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="830e5-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="830e5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="830e5-108">EXAMPLES</span></span>

### <span data-ttu-id="830e5-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="830e5-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="830e5-110">W tym przykładzie przedstawiono tworzenie **zakładki** w określonym obszarze roboczym, a następnie zapisanie jej w zmiennej $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="830e5-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="830e5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="830e5-111">PARAMETERS</span></span>

### <span data-ttu-id="830e5-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="830e5-112">-BookmarkId</span></span>
<span data-ttu-id="830e5-113">Identyfikator zakładki,</span><span class="sxs-lookup"><span data-stu-id="830e5-113">Bookmark Id,</span></span>

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

### <span data-ttu-id="830e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830e5-114">-DefaultProfile</span></span>
<span data-ttu-id="830e5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="830e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="830e5-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="830e5-116">-DisplayName</span></span>
<span data-ttu-id="830e5-117">Nazwa wyświetlana reguły zakładki.</span><span class="sxs-lookup"><span data-stu-id="830e5-117">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="830e5-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="830e5-118">-IncidentInfo</span></span>
<span data-ttu-id="830e5-119">Informacje o zdarzeniu zakładki.</span><span class="sxs-lookup"><span data-stu-id="830e5-119">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="830e5-120">-Label</span><span class="sxs-lookup"><span data-stu-id="830e5-120">-Label</span></span>
<span data-ttu-id="830e5-121">Etykiety zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="830e5-121">Incident Labels.</span></span>

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

### <span data-ttu-id="830e5-122">-Uwagi</span><span class="sxs-lookup"><span data-stu-id="830e5-122">-Notes</span></span>
<span data-ttu-id="830e5-123">Notatki z zakładkami.</span><span class="sxs-lookup"><span data-stu-id="830e5-123">Bookmark Notes.</span></span>

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

### <span data-ttu-id="830e5-124">-Query</span><span class="sxs-lookup"><span data-stu-id="830e5-124">-Query</span></span>
<span data-ttu-id="830e5-125">Kwerenda zakładki.</span><span class="sxs-lookup"><span data-stu-id="830e5-125">Bookmark Query.</span></span>

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

### <span data-ttu-id="830e5-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="830e5-126">-QueryResult</span></span>
<span data-ttu-id="830e5-127">Wynik kwerendy zakładki.</span><span class="sxs-lookup"><span data-stu-id="830e5-127">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="830e5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="830e5-128">-ResourceGroupName</span></span>
<span data-ttu-id="830e5-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="830e5-129">Resource group name.</span></span>

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

### <span data-ttu-id="830e5-130">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="830e5-130">-WorkspaceName</span></span>
<span data-ttu-id="830e5-131">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="830e5-131">Workspace Name.</span></span>

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

### <span data-ttu-id="830e5-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="830e5-132">-Confirm</span></span>
<span data-ttu-id="830e5-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="830e5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="830e5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="830e5-134">-WhatIf</span></span>
<span data-ttu-id="830e5-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="830e5-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="830e5-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="830e5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="830e5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830e5-137">CommonParameters</span></span>
<span data-ttu-id="830e5-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="830e5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830e5-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="830e5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830e5-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="830e5-140">INPUTS</span></span>

### <span data-ttu-id="830e5-141">Microsoft. Azure. Commands. SecurityInsights. models. zakładki. PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="830e5-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="830e5-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="830e5-142">OUTPUTS</span></span>

### <span data-ttu-id="830e5-143">Microsoft. Azure. Commands. SecurityInsights. models. zakładki. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="830e5-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="830e5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="830e5-144">NOTES</span></span>

## <span data-ttu-id="830e5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="830e5-145">RELATED LINKS</span></span>
