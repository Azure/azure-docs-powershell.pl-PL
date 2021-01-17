---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: c6a7381c993b52995ab39a60fde54900092a5915
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350149"
---
# <span data-ttu-id="83ab9-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="83ab9-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="83ab9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="83ab9-103">Wdrożenie wbudowanej usługi JAR to go.</span><span class="sxs-lookup"><span data-stu-id="83ab9-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="83ab9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83ab9-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="83ab9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="83ab9-105">DESCRIPTION</span></span>
<span data-ttu-id="83ab9-106">Wdrożenie wbudowanej usługi JAR to go.</span><span class="sxs-lookup"><span data-stu-id="83ab9-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="83ab9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83ab9-107">EXAMPLES</span></span>

### <span data-ttu-id="83ab9-108">Przykład 1: wdrażanie lokalnego skompilowanego jar w celu obsługi według nazwy.</span><span class="sxs-lookup"><span data-stu-id="83ab9-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="83ab9-109">Wdrażanie lokalnego skompilowanego jar w celu obsługi według nazwy.</span><span class="sxs-lookup"><span data-stu-id="83ab9-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="83ab9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83ab9-110">PARAMETERS</span></span>

### <span data-ttu-id="83ab9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83ab9-111">-AsJob</span></span>
<span data-ttu-id="83ab9-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="83ab9-112">Run the command as a job</span></span>

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

### <span data-ttu-id="83ab9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ab9-113">-DefaultProfile</span></span>
<span data-ttu-id="83ab9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="83ab9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83ab9-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="83ab9-115">-JarPath</span></span>
<span data-ttu-id="83ab9-116">Ścieżka jar musi być deploied.</span><span class="sxs-lookup"><span data-stu-id="83ab9-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="83ab9-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="83ab9-117">-Name</span></span>
<span data-ttu-id="83ab9-118">Nazwa zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="83ab9-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="83ab9-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="83ab9-119">-NoWait</span></span>
<span data-ttu-id="83ab9-120">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="83ab9-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="83ab9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83ab9-121">-ResourceGroupName</span></span>
<span data-ttu-id="83ab9-122">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="83ab9-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="83ab9-123">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="83ab9-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="83ab9-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="83ab9-124">-ServiceName</span></span>
<span data-ttu-id="83ab9-125">Nazwa zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="83ab9-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="83ab9-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="83ab9-126">-SubscriptionId</span></span>
<span data-ttu-id="83ab9-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83ab9-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="83ab9-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="83ab9-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="83ab9-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83ab9-129">-Confirm</span></span>
<span data-ttu-id="83ab9-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83ab9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83ab9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83ab9-131">-WhatIf</span></span>
<span data-ttu-id="83ab9-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83ab9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83ab9-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83ab9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83ab9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ab9-134">CommonParameters</span></span>
<span data-ttu-id="83ab9-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ab9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ab9-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83ab9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ab9-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83ab9-137">INPUTS</span></span>

## <span data-ttu-id="83ab9-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83ab9-138">OUTPUTS</span></span>

### <span data-ttu-id="83ab9-139">Microsoft. Azure. PowerShell. polecenia. SpringCloud. models. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="83ab9-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="83ab9-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83ab9-140">NOTES</span></span>

<span data-ttu-id="83ab9-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="83ab9-141">ALIASES</span></span>

## <span data-ttu-id="83ab9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83ab9-142">RELATED LINKS</span></span>

