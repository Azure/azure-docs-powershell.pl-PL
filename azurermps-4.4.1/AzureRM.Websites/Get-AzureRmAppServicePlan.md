---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
ms.openlocfilehash: 9cadc32a34f94a29221984e25141bcc3a844de4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717549"
---
# <span data-ttu-id="f6a8c-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f6a8c-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="f6a8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a8c-103">Pobiera plan usługi aplikacji platformy Azure w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6a8c-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6a8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6a8c-104">SYNTAX</span></span>

### <span data-ttu-id="f6a8c-105">S1</span><span class="sxs-lookup"><span data-stu-id="f6a8c-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6a8c-106">S2</span><span class="sxs-lookup"><span data-stu-id="f6a8c-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6a8c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f6a8c-107">DESCRIPTION</span></span>
<span data-ttu-id="f6a8c-108">Polecenie cmdlet **Get-AzureRmAppServicePlan** pobiera plan usługi Azure App Service w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6a8c-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="f6a8c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6a8c-109">EXAMPLES</span></span>

### <span data-ttu-id="f6a8c-110">Przykład 1: pobieranie planu usługi App Service z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f6a8c-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="f6a8c-111">To polecenie pobiera plan usługi App Service (o nazwie ContosoASP) należący do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="f6a8c-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="f6a8c-112">Przykład 2: pobieranie wszystkich planów usługi App Service w lokalizacji</span><span class="sxs-lookup"><span data-stu-id="f6a8c-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="f6a8c-113">To polecenie pobiera wszystkie plany usługi App Service, które znajdują się w regionie "Zachodnia USA".</span><span class="sxs-lookup"><span data-stu-id="f6a8c-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="f6a8c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6a8c-114">PARAMETERS</span></span>

### <span data-ttu-id="f6a8c-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f6a8c-115">-Location</span></span>
<span data-ttu-id="f6a8c-116">Pozycję</span><span class="sxs-lookup"><span data-stu-id="f6a8c-116">Location</span></span> 

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

### <span data-ttu-id="f6a8c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f6a8c-117">-Name</span></span>
<span data-ttu-id="f6a8c-118">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="f6a8c-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="f6a8c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a8c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f6a8c-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f6a8c-120">Resource Group Name</span></span>

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

### <span data-ttu-id="f6a8c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a8c-121">-DefaultProfile</span></span>
<span data-ttu-id="f6a8c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a8c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6a8c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a8c-123">CommonParameters</span></span>
<span data-ttu-id="f6a8c-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6a8c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a8c-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a8c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a8c-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6a8c-126">INPUTS</span></span>

## <span data-ttu-id="f6a8c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6a8c-127">OUTPUTS</span></span>

### <span data-ttu-id="f6a8c-128">Microsoft. Azure. Management. Web. MODELES. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="f6a8c-128">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="f6a8c-129">Microsoft. Azure. Management. Web. MODELES. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="f6a8c-129">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="f6a8c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6a8c-130">NOTES</span></span>

## <span data-ttu-id="f6a8c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6a8c-131">RELATED LINKS</span></span>

[<span data-ttu-id="f6a8c-132">Nowe — AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f6a8c-132">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="f6a8c-133">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f6a8c-133">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="f6a8c-134">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f6a8c-134">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


