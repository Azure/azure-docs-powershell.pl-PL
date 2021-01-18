---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: d33c126da2a77736871a9ec1f950382168f52bee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502979"
---
# <span data-ttu-id="e932a-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="e932a-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="e932a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e932a-102">SYNOPSIS</span></span>
<span data-ttu-id="e932a-103">Uzyskaj komentarz dotyczący incydentu.</span><span class="sxs-lookup"><span data-stu-id="e932a-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="e932a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e932a-104">SYNTAX</span></span>

### <span data-ttu-id="e932a-105">IncidentId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e932a-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e932a-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="e932a-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e932a-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e932a-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e932a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e932a-108">DESCRIPTION</span></span>
<span data-ttu-id="e932a-109">Polecenie cmdlet **Get-AzSentinelIncidentComment** pobiera komentarz dotyczący incydentu z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e932a-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="e932a-110">Jeśli określisz parametry *IncidentCommentId* i *IncidentId* , zwracany jest jeden obiekt **IncidentComment** .</span><span class="sxs-lookup"><span data-stu-id="e932a-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="e932a-111">Jeśli nie określisz parametru *IncidentCommentId* , zostanie zwrócona tablica zawierająca wszystkie komentarze incydentu dla określonego incydentu w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="e932a-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="e932a-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e932a-112">EXAMPLES</span></span>

### <span data-ttu-id="e932a-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e932a-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="e932a-114">W tym przykładzie są pobierane wszystkie **IncidentComments** dla określonego incydentu w określonym obszarze roboczym, a następnie są przechowywane w zmiennej $IncidentComments.</span><span class="sxs-lookup"><span data-stu-id="e932a-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="e932a-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e932a-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="e932a-116">W tym przykładzie jest pobierana **IncidentComment** dla określonego incydentu w określonym obszarze roboczym, a następnie jest ona przechowywana w zmiennej $IncidentComment.</span><span class="sxs-lookup"><span data-stu-id="e932a-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="e932a-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e932a-117">PARAMETERS</span></span>

### <span data-ttu-id="e932a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e932a-118">-DefaultProfile</span></span>
<span data-ttu-id="e932a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e932a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e932a-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="e932a-120">-IncidentCommentId</span></span>
<span data-ttu-id="e932a-121">Identyfikator komentarza dotyczącego incydentu.</span><span class="sxs-lookup"><span data-stu-id="e932a-121">Incident Comment Id.</span></span>

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

### <span data-ttu-id="e932a-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="e932a-122">-IncidentId</span></span>
<span data-ttu-id="e932a-123">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="e932a-123">Incident Id.</span></span>

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

### <span data-ttu-id="e932a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e932a-124">-ResourceGroupName</span></span>
<span data-ttu-id="e932a-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e932a-125">Resource group name.</span></span>

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

### <span data-ttu-id="e932a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e932a-126">-ResourceId</span></span>
<span data-ttu-id="e932a-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e932a-127">Resource Id.</span></span>

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

### <span data-ttu-id="e932a-128">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="e932a-128">-WorkspaceName</span></span>
<span data-ttu-id="e932a-129">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e932a-129">Workspace Name.</span></span>

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

### <span data-ttu-id="e932a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e932a-130">CommonParameters</span></span>
<span data-ttu-id="e932a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e932a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e932a-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e932a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e932a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e932a-133">INPUTS</span></span>

### <span data-ttu-id="e932a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e932a-134">System.String</span></span>
## <span data-ttu-id="e932a-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e932a-135">OUTPUTS</span></span>

### <span data-ttu-id="e932a-136">Microsoft. Azure. Commands. SecurityInsights. models. IncidentComments. PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="e932a-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="e932a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e932a-137">NOTES</span></span>

## <span data-ttu-id="e932a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e932a-138">RELATED LINKS</span></span>
