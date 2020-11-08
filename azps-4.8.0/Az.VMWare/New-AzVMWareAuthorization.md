---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222409"
---
# <span data-ttu-id="5607b-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="5607b-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="5607b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5607b-102">SYNOPSIS</span></span>
<span data-ttu-id="5607b-103">Tworzenie lub aktualizowanie autoryzacji obwodu ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="5607b-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="5607b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5607b-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5607b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5607b-105">DESCRIPTION</span></span>
<span data-ttu-id="5607b-106">Tworzenie lub aktualizowanie autoryzacji obwodu ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="5607b-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="5607b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5607b-107">EXAMPLES</span></span>

### <span data-ttu-id="5607b-108">Przykład 1: Create Autorization</span><span class="sxs-lookup"><span data-stu-id="5607b-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="5607b-109">To polecenie cmdlet umożliwia utworzenie autoryzacji `azps-test-auth` w ramach prywatnej chmury `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="5607b-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="5607b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5607b-110">PARAMETERS</span></span>

### <span data-ttu-id="5607b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5607b-111">-AsJob</span></span>
<span data-ttu-id="5607b-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="5607b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5607b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5607b-113">-DefaultProfile</span></span>
<span data-ttu-id="5607b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5607b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5607b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5607b-115">-Name</span></span>
<span data-ttu-id="5607b-116">Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="5607b-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="5607b-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5607b-117">-NoWait</span></span>
<span data-ttu-id="5607b-118">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="5607b-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5607b-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="5607b-119">-PrivateCloudName</span></span>
<span data-ttu-id="5607b-120">Nazwa prywatnej chmury.</span><span class="sxs-lookup"><span data-stu-id="5607b-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="5607b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5607b-121">-ResourceGroupName</span></span>
<span data-ttu-id="5607b-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5607b-122">The name of the resource group.</span></span>
<span data-ttu-id="5607b-123">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="5607b-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5607b-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5607b-124">-SubscriptionId</span></span>
<span data-ttu-id="5607b-125">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="5607b-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5607b-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5607b-126">-Confirm</span></span>
<span data-ttu-id="5607b-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5607b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5607b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5607b-128">-WhatIf</span></span>
<span data-ttu-id="5607b-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5607b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5607b-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5607b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5607b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5607b-131">CommonParameters</span></span>
<span data-ttu-id="5607b-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5607b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5607b-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5607b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5607b-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5607b-134">INPUTS</span></span>

## <span data-ttu-id="5607b-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5607b-135">OUTPUTS</span></span>

### <span data-ttu-id="5607b-136">Microsoft. Azure. PowerShell. cmdlet. VMWare. modele. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="5607b-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="5607b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5607b-137">NOTES</span></span>

<span data-ttu-id="5607b-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="5607b-138">ALIASES</span></span>

## <span data-ttu-id="5607b-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5607b-139">RELATED LINKS</span></span>

