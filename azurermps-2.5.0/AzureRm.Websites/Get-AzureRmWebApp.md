---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: eb1f96eaf85e6a5e7234e09c319b2e0c1117d456
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897213"
---
# <span data-ttu-id="3e67c-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3e67c-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="3e67c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e67c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e67c-103">Pobiera aplikacje sieci Web platformy Azure w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e67c-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e67c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e67c-104">SYNTAX</span></span>

### <span data-ttu-id="3e67c-105">S1</span><span class="sxs-lookup"><span data-stu-id="3e67c-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e67c-106">S2</span><span class="sxs-lookup"><span data-stu-id="3e67c-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e67c-107">S3</span><span class="sxs-lookup"><span data-stu-id="3e67c-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e67c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3e67c-108">DESCRIPTION</span></span>
<span data-ttu-id="3e67c-109">Polecenie cmdlet **Get-AzureRmWebApp** pobiera informacje o aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="3e67c-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="3e67c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e67c-110">EXAMPLES</span></span>

### <span data-ttu-id="3e67c-111">Przykład 1: uzyskiwanie aplikacji sieci Web z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3e67c-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="3e67c-112">To polecenie umożliwia wyświetlenie aplikacji sieci Web o nazwie ContosoSite należącej do obszaru domyślnego Grupa zasobów — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="3e67c-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="3e67c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e67c-113">PARAMETERS</span></span>

### <span data-ttu-id="3e67c-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3e67c-114">-AppServicePlan</span></span>
<span data-ttu-id="3e67c-115">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="3e67c-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e67c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e67c-116">-DefaultProfile</span></span>
<span data-ttu-id="3e67c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e67c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e67c-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3e67c-118">-Location</span></span>
<span data-ttu-id="3e67c-119">Pozycję</span><span class="sxs-lookup"><span data-stu-id="3e67c-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e67c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e67c-120">-Name</span></span>
<span data-ttu-id="3e67c-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="3e67c-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e67c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e67c-122">-ResourceGroupName</span></span>
<span data-ttu-id="3e67c-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3e67c-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e67c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e67c-124">CommonParameters</span></span>
<span data-ttu-id="3e67c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e67c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e67c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e67c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e67c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e67c-127">INPUTS</span></span>

### <span data-ttu-id="3e67c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3e67c-128">System.String</span></span>

## <span data-ttu-id="3e67c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e67c-129">OUTPUTS</span></span>

### <span data-ttu-id="3e67c-130">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="3e67c-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="3e67c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e67c-131">NOTES</span></span>

## <span data-ttu-id="3e67c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e67c-132">RELATED LINKS</span></span>

[<span data-ttu-id="3e67c-133">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3e67c-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="3e67c-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3e67c-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="3e67c-135">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3e67c-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="3e67c-136">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3e67c-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="3e67c-137">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3e67c-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


