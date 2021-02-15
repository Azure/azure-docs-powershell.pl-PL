---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: c6a7381c993b52995ab39a60fde54900092a5915
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242051"
---
# <span data-ttu-id="455a0-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="455a0-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="455a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="455a0-102">SYNOPSIS</span></span>
<span data-ttu-id="455a0-103">Wddaj wbudowany słoj do serwisu.</span><span class="sxs-lookup"><span data-stu-id="455a0-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="455a0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="455a0-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="455a0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="455a0-105">DESCRIPTION</span></span>
<span data-ttu-id="455a0-106">Wddaj wbudowany słoj do serwisu.</span><span class="sxs-lookup"><span data-stu-id="455a0-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="455a0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="455a0-107">EXAMPLES</span></span>

### <span data-ttu-id="455a0-108">Przykład 1. Wdrażanie lokalnego skompilowanego jar w usłudze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="455a0-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="455a0-109">Wdrażanie lokalnego skompilowanego jar w usłudze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="455a0-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="455a0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="455a0-110">PARAMETERS</span></span>

### <span data-ttu-id="455a0-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="455a0-111">-AsJob</span></span>
<span data-ttu-id="455a0-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="455a0-112">Run the command as a job</span></span>

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

### <span data-ttu-id="455a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="455a0-113">-DefaultProfile</span></span>
<span data-ttu-id="455a0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="455a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="455a0-115">— JarPath</span><span class="sxs-lookup"><span data-stu-id="455a0-115">-JarPath</span></span>
<span data-ttu-id="455a0-116">Ścieżka słoika musi zostać wycofana.</span><span class="sxs-lookup"><span data-stu-id="455a0-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="455a0-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="455a0-117">-Name</span></span>
<span data-ttu-id="455a0-118">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="455a0-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="455a0-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="455a0-119">-NoWait</span></span>
<span data-ttu-id="455a0-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="455a0-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="455a0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="455a0-121">-ResourceGroupName</span></span>
<span data-ttu-id="455a0-122">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="455a0-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="455a0-123">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="455a0-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="455a0-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="455a0-124">-ServiceName</span></span>
<span data-ttu-id="455a0-125">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="455a0-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="455a0-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="455a0-126">-SubscriptionId</span></span>
<span data-ttu-id="455a0-127">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="455a0-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="455a0-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="455a0-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="455a0-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="455a0-129">-Confirm</span></span>
<span data-ttu-id="455a0-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="455a0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="455a0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="455a0-131">-WhatIf</span></span>
<span data-ttu-id="455a0-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="455a0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="455a0-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="455a0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="455a0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="455a0-134">CommonParameters</span></span>
<span data-ttu-id="455a0-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="455a0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="455a0-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="455a0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="455a0-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="455a0-137">INPUTS</span></span>

## <span data-ttu-id="455a0-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="455a0-138">OUTPUTS</span></span>

### <span data-ttu-id="455a0-139">Microsoft.Azure.PowerShell.cmdlet.SpringCloud.Models.Api200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="455a0-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="455a0-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="455a0-140">NOTES</span></span>

<span data-ttu-id="455a0-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="455a0-141">ALIASES</span></span>

## <span data-ttu-id="455a0-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="455a0-142">RELATED LINKS</span></span>

