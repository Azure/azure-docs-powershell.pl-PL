---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 0533864f3fd16e9810e837629782b767fbdc0435
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223968"
---
# <span data-ttu-id="863ce-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="863ce-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="863ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="863ce-102">SYNOPSIS</span></span>
<span data-ttu-id="863ce-103">Wyrejestrowanie grupy aplikacji pulpit wirtualny systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="863ce-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="863ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="863ce-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="863ce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="863ce-105">DESCRIPTION</span></span>
<span data-ttu-id="863ce-106">Wyrejestrowanie grupy aplikacji pulpit wirtualny systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="863ce-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="863ce-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="863ce-107">EXAMPLES</span></span>

### <span data-ttu-id="863ce-108">Przykład 1. Wyrejestrowanie grupy aplikacji klasycznej Windows Virtual</span><span class="sxs-lookup"><span data-stu-id="863ce-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="863ce-109">To polecenie wyrejestrowuje grupę wirtualnych aplikacji klasycznych systemu Windows w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="863ce-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="863ce-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="863ce-110">PARAMETERS</span></span>

### <span data-ttu-id="863ce-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="863ce-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="863ce-112">Ścieżka ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="863ce-112">ResourceGroupName Path</span></span>

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

### <span data-ttu-id="863ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="863ce-113">-DefaultProfile</span></span>
<span data-ttu-id="863ce-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="863ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="863ce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="863ce-115">-ResourceGroupName</span></span>
<span data-ttu-id="863ce-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="863ce-116">Resource Group Name</span></span>

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

### <span data-ttu-id="863ce-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="863ce-117">-SubscriptionId</span></span>
<span data-ttu-id="863ce-118">Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="863ce-118">Subscription Id</span></span>

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

### <span data-ttu-id="863ce-119">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="863ce-119">-WorkspaceName</span></span>
<span data-ttu-id="863ce-120">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="863ce-120">Workspace Name</span></span>

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

### <span data-ttu-id="863ce-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="863ce-121">-Confirm</span></span>
<span data-ttu-id="863ce-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="863ce-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="863ce-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="863ce-123">-WhatIf</span></span>
<span data-ttu-id="863ce-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="863ce-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="863ce-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="863ce-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="863ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="863ce-126">CommonParameters</span></span>
<span data-ttu-id="863ce-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="863ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="863ce-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="863ce-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="863ce-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="863ce-129">INPUTS</span></span>

## <span data-ttu-id="863ce-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="863ce-130">OUTPUTS</span></span>

### <span data-ttu-id="863ce-131">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="863ce-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="863ce-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="863ce-132">NOTES</span></span>

<span data-ttu-id="863ce-133">PISUJE</span><span class="sxs-lookup"><span data-stu-id="863ce-133">ALIASES</span></span>

## <span data-ttu-id="863ce-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="863ce-134">RELATED LINKS</span></span>

