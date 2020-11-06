---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d5164e47dd759538fea6f0ab143ef9640055f1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542107"
---
# <span data-ttu-id="c2077-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c2077-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="c2077-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2077-102">SYNOPSIS</span></span>
<span data-ttu-id="c2077-103">Usuwa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="c2077-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2077-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2077-104">SYNTAX</span></span>

### <span data-ttu-id="c2077-105">S1</span><span class="sxs-lookup"><span data-stu-id="c2077-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2077-106">S2</span><span class="sxs-lookup"><span data-stu-id="c2077-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2077-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c2077-107">DESCRIPTION</span></span>
<span data-ttu-id="c2077-108">Polecenie cmdlet **Remove-AzureRmAppServicePlan** usuwa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="c2077-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="c2077-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2077-109">EXAMPLES</span></span>

### <span data-ttu-id="c2077-110">Przykład 1: usuwanie planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="c2077-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="c2077-111">To polecenie usuwa plan usługi Azure App Service o nazwie ContosoASP należący do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="c2077-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c2077-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2077-112">PARAMETERS</span></span>

### <span data-ttu-id="c2077-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c2077-113">-AppServicePlan</span></span>
<span data-ttu-id="c2077-114">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="c2077-114">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2077-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2077-115">-DefaultProfile</span></span>
<span data-ttu-id="c2077-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2077-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2077-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c2077-117">-Force</span></span>
<span data-ttu-id="c2077-118">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="c2077-118">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2077-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2077-119">-Name</span></span>
<span data-ttu-id="c2077-120">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="c2077-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2077-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2077-121">-ResourceGroupName</span></span>
<span data-ttu-id="c2077-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c2077-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2077-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2077-123">-Confirm</span></span>
<span data-ttu-id="c2077-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2077-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2077-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2077-125">-WhatIf</span></span>
<span data-ttu-id="c2077-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2077-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2077-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2077-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2077-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2077-128">-AsJob</span></span>
<span data-ttu-id="c2077-129">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c2077-129">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2077-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2077-130">CommonParameters</span></span>
<span data-ttu-id="c2077-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2077-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2077-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2077-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2077-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2077-133">INPUTS</span></span>

### <span data-ttu-id="c2077-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="c2077-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="c2077-135">Parametr "AppServicePlan" akceptuje wartość typu "ServerFarmWithRichSku" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c2077-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="c2077-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2077-136">OUTPUTS</span></span>

### <span data-ttu-id="c2077-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c2077-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="c2077-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2077-138">NOTES</span></span>

## <span data-ttu-id="c2077-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2077-139">RELATED LINKS</span></span>

[<span data-ttu-id="c2077-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c2077-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="c2077-141">Nowe — AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c2077-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="c2077-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c2077-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


