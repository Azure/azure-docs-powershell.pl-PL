---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238049"
---
# <span data-ttu-id="8ff1d-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="8ff1d-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="8ff1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ff1d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff1d-103">Zarejestruj grupę aplikacji pulpitu wirtualnego systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="8ff1d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8ff1d-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8ff1d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8ff1d-105">DESCRIPTION</span></span>
<span data-ttu-id="8ff1d-106">Zarejestruj grupę aplikacji pulpitu wirtualnego systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="8ff1d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8ff1d-107">EXAMPLES</span></span>

### <span data-ttu-id="8ff1d-108">Przykład 1. Rejestrowanie grupy aplikacji pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="8ff1d-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="8ff1d-109">To polecenie rejestruje grupę aplikacji pulpitu wirtualnego systemu Windows w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="8ff1d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ff1d-110">PARAMETERS</span></span>

### <span data-ttu-id="8ff1d-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="8ff1d-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="8ff1d-112">Ścieżka applicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="8ff1d-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="8ff1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ff1d-113">-DefaultProfile</span></span>
<span data-ttu-id="8ff1d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ff1d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ff1d-115">-ResourceGroupName</span></span>
<span data-ttu-id="8ff1d-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8ff1d-116">Resource Group Name</span></span>

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

### <span data-ttu-id="8ff1d-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ff1d-117">-SubscriptionId</span></span>
<span data-ttu-id="8ff1d-118">Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8ff1d-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ff1d-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8ff1d-119">-WorkspaceName</span></span>
<span data-ttu-id="8ff1d-120">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="8ff1d-120">Workspace Name</span></span>

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

### <span data-ttu-id="8ff1d-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ff1d-121">-Confirm</span></span>
<span data-ttu-id="8ff1d-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ff1d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ff1d-123">-WhatIf</span></span>
<span data-ttu-id="8ff1d-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ff1d-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ff1d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff1d-126">CommonParameters</span></span>
<span data-ttu-id="8ff1d-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff1d-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ff1d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff1d-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ff1d-129">INPUTS</span></span>

## <span data-ttu-id="8ff1d-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ff1d-130">OUTPUTS</span></span>

### <span data-ttu-id="8ff1d-131">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="8ff1d-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="8ff1d-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8ff1d-132">NOTES</span></span>

<span data-ttu-id="8ff1d-133">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8ff1d-133">ALIASES</span></span>

## <span data-ttu-id="8ff1d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ff1d-134">RELATED LINKS</span></span>

