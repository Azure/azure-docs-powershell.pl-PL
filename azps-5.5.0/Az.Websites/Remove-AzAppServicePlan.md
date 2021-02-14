---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: dfd2cfd20ab11e2e70e03dc3e166c83729ef344a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188698"
---
# <span data-ttu-id="0ea0f-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0ea0f-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="0ea0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ea0f-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea0f-103">Usuwa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="0ea0f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0ea0f-104">SYNTAX</span></span>

### <span data-ttu-id="0ea0f-105">S1</span><span class="sxs-lookup"><span data-stu-id="0ea0f-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ea0f-106">S2</span><span class="sxs-lookup"><span data-stu-id="0ea0f-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ea0f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0ea0f-107">DESCRIPTION</span></span>
<span data-ttu-id="0ea0f-108">Polecenie **cmdlet Remove-AzAppServicePlan** usuwa plan usługi azure app.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="0ea0f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0ea0f-109">EXAMPLES</span></span>

### <span data-ttu-id="0ea0f-110">Przykład 1. Usuwanie planu usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="0ea0f-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="0ea0f-111">To polecenie usuwa plan usługi aplikacji Azure o nazwie ContosoASP należący do grupy zasobów o nazwie Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0ea0f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ea0f-112">PARAMETERS</span></span>

### <span data-ttu-id="0ea0f-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0ea0f-113">-AppServicePlan</span></span>
<span data-ttu-id="0ea0f-114">Obiekt Planu usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="0ea0f-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="0ea0f-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0ea0f-115">-AsJob</span></span>
<span data-ttu-id="0ea0f-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0ea0f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ea0f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea0f-117">-DefaultProfile</span></span>
<span data-ttu-id="0ea0f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ea0f-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0ea0f-119">-Force</span></span>
<span data-ttu-id="0ea0f-120">Wymuszanie usuwania opcji</span><span class="sxs-lookup"><span data-stu-id="0ea0f-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="0ea0f-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0ea0f-121">-Name</span></span>
<span data-ttu-id="0ea0f-122">Nazwa planu serwisowego aplikacji</span><span class="sxs-lookup"><span data-stu-id="0ea0f-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="0ea0f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ea0f-123">-ResourceGroupName</span></span>
<span data-ttu-id="0ea0f-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0ea0f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0ea0f-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ea0f-125">-Confirm</span></span>
<span data-ttu-id="0ea0f-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ea0f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ea0f-127">-WhatIf</span></span>
<span data-ttu-id="0ea0f-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ea0f-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ea0f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea0f-130">CommonParameters</span></span>
<span data-ttu-id="0ea0f-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea0f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ea0f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea0f-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ea0f-133">INPUTS</span></span>

### <span data-ttu-id="0ea0f-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0ea0f-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="0ea0f-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0ea0f-135">OUTPUTS</span></span>

### <span data-ttu-id="0ea0f-136">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0ea0f-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0ea0f-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0ea0f-137">NOTES</span></span>

## <span data-ttu-id="0ea0f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ea0f-138">RELATED LINKS</span></span>

[<span data-ttu-id="0ea0f-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0ea0f-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="0ea0f-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0ea0f-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="0ea0f-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0ea0f-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


