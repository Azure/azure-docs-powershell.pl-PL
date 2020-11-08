---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: af94f1bec48bf54284ccf6e0011753a737dac30b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231589"
---
# <span data-ttu-id="2bb28-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2bb28-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="2bb28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2bb28-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb28-103">Tworzy plan usługi App Service w danej lokalizacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="2bb28-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="2bb28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2bb28-104">SYNTAX</span></span>

### <span data-ttu-id="2bb28-105">S1</span><span class="sxs-lookup"><span data-stu-id="2bb28-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2bb28-106">S2</span><span class="sxs-lookup"><span data-stu-id="2bb28-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bb28-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2bb28-107">DESCRIPTION</span></span>
<span data-ttu-id="2bb28-108">Polecenie cmdlet **New-AzAppServicePlan** tworzy plan usługi Azure App Service w podanej lokalizacji geograficznej z określoną warstwą, rozmiarem pracownika oraz liczbą pracowników.</span><span class="sxs-lookup"><span data-stu-id="2bb28-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="2bb28-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2bb28-109">EXAMPLES</span></span>

### <span data-ttu-id="2bb28-110">Przykład 1. Tworzenie planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="2bb28-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="2bb28-111">To polecenie tworzy plan usługi App Service o nazwie ContosoASP w grupie zasobów o nazwie Default-Web-Zachodnia w lokalizacji geograficznej zachód w STANach geograficznych.</span><span class="sxs-lookup"><span data-stu-id="2bb28-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="2bb28-112">Polecenie określa podstawową warstwę i przydziela dwóch małych pracowników.</span><span class="sxs-lookup"><span data-stu-id="2bb28-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="2bb28-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2bb28-113">PARAMETERS</span></span>

### <span data-ttu-id="2bb28-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2bb28-114">-AppServicePlan</span></span>
<span data-ttu-id="2bb28-115">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="2bb28-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="2bb28-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="2bb28-116">-AseName</span></span>
<span data-ttu-id="2bb28-117">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="2bb28-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="2bb28-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bb28-118">-AseResourceGroupName</span></span>
<span data-ttu-id="2bb28-119">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="2bb28-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="2bb28-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bb28-120">-AsJob</span></span>
<span data-ttu-id="2bb28-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2bb28-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bb28-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bb28-122">-DefaultProfile</span></span>
<span data-ttu-id="2bb28-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb28-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bb28-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="2bb28-124">-HyperV</span></span>
<span data-ttu-id="2bb28-125">Określ, czy plan usługi App Service będzie uruchamiać kontenery systemu Windows</span><span class="sxs-lookup"><span data-stu-id="2bb28-125">Specify this, App Service Plan will run Windows Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bb28-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2bb28-126">-Location</span></span>
<span data-ttu-id="2bb28-127">Pozycję</span><span class="sxs-lookup"><span data-stu-id="2bb28-127">Location</span></span> 

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

### <span data-ttu-id="2bb28-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2bb28-128">-Name</span></span>
<span data-ttu-id="2bb28-129">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="2bb28-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="2bb28-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="2bb28-130">-NumberofWorkers</span></span>
<span data-ttu-id="2bb28-131">Liczba pracowników</span><span class="sxs-lookup"><span data-stu-id="2bb28-131">Number Of Workers</span></span>

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

### <span data-ttu-id="2bb28-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="2bb28-132">-PerSiteScaling</span></span>
<span data-ttu-id="2bb28-133">Możliwość włączenia skalowania dla witryny</span><span class="sxs-lookup"><span data-stu-id="2bb28-133">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="2bb28-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bb28-134">-ResourceGroupName</span></span>
<span data-ttu-id="2bb28-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2bb28-135">Resource Group Name</span></span>

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

### <span data-ttu-id="2bb28-136">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="2bb28-136">-Tier</span></span>
<span data-ttu-id="2bb28-137">Trójwarstwowej</span><span class="sxs-lookup"><span data-stu-id="2bb28-137">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bb28-138">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="2bb28-138">-WorkerSize</span></span>
<span data-ttu-id="2bb28-139">Rozmiar procesu roboczego sieci Web</span><span class="sxs-lookup"><span data-stu-id="2bb28-139">Size of web worker</span></span>

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

### <span data-ttu-id="2bb28-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb28-140">CommonParameters</span></span>
<span data-ttu-id="2bb28-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bb28-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb28-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bb28-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb28-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2bb28-143">INPUTS</span></span>

### <span data-ttu-id="2bb28-144">Microsoft. Azure. Commands. webapps. modele. aplikacji. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2bb28-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="2bb28-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2bb28-145">OUTPUTS</span></span>

### <span data-ttu-id="2bb28-146">Microsoft. Azure. Commands. webapps. modele. aplikacji. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2bb28-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="2bb28-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2bb28-147">NOTES</span></span>

## <span data-ttu-id="2bb28-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2bb28-148">RELATED LINKS</span></span>

[<span data-ttu-id="2bb28-149">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2bb28-149">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="2bb28-150">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2bb28-150">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="2bb28-151">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2bb28-151">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


