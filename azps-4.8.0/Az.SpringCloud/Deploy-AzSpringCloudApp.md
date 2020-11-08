---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: 8a80c323f1cf1d8d015faeda6541b77667a6ca19
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220340"
---
# <span data-ttu-id="1ed27-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="1ed27-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="1ed27-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ed27-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed27-103">Wdrożenie wbudowanej usługi JAR to go.</span><span class="sxs-lookup"><span data-stu-id="1ed27-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="1ed27-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ed27-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1ed27-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ed27-105">DESCRIPTION</span></span>
<span data-ttu-id="1ed27-106">Wdrożenie wbudowanej usługi JAR to go.</span><span class="sxs-lookup"><span data-stu-id="1ed27-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="1ed27-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ed27-107">EXAMPLES</span></span>

### <span data-ttu-id="1ed27-108">Przykład 1: wdrażanie lokalnego skompilowanego jar w celu obsługi według nazwy.</span><span class="sxs-lookup"><span data-stu-id="1ed27-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="1ed27-109">Wdrażanie lokalnego skompilowanego jar w celu obsługi według nazwy.</span><span class="sxs-lookup"><span data-stu-id="1ed27-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="1ed27-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ed27-110">PARAMETERS</span></span>

### <span data-ttu-id="1ed27-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ed27-111">-AsJob</span></span>
<span data-ttu-id="1ed27-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="1ed27-112">Run the command as a job</span></span>

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

### <span data-ttu-id="1ed27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed27-113">-DefaultProfile</span></span>
<span data-ttu-id="1ed27-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ed27-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ed27-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="1ed27-115">-JarPath</span></span>
<span data-ttu-id="1ed27-116">Ścieżka jar musi być deploied.</span><span class="sxs-lookup"><span data-stu-id="1ed27-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="1ed27-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ed27-117">-Name</span></span>
<span data-ttu-id="1ed27-118">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1ed27-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="1ed27-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1ed27-119">-NoWait</span></span>
<span data-ttu-id="1ed27-120">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="1ed27-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1ed27-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ed27-121">-ResourceGroupName</span></span>
<span data-ttu-id="1ed27-122">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="1ed27-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1ed27-123">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="1ed27-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1ed27-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1ed27-124">-ServiceName</span></span>
<span data-ttu-id="1ed27-125">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="1ed27-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="1ed27-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1ed27-126">-SubscriptionId</span></span>
<span data-ttu-id="1ed27-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1ed27-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1ed27-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="1ed27-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1ed27-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ed27-129">-Confirm</span></span>
<span data-ttu-id="1ed27-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ed27-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ed27-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ed27-131">-WhatIf</span></span>
<span data-ttu-id="1ed27-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ed27-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ed27-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ed27-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ed27-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed27-134">CommonParameters</span></span>
<span data-ttu-id="1ed27-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ed27-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed27-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ed27-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed27-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ed27-137">INPUTS</span></span>

## <span data-ttu-id="1ed27-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ed27-138">OUTPUTS</span></span>

### <span data-ttu-id="1ed27-139">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. Api20190501Preview. IAppResource</span><span class="sxs-lookup"><span data-stu-id="1ed27-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="1ed27-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ed27-140">NOTES</span></span>

<span data-ttu-id="1ed27-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="1ed27-141">ALIASES</span></span>

## <span data-ttu-id="1ed27-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ed27-142">RELATED LINKS</span></span>

