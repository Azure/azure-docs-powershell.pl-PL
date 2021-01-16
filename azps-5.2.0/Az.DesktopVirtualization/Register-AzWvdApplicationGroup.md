---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341146"
---
# <span data-ttu-id="50aca-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="50aca-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="50aca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50aca-102">SYNOPSIS</span></span>
<span data-ttu-id="50aca-103">Rejestrowanie grupy aplikacji klasycznej Windows Virtual.</span><span class="sxs-lookup"><span data-stu-id="50aca-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="50aca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50aca-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="50aca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50aca-105">DESCRIPTION</span></span>
<span data-ttu-id="50aca-106">Rejestrowanie grupy aplikacji klasycznej Windows Virtual.</span><span class="sxs-lookup"><span data-stu-id="50aca-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="50aca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50aca-107">EXAMPLES</span></span>

### <span data-ttu-id="50aca-108">Przykład 1: rejestrowanie grupy aplikacji klasycznej Windows Virtual</span><span class="sxs-lookup"><span data-stu-id="50aca-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="50aca-109">To polecenie rejestruje grupę aplikacji pulpit wirtualny systemu Windows w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="50aca-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="50aca-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50aca-110">PARAMETERS</span></span>

### <span data-ttu-id="50aca-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="50aca-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="50aca-112">Ścieżka ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="50aca-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="50aca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50aca-113">-DefaultProfile</span></span>
<span data-ttu-id="50aca-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50aca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50aca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50aca-115">-ResourceGroupName</span></span>
<span data-ttu-id="50aca-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="50aca-116">Resource Group Name</span></span>

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

### <span data-ttu-id="50aca-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="50aca-117">-SubscriptionId</span></span>
<span data-ttu-id="50aca-118">Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="50aca-118">Subscription Id</span></span>

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

### <span data-ttu-id="50aca-119">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="50aca-119">-WorkspaceName</span></span>
<span data-ttu-id="50aca-120">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="50aca-120">Workspace Name</span></span>

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

### <span data-ttu-id="50aca-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50aca-121">-Confirm</span></span>
<span data-ttu-id="50aca-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50aca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50aca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50aca-123">-WhatIf</span></span>
<span data-ttu-id="50aca-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50aca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50aca-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="50aca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50aca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50aca-126">CommonParameters</span></span>
<span data-ttu-id="50aca-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50aca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50aca-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50aca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50aca-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50aca-129">INPUTS</span></span>

## <span data-ttu-id="50aca-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50aca-130">OUTPUTS</span></span>

### <span data-ttu-id="50aca-131">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="50aca-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="50aca-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50aca-132">NOTES</span></span>

<span data-ttu-id="50aca-133">PISUJE</span><span class="sxs-lookup"><span data-stu-id="50aca-133">ALIASES</span></span>

## <span data-ttu-id="50aca-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50aca-134">RELATED LINKS</span></span>

