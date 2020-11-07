---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: b85d22d1030eaa12e58cded1c7225231c7e8b964
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897774"
---
# <span data-ttu-id="a3e90-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a3e90-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="a3e90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3e90-102">SYNOPSIS</span></span>
<span data-ttu-id="a3e90-103">Pobiera plan usługi aplikacji platformy Azure w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3e90-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3e90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3e90-104">SYNTAX</span></span>

### <span data-ttu-id="a3e90-105">S1</span><span class="sxs-lookup"><span data-stu-id="a3e90-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3e90-106">S2</span><span class="sxs-lookup"><span data-stu-id="a3e90-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3e90-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a3e90-107">DESCRIPTION</span></span>
<span data-ttu-id="a3e90-108">Polecenie cmdlet **Get-AzureRmAppServicePlan** pobiera plan usługi Azure App Service w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3e90-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="a3e90-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3e90-109">EXAMPLES</span></span>

### <span data-ttu-id="a3e90-110">Przykład 1: pobieranie planu usługi App Service z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a3e90-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="a3e90-111">To polecenie pobiera plan usługi App Service (o nazwie ContosoASP) należący do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="a3e90-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="a3e90-112">Przykład 2: pobieranie wszystkich planów usługi App Service w lokalizacji</span><span class="sxs-lookup"><span data-stu-id="a3e90-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="a3e90-113">To polecenie pobiera wszystkie plany usługi App Service, które znajdują się w regionie "Zachodnia USA".</span><span class="sxs-lookup"><span data-stu-id="a3e90-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="a3e90-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3e90-114">PARAMETERS</span></span>

### <span data-ttu-id="a3e90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3e90-115">-DefaultProfile</span></span>
<span data-ttu-id="a3e90-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3e90-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3e90-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a3e90-117">-Location</span></span>
<span data-ttu-id="a3e90-118">Pozycję</span><span class="sxs-lookup"><span data-stu-id="a3e90-118">Location</span></span> 

```yaml
Type: String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e90-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3e90-119">-Name</span></span>
<span data-ttu-id="a3e90-120">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="a3e90-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e90-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3e90-121">-ResourceGroupName</span></span>
<span data-ttu-id="a3e90-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a3e90-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e90-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e90-123">CommonParameters</span></span>
<span data-ttu-id="a3e90-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3e90-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3e90-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3e90-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e90-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3e90-126">INPUTS</span></span>

### <span data-ttu-id="a3e90-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a3e90-127">None</span></span>
<span data-ttu-id="a3e90-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a3e90-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a3e90-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3e90-129">OUTPUTS</span></span>

### <span data-ttu-id="a3e90-130">Microsoft. Azure. Management. Web. MODELES. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="a3e90-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="a3e90-131">Microsoft. Azure. Management. Web. MODELES. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="a3e90-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="a3e90-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3e90-132">NOTES</span></span>

## <span data-ttu-id="a3e90-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3e90-133">RELATED LINKS</span></span>

[<span data-ttu-id="a3e90-134">Nowe — AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a3e90-134">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="a3e90-135">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a3e90-135">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="a3e90-136">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a3e90-136">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


