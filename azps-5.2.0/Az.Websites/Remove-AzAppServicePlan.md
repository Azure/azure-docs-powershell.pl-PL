---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: dfd2cfd20ab11e2e70e03dc3e166c83729ef344a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367059"
---
# <span data-ttu-id="d2acd-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d2acd-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="d2acd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2acd-102">SYNOPSIS</span></span>
<span data-ttu-id="d2acd-103">Usuwa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="d2acd-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="d2acd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2acd-104">SYNTAX</span></span>

### <span data-ttu-id="d2acd-105">S1</span><span class="sxs-lookup"><span data-stu-id="d2acd-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2acd-106">S2</span><span class="sxs-lookup"><span data-stu-id="d2acd-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2acd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d2acd-107">DESCRIPTION</span></span>
<span data-ttu-id="d2acd-108">Polecenie cmdlet **Remove-AzAppServicePlan** usuwa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="d2acd-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="d2acd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2acd-109">EXAMPLES</span></span>

### <span data-ttu-id="d2acd-110">Przykład 1: usuwanie planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="d2acd-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="d2acd-111">To polecenie usuwa plan usługi Azure App Service o nazwie ContosoASP należący do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="d2acd-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d2acd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2acd-112">PARAMETERS</span></span>

### <span data-ttu-id="d2acd-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d2acd-113">-AppServicePlan</span></span>
<span data-ttu-id="d2acd-114">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="d2acd-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2acd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2acd-115">-AsJob</span></span>
<span data-ttu-id="d2acd-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d2acd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2acd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2acd-117">-DefaultProfile</span></span>
<span data-ttu-id="d2acd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2acd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2acd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d2acd-119">-Force</span></span>
<span data-ttu-id="d2acd-120">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="d2acd-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="d2acd-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d2acd-121">-Name</span></span>
<span data-ttu-id="d2acd-122">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="d2acd-122">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2acd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2acd-123">-ResourceGroupName</span></span>
<span data-ttu-id="d2acd-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d2acd-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2acd-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2acd-125">-Confirm</span></span>
<span data-ttu-id="d2acd-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2acd-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2acd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2acd-127">-WhatIf</span></span>
<span data-ttu-id="d2acd-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2acd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2acd-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d2acd-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2acd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2acd-130">CommonParameters</span></span>
<span data-ttu-id="d2acd-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2acd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2acd-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2acd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2acd-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2acd-133">INPUTS</span></span>

### <span data-ttu-id="d2acd-134">Microsoft. Azure. Commands. webapps. modele. aplikacji. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d2acd-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="d2acd-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2acd-135">OUTPUTS</span></span>

### <span data-ttu-id="d2acd-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d2acd-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="d2acd-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2acd-137">NOTES</span></span>

## <span data-ttu-id="d2acd-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2acd-138">RELATED LINKS</span></span>

[<span data-ttu-id="d2acd-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d2acd-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="d2acd-140">Nowe — AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d2acd-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="d2acd-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d2acd-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


