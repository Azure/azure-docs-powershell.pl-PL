---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 9a1c1de8aef41089cfc874cf35b26fcc9bf0be52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011130"
---
# <span data-ttu-id="27a83-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="27a83-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="27a83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27a83-102">SYNOPSIS</span></span>
<span data-ttu-id="27a83-103">Tworzy plan usługi aplikacji Azure w danej lokalizacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="27a83-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="27a83-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="27a83-104">SYNTAX</span></span>

### <span data-ttu-id="27a83-105">S1</span><span class="sxs-lookup"><span data-stu-id="27a83-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-Tag <Hashtable>] [-Linux] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27a83-106">S2</span><span class="sxs-lookup"><span data-stu-id="27a83-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27a83-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="27a83-107">DESCRIPTION</span></span>
<span data-ttu-id="27a83-108">Polecenie **cmdlet New-AzAppServicePlan** tworzy plan usługi aplikacji Azure w określonej lokalizacji geograficznej z określoną warstwą, rozmiarem pracownika i liczbą pracowników.</span><span class="sxs-lookup"><span data-stu-id="27a83-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="27a83-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="27a83-109">EXAMPLES</span></span>

### <span data-ttu-id="27a83-110">Przykład 1. Tworzenie planu usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="27a83-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="27a83-111">To polecenie tworzy plan usługi aplikacji o nazwie ContosoASP w grupie zasobów o nazwie Default-Web-WestUS w lokalizacji geograficznej Zachód USA.</span><span class="sxs-lookup"><span data-stu-id="27a83-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="27a83-112">To polecenie określa warstwę podstawową i przydziela dwóch małych pracowników.</span><span class="sxs-lookup"><span data-stu-id="27a83-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="27a83-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27a83-113">PARAMETERS</span></span>

### <span data-ttu-id="27a83-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="27a83-114">-AppServicePlan</span></span>
<span data-ttu-id="27a83-115">Obiekt Planu usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="27a83-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="27a83-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="27a83-116">-AseName</span></span>
<span data-ttu-id="27a83-117">Nazwa środowiska usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="27a83-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="27a83-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a83-118">-AseResourceGroupName</span></span>
<span data-ttu-id="27a83-119">Nazwa grupy zasobów środowiska usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="27a83-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="27a83-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="27a83-120">-AsJob</span></span>
<span data-ttu-id="27a83-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="27a83-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27a83-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a83-122">-DefaultProfile</span></span>
<span data-ttu-id="27a83-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="27a83-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27a83-124">— HyperV</span><span class="sxs-lookup"><span data-stu-id="27a83-124">-HyperV</span></span>
<span data-ttu-id="27a83-125">Określ to, w planie usługi aplikacji będą uruchamiane kontenery systemu Windows</span><span class="sxs-lookup"><span data-stu-id="27a83-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="27a83-126">— Linux</span><span class="sxs-lookup"><span data-stu-id="27a83-126">-Linux</span></span>
<span data-ttu-id="27a83-127">Określ to, plan usługi aplikacji będzie uruchamiał kontenery systemu Linux</span><span class="sxs-lookup"><span data-stu-id="27a83-127">Specify this, App Service Plan will run Linux Containers</span></span>

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

### <span data-ttu-id="27a83-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="27a83-128">-Location</span></span>
<span data-ttu-id="27a83-129">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="27a83-129">Location</span></span> 

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

### <span data-ttu-id="27a83-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="27a83-130">-Name</span></span>
<span data-ttu-id="27a83-131">Nazwa planu serwisowego aplikacji</span><span class="sxs-lookup"><span data-stu-id="27a83-131">App Service Plan Name</span></span>

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

### <span data-ttu-id="27a83-132">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="27a83-132">-NumberofWorkers</span></span>
<span data-ttu-id="27a83-133">Liczba pracowników</span><span class="sxs-lookup"><span data-stu-id="27a83-133">Number Of Workers</span></span>

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

### <span data-ttu-id="27a83-134">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="27a83-134">-PerSiteScaling</span></span>
<span data-ttu-id="27a83-135">Czy należy włączyć skalowanie według witryny, czy nie</span><span class="sxs-lookup"><span data-stu-id="27a83-135">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="27a83-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a83-136">-ResourceGroupName</span></span>
<span data-ttu-id="27a83-137">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="27a83-137">Resource Group Name</span></span>

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

### <span data-ttu-id="27a83-138">— Tag</span><span class="sxs-lookup"><span data-stu-id="27a83-138">-Tag</span></span>
<span data-ttu-id="27a83-139">Tagi to pary nazwa/wartość, które umożliwiają kategoryzowanie zasobów</span><span class="sxs-lookup"><span data-stu-id="27a83-139">Tags are name/value pairs that enable you to categorize resources</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a83-140">- Warstwa</span><span class="sxs-lookup"><span data-stu-id="27a83-140">-Tier</span></span>
<span data-ttu-id="27a83-141">Warstwa</span><span class="sxs-lookup"><span data-stu-id="27a83-141">Tier</span></span>

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

### <span data-ttu-id="27a83-142">— WorkerSize</span><span class="sxs-lookup"><span data-stu-id="27a83-142">-WorkerSize</span></span>
<span data-ttu-id="27a83-143">Rozmiar pracownika sieci Web</span><span class="sxs-lookup"><span data-stu-id="27a83-143">Size of web worker</span></span>

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

### <span data-ttu-id="27a83-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a83-144">CommonParameters</span></span>
<span data-ttu-id="27a83-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27a83-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a83-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27a83-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a83-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27a83-147">INPUTS</span></span>

### <span data-ttu-id="27a83-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="27a83-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="27a83-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27a83-149">OUTPUTS</span></span>

### <span data-ttu-id="27a83-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="27a83-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="27a83-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="27a83-151">NOTES</span></span>

## <span data-ttu-id="27a83-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27a83-152">RELATED LINKS</span></span>

[<span data-ttu-id="27a83-153">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="27a83-153">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="27a83-154">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="27a83-154">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="27a83-155">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="27a83-155">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


