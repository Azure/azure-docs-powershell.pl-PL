---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: afbee0d6b13c1ce42931a2379cff6aa7ee0127b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317473"
---
# <span data-ttu-id="8c1a4-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c1a4-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="8c1a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c1a4-102">SYNOPSIS</span></span>
<span data-ttu-id="8c1a4-103">Pobiera plan usługi aplikacji platformy Azure w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c1a4-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="8c1a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c1a4-104">SYNTAX</span></span>

### <span data-ttu-id="8c1a4-105">S1</span><span class="sxs-lookup"><span data-stu-id="8c1a4-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c1a4-106">S2</span><span class="sxs-lookup"><span data-stu-id="8c1a4-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c1a4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8c1a4-107">DESCRIPTION</span></span>
<span data-ttu-id="8c1a4-108">Polecenie cmdlet **Get-AzAppServicePlan** pobiera plan usługi Azure App Service w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c1a4-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="8c1a4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c1a4-109">EXAMPLES</span></span>

### <span data-ttu-id="8c1a4-110">Przykład 1: pobieranie planu usługi App Service z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8c1a4-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="8c1a4-111">To polecenie pobiera plan usługi App Service (o nazwie ContosoASP) należący do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="8c1a4-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="8c1a4-112">Przykład 2: pobieranie wszystkich planów usługi App Service w lokalizacji</span><span class="sxs-lookup"><span data-stu-id="8c1a4-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="8c1a4-113">To polecenie pobiera wszystkie plany usługi App Service, które znajdują się w regionie "Zachodnia USA".</span><span class="sxs-lookup"><span data-stu-id="8c1a4-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="8c1a4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c1a4-114">PARAMETERS</span></span>

### <span data-ttu-id="8c1a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c1a4-115">-DefaultProfile</span></span>
<span data-ttu-id="8c1a4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c1a4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c1a4-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8c1a4-117">-Location</span></span>
<span data-ttu-id="8c1a4-118">Pozycję</span><span class="sxs-lookup"><span data-stu-id="8c1a4-118">Location</span></span> 

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

### <span data-ttu-id="8c1a4-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c1a4-119">-Name</span></span>
<span data-ttu-id="8c1a4-120">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="8c1a4-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="8c1a4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c1a4-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c1a4-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8c1a4-122">Resource Group Name</span></span>

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

### <span data-ttu-id="8c1a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c1a4-123">CommonParameters</span></span>
<span data-ttu-id="8c1a4-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c1a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c1a4-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c1a4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c1a4-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c1a4-126">INPUTS</span></span>

### <span data-ttu-id="8c1a4-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8c1a4-127">None</span></span>

## <span data-ttu-id="8c1a4-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c1a4-128">OUTPUTS</span></span>

### <span data-ttu-id="8c1a4-129">Microsoft. Azure. Commands. webapps. modele. aplikacji. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c1a4-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="8c1a4-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c1a4-130">NOTES</span></span>

## <span data-ttu-id="8c1a4-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c1a4-131">RELATED LINKS</span></span>

[<span data-ttu-id="8c1a4-132">Nowe — AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c1a4-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="8c1a4-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c1a4-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="8c1a4-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c1a4-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


