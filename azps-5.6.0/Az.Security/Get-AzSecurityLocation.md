---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: b835113b07fb2295193b89fd817ba82ceca71655
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995954"
---
# <span data-ttu-id="d5476-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="d5476-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="d5476-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5476-102">SYNOPSIS</span></span>
<span data-ttu-id="d5476-103">Pobiera lokalizację, w której Usługa Azure Security Center będzie automatycznie zapisywać dane dla określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d5476-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="d5476-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d5476-104">SYNTAX</span></span>

### <span data-ttu-id="d5476-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d5476-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5476-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d5476-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5476-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5476-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5476-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d5476-108">DESCRIPTION</span></span>
<span data-ttu-id="d5476-109">Centrum zabezpieczeń Azure automatycznie wybierze lokalizację zapisu części danych.</span><span class="sxs-lookup"><span data-stu-id="d5476-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="d5476-110">Użyj tego polecenia cmdlet, aby odnaleźć tę lokalizację.</span><span class="sxs-lookup"><span data-stu-id="d5476-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="d5476-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d5476-111">EXAMPLES</span></span>

### <span data-ttu-id="d5476-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d5476-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="d5476-113">Pobiera lokalizację, w której Usługa Azure Security Center zapisuje obliczone dane zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="d5476-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="d5476-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5476-114">PARAMETERS</span></span>

### <span data-ttu-id="d5476-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5476-115">-DefaultProfile</span></span>
<span data-ttu-id="d5476-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5476-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5476-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d5476-117">-Name</span></span>
<span data-ttu-id="d5476-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="d5476-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5476-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5476-119">-ResourceId</span></span>
<span data-ttu-id="d5476-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d5476-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5476-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5476-121">CommonParameters</span></span>
<span data-ttu-id="d5476-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5476-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5476-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5476-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5476-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5476-124">INPUTS</span></span>

### <span data-ttu-id="d5476-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d5476-125">System.String</span></span>

## <span data-ttu-id="d5476-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5476-126">OUTPUTS</span></span>

### <span data-ttu-id="d5476-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="d5476-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="d5476-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d5476-128">NOTES</span></span>

## <span data-ttu-id="d5476-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5476-129">RELATED LINKS</span></span>
