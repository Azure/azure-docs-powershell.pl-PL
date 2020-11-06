---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 16b2c8df737047619366ebf6b75a4c2ed2264fdc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550436"
---
# <span data-ttu-id="b5bf3-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b5bf3-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="b5bf3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="b5bf3-103">Umożliwia ustawienie planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="b5bf3-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5bf3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5bf3-104">SYNTAX</span></span>

### <span data-ttu-id="b5bf3-105">S1</span><span class="sxs-lookup"><span data-stu-id="b5bf3-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5bf3-106">S2</span><span class="sxs-lookup"><span data-stu-id="b5bf3-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5bf3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b5bf3-107">DESCRIPTION</span></span>
<span data-ttu-id="b5bf3-108">Polecenie cmdlet **Set-AzureRmAppServicePlan** określa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="b5bf3-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="b5bf3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5bf3-109">EXAMPLES</span></span>

### <span data-ttu-id="b5bf3-110">1: modyfikowanie planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="b5bf3-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="b5bf3-111">To polecenie ustawia opcję PerSiteScaling na wartość prawda w planie usługi App Service o nazwie ContosoASP należącego do grupy zasobów o nazwie Default-Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="b5bf3-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b5bf3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5bf3-112">PARAMETERS</span></span>

### <span data-ttu-id="b5bf3-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="b5bf3-113">-AdminSiteName</span></span>
<span data-ttu-id="b5bf3-114">Nazwa witryny administracyjnej</span><span class="sxs-lookup"><span data-stu-id="b5bf3-114">Admin Site Name</span></span>

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

### <span data-ttu-id="b5bf3-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b5bf3-115">-AppServicePlan</span></span>
<span data-ttu-id="b5bf3-116">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="b5bf3-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="b5bf3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5bf3-117">-DefaultProfile</span></span>
<span data-ttu-id="b5bf3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5bf3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5bf3-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5bf3-119">-Name</span></span>
<span data-ttu-id="b5bf3-120">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="b5bf3-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="b5bf3-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="b5bf3-121">-NumberofWorkers</span></span>
<span data-ttu-id="b5bf3-122">Liczba pracowników</span><span class="sxs-lookup"><span data-stu-id="b5bf3-122">Number Of Workers</span></span>

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

### <span data-ttu-id="b5bf3-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="b5bf3-123">-PerSiteScaling</span></span>
<span data-ttu-id="b5bf3-124">Wartość logiczna skalowania dla witryny</span><span class="sxs-lookup"><span data-stu-id="b5bf3-124">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="b5bf3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5bf3-125">-ResourceGroupName</span></span>
<span data-ttu-id="b5bf3-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b5bf3-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b5bf3-127">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="b5bf3-127">-Tier</span></span>
<span data-ttu-id="b5bf3-128">Trójwarstwowej</span><span class="sxs-lookup"><span data-stu-id="b5bf3-128">Tier</span></span>

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

### <span data-ttu-id="b5bf3-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="b5bf3-129">-WorkerSize</span></span>
<span data-ttu-id="b5bf3-130">Rozmiar pracownika</span><span class="sxs-lookup"><span data-stu-id="b5bf3-130">Worker Size</span></span>

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
### <span data-ttu-id="b5bf3-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5bf3-131">-AsJob</span></span>
<span data-ttu-id="b5bf3-132">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b5bf3-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5bf3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5bf3-133">CommonParameters</span></span>
<span data-ttu-id="b5bf3-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5bf3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5bf3-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5bf3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5bf3-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5bf3-136">INPUTS</span></span>

### <span data-ttu-id="b5bf3-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="b5bf3-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="b5bf3-138">Parametr "AppServicePlan" akceptuje wartość typu "ServerFarmWithRichSku" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="b5bf3-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="b5bf3-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5bf3-139">OUTPUTS</span></span>

### <span data-ttu-id="b5bf3-140">Microsoft. Azure. Management. Web. MODELES. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="b5bf3-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="b5bf3-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5bf3-141">NOTES</span></span>

## <span data-ttu-id="b5bf3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5bf3-142">RELATED LINKS</span></span>

[<span data-ttu-id="b5bf3-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b5bf3-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="b5bf3-144">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b5bf3-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="b5bf3-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b5bf3-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="b5bf3-146">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b5bf3-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="b5bf3-147">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b5bf3-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="b5bf3-148">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b5bf3-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


