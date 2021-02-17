---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: eb0854ee3a71af3bdf19d2258187c435fb0f5860
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183538"
---
# <span data-ttu-id="49885-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="49885-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="49885-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49885-102">SYNOPSIS</span></span>
<span data-ttu-id="49885-103">Uzyskaj zdarzenie.</span><span class="sxs-lookup"><span data-stu-id="49885-103">Get an Incident.</span></span>

## <span data-ttu-id="49885-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49885-104">SYNTAX</span></span>

### <span data-ttu-id="49885-105">WorkspaceScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="49885-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49885-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="49885-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49885-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="49885-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49885-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="49885-108">DESCRIPTION</span></span>
<span data-ttu-id="49885-109">Polecenie **cmdlet Get-AzSentinelIncident** pobiera polecenie Incident z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="49885-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="49885-110">W przypadku określenia *parametru Identyfikator Zdarzenia* jest **zwracany** jeden obiekt Incident.</span><span class="sxs-lookup"><span data-stu-id="49885-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="49885-111">Jeśli parametr *IncidentId* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie zdarzenia w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="49885-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="49885-112">Za pomocą obiektu **Zdarzenie** można zaktualizować zdarzenie, na przykład możesz dodać notatki o **zdarzeniu.**</span><span class="sxs-lookup"><span data-stu-id="49885-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="49885-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49885-113">EXAMPLES</span></span>

### <span data-ttu-id="49885-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49885-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="49885-115">W tym przykładzie wszystkie zdarzenia **w** określonym obszarze roboczym są przechowywane w $Incidents danych.</span><span class="sxs-lookup"><span data-stu-id="49885-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="49885-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="49885-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="49885-117">W tym przykładzie **zdarzenie jest przechowywane** w określonym obszarze roboczym, a następnie jest przechowywane $Incident zmienną.</span><span class="sxs-lookup"><span data-stu-id="49885-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="49885-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49885-118">PARAMETERS</span></span>

### <span data-ttu-id="49885-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49885-119">-DefaultProfile</span></span>
<span data-ttu-id="49885-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49885-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49885-121">- IncidentId</span><span class="sxs-lookup"><span data-stu-id="49885-121">-IncidentId</span></span>
<span data-ttu-id="49885-122">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="49885-122">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49885-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49885-123">-ResourceGroupName</span></span>
<span data-ttu-id="49885-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49885-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49885-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49885-125">-ResourceId</span></span>
<span data-ttu-id="49885-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="49885-126">Resource Id.</span></span>

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

### <span data-ttu-id="49885-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="49885-127">-WorkspaceName</span></span>
<span data-ttu-id="49885-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="49885-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49885-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49885-129">CommonParameters</span></span>
<span data-ttu-id="49885-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49885-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49885-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49885-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49885-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49885-132">INPUTS</span></span>

### <span data-ttu-id="49885-133">System.String</span><span class="sxs-lookup"><span data-stu-id="49885-133">System.String</span></span>
## <span data-ttu-id="49885-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49885-134">OUTPUTS</span></span>

### <span data-ttu-id="49885-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="49885-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="49885-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49885-136">NOTES</span></span>

## <span data-ttu-id="49885-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49885-137">RELATED LINKS</span></span>
