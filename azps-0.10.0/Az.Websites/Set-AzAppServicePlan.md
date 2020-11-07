---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: b679b98e84f389e35e7dc291822049e554d40a9a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891834"
---
# <span data-ttu-id="dd60c-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="dd60c-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="dd60c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd60c-102">SYNOPSIS</span></span>
<span data-ttu-id="dd60c-103">Umożliwia ustawienie planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="dd60c-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="dd60c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd60c-104">SYNTAX</span></span>

### <span data-ttu-id="dd60c-105">S1</span><span class="sxs-lookup"><span data-stu-id="dd60c-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd60c-106">S2</span><span class="sxs-lookup"><span data-stu-id="dd60c-106">S2</span></span>
```
Set-AzAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd60c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dd60c-107">DESCRIPTION</span></span>
<span data-ttu-id="dd60c-108">Polecenie cmdlet **Set-AzAppServicePlan** określa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="dd60c-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="dd60c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd60c-109">EXAMPLES</span></span>

### <span data-ttu-id="dd60c-110">1: modyfikowanie planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="dd60c-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="dd60c-111">To polecenie ustawia opcję PerSiteScaling na wartość prawda w planie usługi App Service o nazwie ContosoASP należącego do grupy zasobów o nazwie Default-Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="dd60c-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="dd60c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd60c-112">PARAMETERS</span></span>

### <span data-ttu-id="dd60c-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="dd60c-113">-AdminSiteName</span></span>
<span data-ttu-id="dd60c-114">Nazwa witryny administracyjnej</span><span class="sxs-lookup"><span data-stu-id="dd60c-114">Admin Site Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd60c-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="dd60c-115">-AppServicePlan</span></span>
<span data-ttu-id="dd60c-116">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="dd60c-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="dd60c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd60c-117">-DefaultProfile</span></span>
<span data-ttu-id="dd60c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd60c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd60c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd60c-119">-Name</span></span>
<span data-ttu-id="dd60c-120">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="dd60c-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="dd60c-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="dd60c-121">-NumberofWorkers</span></span>
<span data-ttu-id="dd60c-122">Liczba pracowników</span><span class="sxs-lookup"><span data-stu-id="dd60c-122">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd60c-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="dd60c-123">-PerSiteScaling</span></span>
<span data-ttu-id="dd60c-124">Wartość logiczna skalowania dla witryny</span><span class="sxs-lookup"><span data-stu-id="dd60c-124">Per Site Scaling Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd60c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd60c-125">-ResourceGroupName</span></span>
<span data-ttu-id="dd60c-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dd60c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="dd60c-127">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="dd60c-127">-Tier</span></span>
<span data-ttu-id="dd60c-128">Trójwarstwowej</span><span class="sxs-lookup"><span data-stu-id="dd60c-128">Tier</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd60c-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="dd60c-129">-WorkerSize</span></span>
<span data-ttu-id="dd60c-130">Rozmiar pracownika</span><span class="sxs-lookup"><span data-stu-id="dd60c-130">Worker Size</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="dd60c-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd60c-131">-AsJob</span></span>
<span data-ttu-id="dd60c-132">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="dd60c-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd60c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd60c-133">CommonParameters</span></span>
<span data-ttu-id="dd60c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd60c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd60c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd60c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd60c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd60c-136">INPUTS</span></span>

### <span data-ttu-id="dd60c-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="dd60c-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="dd60c-138">Parametr "AppServicePlan" akceptuje wartość typu "ServerFarmWithRichSku" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="dd60c-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="dd60c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd60c-139">OUTPUTS</span></span>

### <span data-ttu-id="dd60c-140">Microsoft. Azure. Management. Web. MODELES. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="dd60c-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="dd60c-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd60c-141">NOTES</span></span>

## <span data-ttu-id="dd60c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd60c-142">RELATED LINKS</span></span>

[<span data-ttu-id="dd60c-143">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dd60c-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="dd60c-144">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dd60c-144">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="dd60c-145">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dd60c-145">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="dd60c-146">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dd60c-146">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="dd60c-147">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dd60c-147">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="dd60c-148">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dd60c-148">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


