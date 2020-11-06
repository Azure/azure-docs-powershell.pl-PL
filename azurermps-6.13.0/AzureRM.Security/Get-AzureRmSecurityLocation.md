---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
ms.openlocfilehash: 034681ad8ce4fbd30b10b959eda024f1a375c366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526042"
---
# <span data-ttu-id="bc4e9-101">Get-AzureRmSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="bc4e9-101">Get-AzureRmSecurityLocation</span></span>

## <span data-ttu-id="bc4e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc4e9-102">SYNOPSIS</span></span>
<span data-ttu-id="bc4e9-103">Pobiera lokalizację, w której usługa Azure Security Center będzie automatycznie zapisywać dane dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bc4e9-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc4e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc4e9-104">SYNTAX</span></span>

### <span data-ttu-id="bc4e9-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bc4e9-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc4e9-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="bc4e9-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc4e9-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="bc4e9-107">ResourceId</span></span>
```
Get-AzureRmSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc4e9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bc4e9-108">DESCRIPTION</span></span>
<span data-ttu-id="bc4e9-109">Usługa Azure Security Center automatycznie zdecyduje w lokalizacji, w której będą zapisywane niektóre dane.</span><span class="sxs-lookup"><span data-stu-id="bc4e9-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="bc4e9-110">Użyj tego polecenia cmdlet, aby wykryć lokalizację.</span><span class="sxs-lookup"><span data-stu-id="bc4e9-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="bc4e9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc4e9-111">EXAMPLES</span></span>

### <span data-ttu-id="bc4e9-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bc4e9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="bc4e9-113">Pobiera lokalizację, w której usługa Azure Security Center zapisuje obliczone dane zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="bc4e9-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="bc4e9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc4e9-114">PARAMETERS</span></span>

### <span data-ttu-id="bc4e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc4e9-115">-DefaultProfile</span></span>
<span data-ttu-id="bc4e9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc4e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc4e9-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bc4e9-117">-Name</span></span>
<span data-ttu-id="bc4e9-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="bc4e9-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4e9-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc4e9-119">-ResourceId</span></span>
<span data-ttu-id="bc4e9-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="bc4e9-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc4e9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc4e9-121">CommonParameters</span></span>
<span data-ttu-id="bc4e9-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc4e9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc4e9-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc4e9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc4e9-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc4e9-124">INPUTS</span></span>

### <span data-ttu-id="bc4e9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bc4e9-125">System.String</span></span>

## <span data-ttu-id="bc4e9-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc4e9-126">OUTPUTS</span></span>

### <span data-ttu-id="bc4e9-127">Microsoft. Azure. Commands. Security. MODELES. Locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="bc4e9-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="bc4e9-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc4e9-128">NOTES</span></span>

## <span data-ttu-id="bc4e9-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc4e9-129">RELATED LINKS</span></span>
