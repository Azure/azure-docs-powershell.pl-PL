---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: 3d0e3ad30df71700eb83938181ed86a97a77528a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891877"
---
# <span data-ttu-id="49ea5-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49ea5-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="49ea5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="49ea5-103">Usuwa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="49ea5-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="49ea5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49ea5-104">SYNTAX</span></span>

### <span data-ttu-id="49ea5-105">S1</span><span class="sxs-lookup"><span data-stu-id="49ea5-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ea5-106">S2</span><span class="sxs-lookup"><span data-stu-id="49ea5-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ea5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="49ea5-107">DESCRIPTION</span></span>
<span data-ttu-id="49ea5-108">Polecenie cmdlet **Remove-AzAppServicePlan** usuwa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="49ea5-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="49ea5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49ea5-109">EXAMPLES</span></span>

### <span data-ttu-id="49ea5-110">Przykład 1: usuwanie planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="49ea5-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="49ea5-111">To polecenie usuwa plan usługi Azure App Service o nazwie ContosoASP należący do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="49ea5-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="49ea5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49ea5-112">PARAMETERS</span></span>

### <span data-ttu-id="49ea5-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49ea5-113">-AppServicePlan</span></span>
<span data-ttu-id="49ea5-114">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="49ea5-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49ea5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ea5-115">-DefaultProfile</span></span>
<span data-ttu-id="49ea5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49ea5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ea5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="49ea5-117">-Force</span></span>
<span data-ttu-id="49ea5-118">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="49ea5-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="49ea5-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="49ea5-119">-Name</span></span>
<span data-ttu-id="49ea5-120">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="49ea5-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="49ea5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49ea5-121">-ResourceGroupName</span></span>
<span data-ttu-id="49ea5-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="49ea5-122">Resource Group Name</span></span>

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

### <span data-ttu-id="49ea5-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49ea5-123">-Confirm</span></span>
<span data-ttu-id="49ea5-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49ea5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49ea5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ea5-125">-WhatIf</span></span>
<span data-ttu-id="49ea5-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49ea5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49ea5-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49ea5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49ea5-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49ea5-128">-AsJob</span></span>
<span data-ttu-id="49ea5-129">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="49ea5-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49ea5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ea5-130">CommonParameters</span></span>
<span data-ttu-id="49ea5-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ea5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ea5-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ea5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ea5-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49ea5-133">INPUTS</span></span>

### <span data-ttu-id="49ea5-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="49ea5-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="49ea5-135">Parametr "AppServicePlan" akceptuje wartość typu "ServerFarmWithRichSku" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="49ea5-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="49ea5-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49ea5-136">OUTPUTS</span></span>

### <span data-ttu-id="49ea5-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="49ea5-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="49ea5-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49ea5-138">NOTES</span></span>

## <span data-ttu-id="49ea5-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49ea5-139">RELATED LINKS</span></span>

[<span data-ttu-id="49ea5-140">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49ea5-140">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="49ea5-141">Nowe — AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49ea5-141">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="49ea5-142">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49ea5-142">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


