---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: b97506b8f104859c54c55ee1a937916623f4201d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525885"
---
# <span data-ttu-id="0c0ca-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0c0ca-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="0c0ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c0ca-102">SYNOPSIS</span></span>
<span data-ttu-id="0c0ca-103">Usuwa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="0c0ca-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c0ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c0ca-104">SYNTAX</span></span>

### <span data-ttu-id="0c0ca-105">S1</span><span class="sxs-lookup"><span data-stu-id="0c0ca-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c0ca-106">S2</span><span class="sxs-lookup"><span data-stu-id="0c0ca-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c0ca-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0c0ca-107">DESCRIPTION</span></span>
<span data-ttu-id="0c0ca-108">Polecenie cmdlet **Remove-AzureRmAppServicePlan** usuwa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="0c0ca-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="0c0ca-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c0ca-109">EXAMPLES</span></span>

### <span data-ttu-id="0c0ca-110">Przykład 1: usuwanie planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="0c0ca-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="0c0ca-111">To polecenie usuwa plan usługi Azure App Service o nazwie ContosoASP należący do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="0c0ca-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0c0ca-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c0ca-112">PARAMETERS</span></span>

### <span data-ttu-id="0c0ca-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0c0ca-113">-AppServicePlan</span></span>
<span data-ttu-id="0c0ca-114">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="0c0ca-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="0c0ca-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c0ca-115">-AsJob</span></span>
<span data-ttu-id="0c0ca-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0c0ca-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c0ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c0ca-117">-DefaultProfile</span></span>
<span data-ttu-id="0c0ca-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c0ca-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c0ca-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0c0ca-119">-Force</span></span>
<span data-ttu-id="0c0ca-120">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="0c0ca-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="0c0ca-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0c0ca-121">-Name</span></span>
<span data-ttu-id="0c0ca-122">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="0c0ca-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="0c0ca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c0ca-123">-ResourceGroupName</span></span>
<span data-ttu-id="0c0ca-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0c0ca-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0c0ca-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c0ca-125">-Confirm</span></span>
<span data-ttu-id="0c0ca-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c0ca-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c0ca-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c0ca-127">-WhatIf</span></span>
<span data-ttu-id="0c0ca-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c0ca-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c0ca-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0c0ca-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c0ca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c0ca-130">CommonParameters</span></span>
<span data-ttu-id="0c0ca-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c0ca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c0ca-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c0ca-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c0ca-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c0ca-133">INPUTS</span></span>

### <span data-ttu-id="0c0ca-134">Microsoft. Azure. Management. Web. MODELES. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0c0ca-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="0c0ca-135">Parametry: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c0ca-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="0c0ca-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c0ca-136">OUTPUTS</span></span>

### <span data-ttu-id="0c0ca-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0c0ca-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0c0ca-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c0ca-138">NOTES</span></span>

## <span data-ttu-id="0c0ca-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c0ca-139">RELATED LINKS</span></span>

[<span data-ttu-id="0c0ca-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0c0ca-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="0c0ca-141">Nowe — AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0c0ca-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="0c0ca-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0c0ca-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


