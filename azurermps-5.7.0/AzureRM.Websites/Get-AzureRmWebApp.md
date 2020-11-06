---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 55bce35d7aa0cc3c2cff905020159f9ba204a48a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550448"
---
# <span data-ttu-id="8c09b-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8c09b-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="8c09b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c09b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c09b-103">Pobiera aplikacje sieci Web platformy Azure w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c09b-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c09b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c09b-104">SYNTAX</span></span>

### <span data-ttu-id="8c09b-105">S1</span><span class="sxs-lookup"><span data-stu-id="8c09b-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c09b-106">S2</span><span class="sxs-lookup"><span data-stu-id="8c09b-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c09b-107">S3</span><span class="sxs-lookup"><span data-stu-id="8c09b-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c09b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8c09b-108">DESCRIPTION</span></span>
<span data-ttu-id="8c09b-109">Polecenie cmdlet **Get-AzureRmWebApp** pobiera informacje o aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8c09b-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="8c09b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c09b-110">EXAMPLES</span></span>

### <span data-ttu-id="8c09b-111">Przykład 1: uzyskiwanie aplikacji sieci Web z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8c09b-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="8c09b-112">To polecenie umożliwia wyświetlenie aplikacji sieci Web o nazwie ContosoSite należącej do obszaru domyślnego Grupa zasobów — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="8c09b-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8c09b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c09b-113">PARAMETERS</span></span>

### <span data-ttu-id="8c09b-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c09b-114">-AppServicePlan</span></span>
<span data-ttu-id="8c09b-115">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="8c09b-115">App Service Plan object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c09b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c09b-116">-DefaultProfile</span></span>
<span data-ttu-id="8c09b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c09b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c09b-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8c09b-118">-Location</span></span>
<span data-ttu-id="8c09b-119">Pozycję</span><span class="sxs-lookup"><span data-stu-id="8c09b-119">Location</span></span>

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

### <span data-ttu-id="8c09b-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c09b-120">-Name</span></span>
<span data-ttu-id="8c09b-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="8c09b-121">WebApp Name</span></span>

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

### <span data-ttu-id="8c09b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c09b-122">-ResourceGroupName</span></span>
<span data-ttu-id="8c09b-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8c09b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="8c09b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c09b-124">CommonParameters</span></span>
<span data-ttu-id="8c09b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c09b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c09b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c09b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c09b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c09b-127">INPUTS</span></span>

### <span data-ttu-id="8c09b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8c09b-128">System.String</span></span>

## <span data-ttu-id="8c09b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c09b-129">OUTPUTS</span></span>

### <span data-ttu-id="8c09b-130">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="8c09b-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="8c09b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c09b-131">NOTES</span></span>

## <span data-ttu-id="8c09b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c09b-132">RELATED LINKS</span></span>

[<span data-ttu-id="8c09b-133">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8c09b-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="8c09b-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8c09b-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="8c09b-135">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8c09b-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="8c09b-136">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8c09b-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="8c09b-137">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8c09b-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


