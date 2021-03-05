---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
ms.openlocfilehash: 7c532f6aca8c959367d4e67725f36b44e4978840
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991817"
---
# <span data-ttu-id="0c0e8-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="0c0e8-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="0c0e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c0e8-102">SYNOPSIS</span></span>
<span data-ttu-id="0c0e8-103">Tworzenie lub aktualizowanie autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="0c0e8-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="0c0e8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0c0e8-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0c0e8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0c0e8-105">DESCRIPTION</span></span>
<span data-ttu-id="0c0e8-106">Tworzenie lub aktualizowanie autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="0c0e8-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="0c0e8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0c0e8-107">EXAMPLES</span></span>

### <span data-ttu-id="0c0e8-108">Przykład 1. Tworzenie autoryzowania</span><span class="sxs-lookup"><span data-stu-id="0c0e8-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="0c0e8-109">To polecenie cmdlet tworzy autoryzację `azps-test-auth` w chmurze prywatnej `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="0c0e8-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="0c0e8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c0e8-110">PARAMETERS</span></span>

### <span data-ttu-id="0c0e8-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0c0e8-111">-AsJob</span></span>
<span data-ttu-id="0c0e8-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="0c0e8-112">Run the command as a job</span></span>

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

### <span data-ttu-id="0c0e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c0e8-113">-DefaultProfile</span></span>
<span data-ttu-id="0c0e8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c0e8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c0e8-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0c0e8-115">-Name</span></span>
<span data-ttu-id="0c0e8-116">Nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="0c0e8-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c0e8-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0c0e8-117">-NoWait</span></span>
<span data-ttu-id="0c0e8-118">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="0c0e8-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0c0e8-119">- PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="0c0e8-119">-PrivateCloudName</span></span>
<span data-ttu-id="0c0e8-120">Nazwa chmury prywatnej.</span><span class="sxs-lookup"><span data-stu-id="0c0e8-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="0c0e8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c0e8-121">-ResourceGroupName</span></span>
<span data-ttu-id="0c0e8-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0c0e8-122">The name of the resource group.</span></span>
<span data-ttu-id="0c0e8-123">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="0c0e8-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0c0e8-124">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c0e8-124">-SubscriptionId</span></span>
<span data-ttu-id="0c0e8-125">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0c0e8-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c0e8-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c0e8-126">-Confirm</span></span>
<span data-ttu-id="0c0e8-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0c0e8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c0e8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c0e8-128">-WhatIf</span></span>
<span data-ttu-id="0c0e8-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c0e8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c0e8-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0c0e8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c0e8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c0e8-131">CommonParameters</span></span>
<span data-ttu-id="0c0e8-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c0e8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c0e8-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c0e8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c0e8-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c0e8-134">INPUTS</span></span>

## <span data-ttu-id="0c0e8-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c0e8-135">OUTPUTS</span></span>

### <span data-ttu-id="0c0e8-136">Microsoft.Azure.PowerShell.cmdlet.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="0c0e8-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="0c0e8-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0c0e8-137">NOTES</span></span>

<span data-ttu-id="0c0e8-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0c0e8-138">ALIASES</span></span>

## <span data-ttu-id="0c0e8-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c0e8-139">RELATED LINKS</span></span>

