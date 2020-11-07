---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 64945cf503248fc0561dc894090c73d2d7151e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717546"
---
# <span data-ttu-id="5f7a0-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5f7a0-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="5f7a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f7a0-102">SYNOPSIS</span></span>
<span data-ttu-id="5f7a0-103">Pobiera aplikacje sieci Web platformy Azure w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f7a0-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f7a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f7a0-104">SYNTAX</span></span>

### <span data-ttu-id="5f7a0-105">S1</span><span class="sxs-lookup"><span data-stu-id="5f7a0-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f7a0-106">S2</span><span class="sxs-lookup"><span data-stu-id="5f7a0-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f7a0-107">S3</span><span class="sxs-lookup"><span data-stu-id="5f7a0-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f7a0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5f7a0-108">DESCRIPTION</span></span>
<span data-ttu-id="5f7a0-109">Polecenie cmdlet **Get-AzureRmWebApp** pobiera informacje o aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5f7a0-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="5f7a0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f7a0-110">EXAMPLES</span></span>

### <span data-ttu-id="5f7a0-111">Przykład 1: uzyskiwanie aplikacji sieci Web z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5f7a0-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -SlotName "Slot001"
```

<span data-ttu-id="5f7a0-112">To polecenie umożliwia wyświetlenie aplikacji sieci Web o nazwie ContosoSite należącej do obszaru domyślnego Grupa zasobów — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5f7a0-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5f7a0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f7a0-113">PARAMETERS</span></span>

### <span data-ttu-id="5f7a0-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5f7a0-114">-AppServicePlan</span></span>
<span data-ttu-id="5f7a0-115">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="5f7a0-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f7a0-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5f7a0-116">-Location</span></span>
<span data-ttu-id="5f7a0-117">Pozycję</span><span class="sxs-lookup"><span data-stu-id="5f7a0-117">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f7a0-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5f7a0-118">-Name</span></span>
<span data-ttu-id="5f7a0-119">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="5f7a0-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f7a0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f7a0-120">-ResourceGroupName</span></span>
<span data-ttu-id="5f7a0-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5f7a0-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f7a0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f7a0-122">-DefaultProfile</span></span>
<span data-ttu-id="5f7a0-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f7a0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f7a0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f7a0-124">CommonParameters</span></span>
<span data-ttu-id="5f7a0-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f7a0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f7a0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f7a0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f7a0-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f7a0-127">INPUTS</span></span>

## <span data-ttu-id="5f7a0-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f7a0-128">OUTPUTS</span></span>

## <span data-ttu-id="5f7a0-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f7a0-129">NOTES</span></span>

## <span data-ttu-id="5f7a0-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f7a0-130">RELATED LINKS</span></span>

[<span data-ttu-id="5f7a0-131">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5f7a0-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="5f7a0-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5f7a0-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="5f7a0-133">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5f7a0-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="5f7a0-134">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5f7a0-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="5f7a0-135">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5f7a0-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


