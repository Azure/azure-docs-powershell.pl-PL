---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d1d07e27a7ad6fb6059cbfc8e4c972b1cedaf7e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553727"
---
# <span data-ttu-id="b4b5a-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b4b5a-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="b4b5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b5a-103">Usuwa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4b5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4b5a-104">SYNTAX</span></span>

### <span data-ttu-id="b4b5a-105">S1</span><span class="sxs-lookup"><span data-stu-id="b4b5a-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4b5a-106">S2</span><span class="sxs-lookup"><span data-stu-id="b4b5a-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4b5a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b4b5a-107">DESCRIPTION</span></span>
<span data-ttu-id="b4b5a-108">Polecenie cmdlet **Remove-AzureRmAppServicePlan** usuwa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="b4b5a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4b5a-109">EXAMPLES</span></span>

### <span data-ttu-id="b4b5a-110">Przykład 1: usuwanie planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="b4b5a-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="b4b5a-111">To polecenie usuwa plan usługi Azure App Service o nazwie ContosoASP należący do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b4b5a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4b5a-112">PARAMETERS</span></span>

### <span data-ttu-id="b4b5a-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b4b5a-113">-AppServicePlan</span></span>
<span data-ttu-id="b4b5a-114">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="b4b5a-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b5a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b4b5a-115">-Force</span></span>
<span data-ttu-id="b4b5a-116">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="b4b5a-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="b4b5a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4b5a-117">-Name</span></span>
<span data-ttu-id="b4b5a-118">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="b4b5a-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="b4b5a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4b5a-119">-ResourceGroupName</span></span>
<span data-ttu-id="b4b5a-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b4b5a-120">Resource Group Name</span></span>

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

### <span data-ttu-id="b4b5a-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4b5a-121">-Confirm</span></span>
<span data-ttu-id="b4b5a-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4b5a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4b5a-123">-WhatIf</span></span>
<span data-ttu-id="b4b5a-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4b5a-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4b5a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b5a-126">-DefaultProfile</span></span>
<span data-ttu-id="b4b5a-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4b5a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b5a-128">CommonParameters</span></span>
<span data-ttu-id="b4b5a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b5a-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4b5a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b5a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4b5a-131">INPUTS</span></span>

### <span data-ttu-id="b4b5a-132">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="b4b5a-132">ServerFarmWithRichSku</span></span>
<span data-ttu-id="b4b5a-133">Parametr "AppServicePlan" akceptuje wartość typu "ServerFarmWithRichSku" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="b4b5a-133">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="b4b5a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4b5a-134">OUTPUTS</span></span>

### <span data-ttu-id="b4b5a-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b4b5a-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b4b5a-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4b5a-136">NOTES</span></span>

## <span data-ttu-id="b4b5a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4b5a-137">RELATED LINKS</span></span>

[<span data-ttu-id="b4b5a-138">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b4b5a-138">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="b4b5a-139">Nowe — AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b4b5a-139">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="b4b5a-140">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b4b5a-140">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


