---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 77f9283b16aa605da066780165c2fe7b42b1830b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503041"
---
# <span data-ttu-id="a3b66-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="a3b66-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="a3b66-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3b66-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b66-103">Pobiera lokalizację, w której usługa Azure Security Center będzie automatycznie zapisywać dane dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a3b66-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="a3b66-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3b66-104">SYNTAX</span></span>

### <span data-ttu-id="a3b66-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a3b66-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3b66-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a3b66-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3b66-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="a3b66-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3b66-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a3b66-108">DESCRIPTION</span></span>
<span data-ttu-id="a3b66-109">Usługa Azure Security Center automatycznie zdecyduje w lokalizacji, w której będą zapisywane niektóre dane.</span><span class="sxs-lookup"><span data-stu-id="a3b66-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="a3b66-110">Użyj tego polecenia cmdlet, aby wykryć lokalizację.</span><span class="sxs-lookup"><span data-stu-id="a3b66-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="a3b66-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3b66-111">EXAMPLES</span></span>

### <span data-ttu-id="a3b66-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3b66-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="a3b66-113">Pobiera lokalizację, w której usługa Azure Security Center zapisuje obliczone dane zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="a3b66-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="a3b66-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3b66-114">PARAMETERS</span></span>

### <span data-ttu-id="a3b66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b66-115">-DefaultProfile</span></span>
<span data-ttu-id="a3b66-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3b66-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3b66-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3b66-117">-Name</span></span>
<span data-ttu-id="a3b66-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a3b66-118">Resource name.</span></span>

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

### <span data-ttu-id="a3b66-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3b66-119">-ResourceId</span></span>
<span data-ttu-id="a3b66-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a3b66-120">Resource ID.</span></span>

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

### <span data-ttu-id="a3b66-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b66-121">CommonParameters</span></span>
<span data-ttu-id="a3b66-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3b66-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b66-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3b66-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b66-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3b66-124">INPUTS</span></span>

### <span data-ttu-id="a3b66-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a3b66-125">System.String</span></span>

## <span data-ttu-id="a3b66-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3b66-126">OUTPUTS</span></span>

### <span data-ttu-id="a3b66-127">Microsoft. Azure. Commands. Security. MODELES. Locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="a3b66-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="a3b66-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3b66-128">NOTES</span></span>

## <span data-ttu-id="a3b66-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3b66-129">RELATED LINKS</span></span>
