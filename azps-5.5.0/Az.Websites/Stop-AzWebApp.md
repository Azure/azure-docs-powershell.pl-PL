---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197202"
---
# <span data-ttu-id="91b82-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="91b82-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="91b82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91b82-102">SYNOPSIS</span></span>
<span data-ttu-id="91b82-103">Zatrzymuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="91b82-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="91b82-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="91b82-104">SYNTAX</span></span>

### <span data-ttu-id="91b82-105">S1</span><span class="sxs-lookup"><span data-stu-id="91b82-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91b82-106">S2</span><span class="sxs-lookup"><span data-stu-id="91b82-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91b82-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="91b82-107">DESCRIPTION</span></span>
<span data-ttu-id="91b82-108">Polecenie **cmdlet Stop-AzWebApp** zatrzymuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="91b82-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="91b82-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="91b82-109">EXAMPLES</span></span>

### <span data-ttu-id="91b82-110">Przykład 1. Zatrzymywanie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="91b82-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="91b82-111">To polecenie zatrzymuje aplikację Sieci Web o nazwie ContosoWebApp należącą do grupy zasobów o nazwie Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="91b82-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="91b82-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91b82-112">PARAMETERS</span></span>

### <span data-ttu-id="91b82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b82-113">-DefaultProfile</span></span>
<span data-ttu-id="91b82-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="91b82-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91b82-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="91b82-115">-Name</span></span>
<span data-ttu-id="91b82-116">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="91b82-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b82-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b82-117">-ResourceGroupName</span></span>
<span data-ttu-id="91b82-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="91b82-118">Resource Group Name</span></span>

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

### <span data-ttu-id="91b82-119">- WebApp</span><span class="sxs-lookup"><span data-stu-id="91b82-119">-WebApp</span></span>
<span data-ttu-id="91b82-120">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="91b82-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91b82-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b82-121">CommonParameters</span></span>
<span data-ttu-id="91b82-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91b82-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b82-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91b82-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b82-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91b82-124">INPUTS</span></span>

### <span data-ttu-id="91b82-125">System.String</span><span class="sxs-lookup"><span data-stu-id="91b82-125">System.String</span></span>

### <span data-ttu-id="91b82-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="91b82-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="91b82-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="91b82-127">OUTPUTS</span></span>

### <span data-ttu-id="91b82-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="91b82-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="91b82-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="91b82-129">NOTES</span></span>

## <span data-ttu-id="91b82-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91b82-130">RELATED LINKS</span></span>

[<span data-ttu-id="91b82-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="91b82-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="91b82-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="91b82-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="91b82-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="91b82-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="91b82-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="91b82-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="91b82-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="91b82-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


