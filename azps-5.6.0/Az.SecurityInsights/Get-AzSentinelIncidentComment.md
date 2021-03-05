---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: b25e99766c4dc0433b14810352968300fd5bd129
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986406"
---
# <span data-ttu-id="5499f-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="5499f-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="5499f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5499f-102">SYNOPSIS</span></span>
<span data-ttu-id="5499f-103">Pobierz komentarz zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="5499f-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="5499f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5499f-104">SYNTAX</span></span>

### <span data-ttu-id="5499f-105">IncidentId (Default)</span><span class="sxs-lookup"><span data-stu-id="5499f-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5499f-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="5499f-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5499f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5499f-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5499f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5499f-108">DESCRIPTION</span></span>
<span data-ttu-id="5499f-109">Polecenie **cmdlet Get-AzSentinelIncidentComment** pobiera komentarz zdarzenia z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="5499f-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="5499f-110">Jeśli określisz parametry *IncidentCommentId* i *IncidentId,* zostanie zwrócony jeden obiekt **IncidentComment.**</span><span class="sxs-lookup"><span data-stu-id="5499f-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="5499f-111">Jeśli parametr *IncidentCommentId* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie komentarze dotyczące zdarzenia dla określonego zdarzenia w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="5499f-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="5499f-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5499f-112">EXAMPLES</span></span>

### <span data-ttu-id="5499f-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5499f-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="5499f-114">W tym przykładzie wszystkie wartości **Zdarzenia** dotyczące określonego zdarzenia są przechowywane w określonym obszarze roboczym, a następnie są przechowywane w $IncidentComments obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="5499f-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="5499f-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5499f-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="5499f-116">Ten przykład pobiera wartość **"IncidentComment"** dla określonego zdarzenia w określonym obszarze roboczym, a następnie zapisuje ją w $IncidentComment obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="5499f-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="5499f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5499f-117">PARAMETERS</span></span>

### <span data-ttu-id="5499f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5499f-118">-DefaultProfile</span></span>
<span data-ttu-id="5499f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5499f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5499f-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="5499f-120">-IncidentCommentId</span></span>
<span data-ttu-id="5499f-121">Identyfikator komentarza zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="5499f-121">Incident Comment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5499f-122">- IncidentId</span><span class="sxs-lookup"><span data-stu-id="5499f-122">-IncidentId</span></span>
<span data-ttu-id="5499f-123">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="5499f-123">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5499f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5499f-124">-ResourceGroupName</span></span>
<span data-ttu-id="5499f-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5499f-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5499f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5499f-126">-ResourceId</span></span>
<span data-ttu-id="5499f-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="5499f-127">Resource Id.</span></span>

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

### <span data-ttu-id="5499f-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5499f-128">-WorkspaceName</span></span>
<span data-ttu-id="5499f-129">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="5499f-129">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5499f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5499f-130">CommonParameters</span></span>
<span data-ttu-id="5499f-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5499f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5499f-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5499f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5499f-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5499f-133">INPUTS</span></span>

### <span data-ttu-id="5499f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5499f-134">System.String</span></span>
## <span data-ttu-id="5499f-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5499f-135">OUTPUTS</span></span>

### <span data-ttu-id="5499f-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="5499f-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="5499f-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5499f-137">NOTES</span></span>

## <span data-ttu-id="5499f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5499f-138">RELATED LINKS</span></span>
