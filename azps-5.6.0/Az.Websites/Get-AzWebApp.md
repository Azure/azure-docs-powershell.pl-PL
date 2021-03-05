---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 32e71b33b3c440701e501c4b68d740dcf121001d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983882"
---
# <span data-ttu-id="55544-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="55544-101">Get-AzWebApp</span></span>

## <span data-ttu-id="55544-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55544-102">SYNOPSIS</span></span>
<span data-ttu-id="55544-103">Pobiera aplikacje Azure Web Apps do określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="55544-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="55544-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="55544-104">SYNTAX</span></span>

### <span data-ttu-id="55544-105">S1</span><span class="sxs-lookup"><span data-stu-id="55544-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55544-106">S2</span><span class="sxs-lookup"><span data-stu-id="55544-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55544-107">S3</span><span class="sxs-lookup"><span data-stu-id="55544-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55544-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="55544-108">DESCRIPTION</span></span>
<span data-ttu-id="55544-109">Polecenie **cmdlet Get-AzWebApp** pobiera informacje o aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="55544-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="55544-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="55544-110">EXAMPLES</span></span>

### <span data-ttu-id="55544-111">Przykład 1. Uzyskiwanie aplikacji Sieci Web z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="55544-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="55544-112">To polecenie pobiera nazwę aplikacji Sieci Web o nazwie ContosoSite należącą do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="55544-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="55544-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55544-113">PARAMETERS</span></span>

### <span data-ttu-id="55544-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="55544-114">-AppServicePlan</span></span>
<span data-ttu-id="55544-115">Obiekt App Service Plan</span><span class="sxs-lookup"><span data-stu-id="55544-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55544-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55544-116">-DefaultProfile</span></span>
<span data-ttu-id="55544-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="55544-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55544-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="55544-118">-Location</span></span>
<span data-ttu-id="55544-119">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="55544-119">Location</span></span>

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

### <span data-ttu-id="55544-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="55544-120">-Name</span></span>
<span data-ttu-id="55544-121">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="55544-121">WebApp Name</span></span>

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

### <span data-ttu-id="55544-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55544-122">-ResourceGroupName</span></span>
<span data-ttu-id="55544-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="55544-123">Resource Group Name</span></span>

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

### <span data-ttu-id="55544-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55544-124">CommonParameters</span></span>
<span data-ttu-id="55544-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55544-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55544-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55544-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55544-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55544-127">INPUTS</span></span>

### <span data-ttu-id="55544-128">System.String</span><span class="sxs-lookup"><span data-stu-id="55544-128">System.String</span></span>

## <span data-ttu-id="55544-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55544-129">OUTPUTS</span></span>

### <span data-ttu-id="55544-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="55544-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="55544-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="55544-131">NOTES</span></span>

## <span data-ttu-id="55544-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55544-132">RELATED LINKS</span></span>

[<span data-ttu-id="55544-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="55544-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="55544-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="55544-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="55544-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="55544-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="55544-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="55544-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="55544-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="55544-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


