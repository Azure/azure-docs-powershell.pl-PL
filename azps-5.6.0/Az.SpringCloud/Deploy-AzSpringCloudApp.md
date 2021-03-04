---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: 96b3b3fcb2fcea50e1607c67d98079e5d1600f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955329"
---
# <span data-ttu-id="2a9eb-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="2a9eb-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="2a9eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a9eb-102">SYNOPSIS</span></span>
<span data-ttu-id="2a9eb-103">Wddaj wbudowany słoj do serwisu.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="2a9eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2a9eb-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2a9eb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2a9eb-105">DESCRIPTION</span></span>
<span data-ttu-id="2a9eb-106">Wddaj wbudowany słoj do serwisu.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="2a9eb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2a9eb-107">EXAMPLES</span></span>

### <span data-ttu-id="2a9eb-108">Przykład 1. Wdrażanie lokalnego skompilowanego jar w usłudze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="2a9eb-109">Wdrażanie lokalnego skompilowanego jar w usłudze według nazwy.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="2a9eb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a9eb-110">PARAMETERS</span></span>

### <span data-ttu-id="2a9eb-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2a9eb-111">-AsJob</span></span>
<span data-ttu-id="2a9eb-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="2a9eb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="2a9eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a9eb-113">-DefaultProfile</span></span>
<span data-ttu-id="2a9eb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a9eb-115">— JarPath</span><span class="sxs-lookup"><span data-stu-id="2a9eb-115">-JarPath</span></span>
<span data-ttu-id="2a9eb-116">Ścieżka słoika musi zostać wycofana.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="2a9eb-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2a9eb-117">-Name</span></span>
<span data-ttu-id="2a9eb-118">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="2a9eb-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2a9eb-119">-NoWait</span></span>
<span data-ttu-id="2a9eb-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="2a9eb-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2a9eb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a9eb-121">-ResourceGroupName</span></span>
<span data-ttu-id="2a9eb-122">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2a9eb-123">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2a9eb-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2a9eb-124">-ServiceName</span></span>
<span data-ttu-id="2a9eb-125">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="2a9eb-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a9eb-126">-SubscriptionId</span></span>
<span data-ttu-id="2a9eb-127">Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2a9eb-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2a9eb-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a9eb-129">-Confirm</span></span>
<span data-ttu-id="2a9eb-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a9eb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a9eb-131">-WhatIf</span></span>
<span data-ttu-id="2a9eb-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a9eb-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a9eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a9eb-134">CommonParameters</span></span>
<span data-ttu-id="2a9eb-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a9eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a9eb-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a9eb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a9eb-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a9eb-137">INPUTS</span></span>

## <span data-ttu-id="2a9eb-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a9eb-138">OUTPUTS</span></span>

### <span data-ttu-id="2a9eb-139">Microsoft.Azure.PowerShell.cmdlet.SpringCloud.Models.Api200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="2a9eb-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="2a9eb-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2a9eb-140">NOTES</span></span>

<span data-ttu-id="2a9eb-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2a9eb-141">ALIASES</span></span>

## <span data-ttu-id="2a9eb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a9eb-142">RELATED LINKS</span></span>

