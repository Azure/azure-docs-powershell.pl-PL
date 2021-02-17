---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198202"
---
# <span data-ttu-id="b815d-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b815d-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="b815d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b815d-102">SYNOPSIS</span></span>
<span data-ttu-id="b815d-103">Pobierz regułę routingu dla nazwy danego miejsca.</span><span class="sxs-lookup"><span data-stu-id="b815d-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="b815d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b815d-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b815d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b815d-105">DESCRIPTION</span></span>
<span data-ttu-id="b815d-106">Polecenie **cmdlet Get-AzWebAppTrafficRouting** pobiera konfigurację reguły routingu z gniazda aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b815d-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="b815d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b815d-107">EXAMPLES</span></span>

### <span data-ttu-id="b815d-108">Przykład 1. Pobiera określoną regułę routingu z gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="b815d-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="b815d-109">To polecenie pobiera regułę routingu dla danego gniazda aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b815d-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="b815d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b815d-110">PARAMETERS</span></span>

### <span data-ttu-id="b815d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b815d-111">-DefaultProfile</span></span>
<span data-ttu-id="b815d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b815d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b815d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b815d-113">-ResourceGroupName</span></span>
<span data-ttu-id="b815d-114">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b815d-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b815d-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="b815d-115">-RuleName</span></span>
<span data-ttu-id="b815d-116">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="b815d-116">Rule Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b815d-117">- WebAppName</span><span class="sxs-lookup"><span data-stu-id="b815d-117">-WebAppName</span></span>
<span data-ttu-id="b815d-118">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="b815d-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b815d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b815d-119">CommonParameters</span></span>
<span data-ttu-id="b815d-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b815d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b815d-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b815d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b815d-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b815d-122">INPUTS</span></span>

### <span data-ttu-id="b815d-123">Brak</span><span class="sxs-lookup"><span data-stu-id="b815d-123">None</span></span>

## <span data-ttu-id="b815d-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b815d-124">OUTPUTS</span></span>

### <span data-ttu-id="b815d-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="b815d-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="b815d-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b815d-126">NOTES</span></span>

## <span data-ttu-id="b815d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b815d-127">RELATED LINKS</span></span>

[<span data-ttu-id="b815d-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b815d-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="b815d-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b815d-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="b815d-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b815d-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
