---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 4b6270a6d56b8f210b2f03311bf19bb09950f361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528170"
---
# <span data-ttu-id="a8a09-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a8a09-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="a8a09-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8a09-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a09-103">Umożliwia ustawienie planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="a8a09-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8a09-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8a09-104">SYNTAX</span></span>

### <span data-ttu-id="a8a09-105">S1</span><span class="sxs-lookup"><span data-stu-id="a8a09-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8a09-106">S2</span><span class="sxs-lookup"><span data-stu-id="a8a09-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8a09-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a8a09-107">DESCRIPTION</span></span>
<span data-ttu-id="a8a09-108">Polecenie cmdlet **Set-AzureRmAppServicePlan** określa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="a8a09-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="a8a09-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8a09-109">EXAMPLES</span></span>

### <span data-ttu-id="a8a09-110">1: modyfikowanie planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="a8a09-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="a8a09-111">To polecenie ustawia opcję PerSiteScaling na wartość prawda w planie usługi App Service o nazwie ContosoASP należącego do grupy zasobów o nazwie Default-Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="a8a09-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a8a09-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8a09-112">PARAMETERS</span></span>

### <span data-ttu-id="a8a09-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="a8a09-113">-AdminSiteName</span></span>
<span data-ttu-id="a8a09-114">Nazwa witryny administracyjnej</span><span class="sxs-lookup"><span data-stu-id="a8a09-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a09-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a8a09-115">-AppServicePlan</span></span>
<span data-ttu-id="a8a09-116">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="a8a09-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="a8a09-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a8a09-117">-Name</span></span>
<span data-ttu-id="a8a09-118">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="a8a09-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="a8a09-119">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="a8a09-119">-NumberofWorkers</span></span>
<span data-ttu-id="a8a09-120">Liczba pracowników</span><span class="sxs-lookup"><span data-stu-id="a8a09-120">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a09-121">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="a8a09-121">-PerSiteScaling</span></span>
<span data-ttu-id="a8a09-122">Wartość logiczna skalowania dla witryny</span><span class="sxs-lookup"><span data-stu-id="a8a09-122">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a09-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8a09-123">-ResourceGroupName</span></span>
<span data-ttu-id="a8a09-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a8a09-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a8a09-125">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="a8a09-125">-Tier</span></span>
<span data-ttu-id="a8a09-126">Trójwarstwowej</span><span class="sxs-lookup"><span data-stu-id="a8a09-126">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a09-127">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="a8a09-127">-WorkerSize</span></span>
<span data-ttu-id="a8a09-128">Rozmiar pracownika</span><span class="sxs-lookup"><span data-stu-id="a8a09-128">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8a09-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8a09-129">-DefaultProfile</span></span>
<span data-ttu-id="a8a09-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8a09-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8a09-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a09-131">CommonParameters</span></span>
<span data-ttu-id="a8a09-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8a09-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a09-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8a09-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a09-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8a09-134">INPUTS</span></span>

### <span data-ttu-id="a8a09-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="a8a09-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="a8a09-136">Parametr "AppServicePlan" akceptuje wartość typu "ServerFarmWithRichSku" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="a8a09-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="a8a09-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8a09-137">OUTPUTS</span></span>

### <span data-ttu-id="a8a09-138">Microsoft. Azure. Management. Web. MODELES. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="a8a09-138">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="a8a09-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8a09-139">NOTES</span></span>

## <span data-ttu-id="a8a09-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8a09-140">RELATED LINKS</span></span>

[<span data-ttu-id="a8a09-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a8a09-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="a8a09-142">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a8a09-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="a8a09-143">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a8a09-143">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="a8a09-144">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a8a09-144">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="a8a09-145">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a8a09-145">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="a8a09-146">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a8a09-146">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


