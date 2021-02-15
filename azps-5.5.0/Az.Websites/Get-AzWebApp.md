---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 7dc1d2c5d6be1fd920ec9fb4eb90bf73b2c464b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182467"
---
# <span data-ttu-id="a74e3-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a74e3-101">Get-AzWebApp</span></span>

## <span data-ttu-id="a74e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a74e3-102">SYNOPSIS</span></span>
<span data-ttu-id="a74e3-103">Pobiera aplikacje Azure Web Apps do określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a74e3-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="a74e3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a74e3-104">SYNTAX</span></span>

### <span data-ttu-id="a74e3-105">S1</span><span class="sxs-lookup"><span data-stu-id="a74e3-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a74e3-106">S2</span><span class="sxs-lookup"><span data-stu-id="a74e3-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a74e3-107">S3</span><span class="sxs-lookup"><span data-stu-id="a74e3-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a74e3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a74e3-108">DESCRIPTION</span></span>
<span data-ttu-id="a74e3-109">Polecenie **cmdlet Get-AzWebApp** pobiera informacje o aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a74e3-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="a74e3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a74e3-110">EXAMPLES</span></span>

### <span data-ttu-id="a74e3-111">Przykład 1. Uzyskiwanie aplikacji Sieci Web z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a74e3-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="a74e3-112">To polecenie pobiera aplikację Sieci Web o nazwie ContosoSite należącą do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="a74e3-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a74e3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a74e3-113">PARAMETERS</span></span>

### <span data-ttu-id="a74e3-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a74e3-114">-AppServicePlan</span></span>
<span data-ttu-id="a74e3-115">Obiekt Plan usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="a74e3-115">App Service Plan object</span></span>

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

### <span data-ttu-id="a74e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74e3-116">-DefaultProfile</span></span>
<span data-ttu-id="a74e3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a74e3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a74e3-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a74e3-118">-Location</span></span>
<span data-ttu-id="a74e3-119">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a74e3-119">Location</span></span>

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

### <span data-ttu-id="a74e3-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a74e3-120">-Name</span></span>
<span data-ttu-id="a74e3-121">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="a74e3-121">WebApp Name</span></span>

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

### <span data-ttu-id="a74e3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a74e3-122">-ResourceGroupName</span></span>
<span data-ttu-id="a74e3-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a74e3-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a74e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74e3-124">CommonParameters</span></span>
<span data-ttu-id="a74e3-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a74e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74e3-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a74e3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74e3-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a74e3-127">INPUTS</span></span>

### <span data-ttu-id="a74e3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a74e3-128">System.String</span></span>

## <span data-ttu-id="a74e3-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a74e3-129">OUTPUTS</span></span>

### <span data-ttu-id="a74e3-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a74e3-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a74e3-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a74e3-131">NOTES</span></span>

## <span data-ttu-id="a74e3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a74e3-132">RELATED LINKS</span></span>

[<span data-ttu-id="a74e3-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a74e3-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="a74e3-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a74e3-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="a74e3-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a74e3-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="a74e3-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a74e3-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="a74e3-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a74e3-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


