---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: bbe4cf87c3af86cd8a4e72f239d4aca7c3386786
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981361"
---
# <span data-ttu-id="bfb7d-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bfb7d-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="bfb7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfb7d-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb7d-103">Pobiera plan usługi aplikacji Azure w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bfb7d-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="bfb7d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bfb7d-104">SYNTAX</span></span>

### <span data-ttu-id="bfb7d-105">S1</span><span class="sxs-lookup"><span data-stu-id="bfb7d-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfb7d-106">S2</span><span class="sxs-lookup"><span data-stu-id="bfb7d-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfb7d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bfb7d-107">DESCRIPTION</span></span>
<span data-ttu-id="bfb7d-108">Polecenie **cmdlet Get-AzAppServicePlan** pobiera plan usługi Azure App Service w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bfb7d-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="bfb7d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bfb7d-109">EXAMPLES</span></span>

### <span data-ttu-id="bfb7d-110">Przykład 1. Uzyskiwanie planu usługi aplikacji z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bfb7d-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="bfb7d-111">To polecenie pobiera plan usługi aplikacji o nazwie ContosoASP należący do grupy zasobów o nazwie Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="bfb7d-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="bfb7d-112">Przykład 2. Uzyskiwanie wszystkich planów usługi aplikacji w lokalizacji</span><span class="sxs-lookup"><span data-stu-id="bfb7d-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="bfb7d-113">To polecenie pobiera wszystkie plany usługi aplikacji znajdujące się w regionie "Zachód US".</span><span class="sxs-lookup"><span data-stu-id="bfb7d-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="bfb7d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfb7d-114">PARAMETERS</span></span>

### <span data-ttu-id="bfb7d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb7d-115">-DefaultProfile</span></span>
<span data-ttu-id="bfb7d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb7d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfb7d-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bfb7d-117">-Location</span></span>
<span data-ttu-id="bfb7d-118">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bfb7d-118">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb7d-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bfb7d-119">-Name</span></span>
<span data-ttu-id="bfb7d-120">Nazwa planu serwisowego aplikacji</span><span class="sxs-lookup"><span data-stu-id="bfb7d-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb7d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb7d-121">-ResourceGroupName</span></span>
<span data-ttu-id="bfb7d-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bfb7d-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb7d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb7d-123">CommonParameters</span></span>
<span data-ttu-id="bfb7d-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb7d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb7d-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb7d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb7d-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfb7d-126">INPUTS</span></span>

### <span data-ttu-id="bfb7d-127">Brak</span><span class="sxs-lookup"><span data-stu-id="bfb7d-127">None</span></span>

## <span data-ttu-id="bfb7d-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfb7d-128">OUTPUTS</span></span>

### <span data-ttu-id="bfb7d-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bfb7d-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="bfb7d-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bfb7d-130">NOTES</span></span>

## <span data-ttu-id="bfb7d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfb7d-131">RELATED LINKS</span></span>

[<span data-ttu-id="bfb7d-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bfb7d-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="bfb7d-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bfb7d-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="bfb7d-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bfb7d-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


