---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: e03e7dee6e233934216c04a44c1e100d3e26347b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718971"
---
# <span data-ttu-id="bbacd-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bbacd-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="bbacd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bbacd-102">SYNOPSIS</span></span>
<span data-ttu-id="bbacd-103">Tworzy plan usługi App Service w danej lokalizacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="bbacd-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbacd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bbacd-104">SYNTAX</span></span>

### <span data-ttu-id="bbacd-105">S1</span><span class="sxs-lookup"><span data-stu-id="bbacd-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbacd-106">S2</span><span class="sxs-lookup"><span data-stu-id="bbacd-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbacd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bbacd-107">DESCRIPTION</span></span>
<span data-ttu-id="bbacd-108">Polecenie cmdlet **New-AzureRmAppServicePlan** tworzy plan usługi Azure App Service w podanej lokalizacji geograficznej z określoną warstwą, rozmiarem pracownika oraz liczbą pracowników.</span><span class="sxs-lookup"><span data-stu-id="bbacd-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="bbacd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bbacd-109">EXAMPLES</span></span>

### <span data-ttu-id="bbacd-110">Przykład 1. Tworzenie planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="bbacd-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="bbacd-111">To polecenie tworzy plan usługi App Service o nazwie ContosoASP w grupie zasobów o nazwie Default-Web-Zachodnia w lokalizacji geograficznej zachód w STANach geograficznych.</span><span class="sxs-lookup"><span data-stu-id="bbacd-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="bbacd-112">Polecenie określa podstawową warstwę i przydziela dwóch małych pracowników.</span><span class="sxs-lookup"><span data-stu-id="bbacd-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="bbacd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bbacd-113">PARAMETERS</span></span>

### <span data-ttu-id="bbacd-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bbacd-114">-AppServicePlan</span></span>
<span data-ttu-id="bbacd-115">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="bbacd-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="bbacd-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="bbacd-116">-AseName</span></span>
<span data-ttu-id="bbacd-117">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="bbacd-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbacd-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbacd-118">-AseResourceGroupName</span></span>
<span data-ttu-id="bbacd-119">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="bbacd-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbacd-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bbacd-120">-Location</span></span>
<span data-ttu-id="bbacd-121">Pozycję</span><span class="sxs-lookup"><span data-stu-id="bbacd-121">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbacd-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bbacd-122">-Name</span></span>
<span data-ttu-id="bbacd-123">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="bbacd-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="bbacd-124">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="bbacd-124">-NumberofWorkers</span></span>
<span data-ttu-id="bbacd-125">Liczba pracowników</span><span class="sxs-lookup"><span data-stu-id="bbacd-125">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbacd-126">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="bbacd-126">-PerSiteScaling</span></span>
<span data-ttu-id="bbacd-127">Możliwość włączenia skalowania dla witryny</span><span class="sxs-lookup"><span data-stu-id="bbacd-127">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbacd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbacd-128">-ResourceGroupName</span></span>
<span data-ttu-id="bbacd-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bbacd-129">Resource Group Name</span></span>

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

### <span data-ttu-id="bbacd-130">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="bbacd-130">-Tier</span></span>
<span data-ttu-id="bbacd-131">Trójwarstwowej</span><span class="sxs-lookup"><span data-stu-id="bbacd-131">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbacd-132">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="bbacd-132">-WorkerSize</span></span>
<span data-ttu-id="bbacd-133">Rozmiar procesu roboczego sieci Web</span><span class="sxs-lookup"><span data-stu-id="bbacd-133">Size of web worker</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbacd-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbacd-134">-DefaultProfile</span></span>
<span data-ttu-id="bbacd-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbacd-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbacd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbacd-136">CommonParameters</span></span>
<span data-ttu-id="bbacd-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbacd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbacd-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbacd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbacd-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbacd-139">INPUTS</span></span>

### <span data-ttu-id="bbacd-140">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="bbacd-140">ServerFarmWithRichSku</span></span>
<span data-ttu-id="bbacd-141">Parametr "AppServicePlan" akceptuje wartość typu "ServerFarmWithRichSku" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="bbacd-141">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="bbacd-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bbacd-142">OUTPUTS</span></span>

### <span data-ttu-id="bbacd-143">Microsoft. Azure. Management. Web. MODELES. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="bbacd-143">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="bbacd-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bbacd-144">NOTES</span></span>

## <span data-ttu-id="bbacd-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbacd-145">RELATED LINKS</span></span>

[<span data-ttu-id="bbacd-146">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bbacd-146">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="bbacd-147">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bbacd-147">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="bbacd-148">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bbacd-148">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


