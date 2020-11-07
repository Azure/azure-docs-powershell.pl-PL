---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: 015a16ec40e7b5159e6082acd47f2583edff1f09
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898125"
---
# <span data-ttu-id="22a38-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="22a38-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="22a38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22a38-102">SYNOPSIS</span></span>
<span data-ttu-id="22a38-103">Tworzy plan usługi App Service w danej lokalizacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="22a38-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22a38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22a38-104">SYNTAX</span></span>

### <span data-ttu-id="22a38-105">S1</span><span class="sxs-lookup"><span data-stu-id="22a38-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob][-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22a38-106">S2</span><span class="sxs-lookup"><span data-stu-id="22a38-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22a38-107">Opis</span><span class="sxs-lookup"><span data-stu-id="22a38-107">DESCRIPTION</span></span>
<span data-ttu-id="22a38-108">Polecenie cmdlet **New-AzureRmAppServicePlan** tworzy plan usługi Azure App Service w podanej lokalizacji geograficznej z określoną warstwą, rozmiarem pracownika oraz liczbą pracowników.</span><span class="sxs-lookup"><span data-stu-id="22a38-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="22a38-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22a38-109">EXAMPLES</span></span>

### <span data-ttu-id="22a38-110">Przykład 1. Tworzenie planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="22a38-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="22a38-111">To polecenie tworzy plan usługi App Service o nazwie ContosoASP w grupie zasobów o nazwie Default-Web-Zachodnia w lokalizacji geograficznej zachód w STANach geograficznych.</span><span class="sxs-lookup"><span data-stu-id="22a38-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="22a38-112">Polecenie określa podstawową warstwę i przydziela dwóch małych pracowników.</span><span class="sxs-lookup"><span data-stu-id="22a38-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="22a38-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22a38-113">PARAMETERS</span></span>

### <span data-ttu-id="22a38-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="22a38-114">-AppServicePlan</span></span>
<span data-ttu-id="22a38-115">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="22a38-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="22a38-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="22a38-116">-AseName</span></span>
<span data-ttu-id="22a38-117">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="22a38-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a38-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a38-118">-AseResourceGroupName</span></span>
<span data-ttu-id="22a38-119">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="22a38-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a38-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a38-120">-DefaultProfile</span></span>
<span data-ttu-id="22a38-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22a38-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22a38-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="22a38-122">-Location</span></span>
<span data-ttu-id="22a38-123">Pozycję</span><span class="sxs-lookup"><span data-stu-id="22a38-123">Location</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a38-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="22a38-124">-Name</span></span>
<span data-ttu-id="22a38-125">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="22a38-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="22a38-126">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="22a38-126">-NumberofWorkers</span></span>
<span data-ttu-id="22a38-127">Liczba pracowników</span><span class="sxs-lookup"><span data-stu-id="22a38-127">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a38-128">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="22a38-128">-PerSiteScaling</span></span>
<span data-ttu-id="22a38-129">Możliwość włączenia skalowania dla witryny</span><span class="sxs-lookup"><span data-stu-id="22a38-129">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a38-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a38-130">-ResourceGroupName</span></span>
<span data-ttu-id="22a38-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="22a38-131">Resource Group Name</span></span>

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

### <span data-ttu-id="22a38-132">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="22a38-132">-Tier</span></span>
<span data-ttu-id="22a38-133">Trójwarstwowej</span><span class="sxs-lookup"><span data-stu-id="22a38-133">Tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a38-134">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="22a38-134">-WorkerSize</span></span>
<span data-ttu-id="22a38-135">Rozmiar procesu roboczego sieci Web</span><span class="sxs-lookup"><span data-stu-id="22a38-135">Size of web worker</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="22a38-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22a38-136">-AsJob</span></span>
<span data-ttu-id="22a38-137">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="22a38-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22a38-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a38-138">CommonParameters</span></span>
<span data-ttu-id="22a38-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22a38-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a38-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22a38-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a38-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22a38-141">INPUTS</span></span>

### <span data-ttu-id="22a38-142">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="22a38-142">ServerFarmWithRichSku</span></span>
<span data-ttu-id="22a38-143">Parametr "AppServicePlan" akceptuje wartość typu "ServerFarmWithRichSku" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="22a38-143">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="22a38-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22a38-144">OUTPUTS</span></span>

### <span data-ttu-id="22a38-145">Microsoft. Azure. Management. Web. MODELES. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="22a38-145">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="22a38-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22a38-146">NOTES</span></span>

## <span data-ttu-id="22a38-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22a38-147">RELATED LINKS</span></span>

[<span data-ttu-id="22a38-148">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="22a38-148">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="22a38-149">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="22a38-149">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="22a38-150">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="22a38-150">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


