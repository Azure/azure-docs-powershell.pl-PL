---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 84cc6f2e8e51de6176b4ab8a04296aab8516a967
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989479"
---
# <span data-ttu-id="d9c05-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="d9c05-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="d9c05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9c05-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c05-103">Pobiera listę lokalizacji usługi komunikacji równorzędnej oferowanych przez firmę Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d9c05-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="d9c05-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9c05-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9c05-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9c05-105">DESCRIPTION</span></span>
<span data-ttu-id="d9c05-106">Lista lokalizacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="d9c05-106">List peering locations.</span></span>

## <span data-ttu-id="d9c05-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9c05-107">EXAMPLES</span></span>

### <span data-ttu-id="d9c05-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9c05-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="d9c05-109">Pobiera lokalizacje komunikacji równorzędnej dla elementu washington.</span><span class="sxs-lookup"><span data-stu-id="d9c05-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="d9c05-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d9c05-110">Example 2</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States"

Country     : United States
State       : Alabama
AzureRegion : East US
Name        : Alabama
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

Country     : United States
State       : Arizona
AzureRegion : West US
Name        : Arizona
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

...
```

<span data-ttu-id="d9c05-111">Pobiera lokalizacje komunikacji równorzędnej dla elementu washington.</span><span class="sxs-lookup"><span data-stu-id="d9c05-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="d9c05-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9c05-112">PARAMETERS</span></span>

### <span data-ttu-id="d9c05-113">— Kraj</span><span class="sxs-lookup"><span data-stu-id="d9c05-113">-Country</span></span>
<span data-ttu-id="d9c05-114">Filtr kraju</span><span class="sxs-lookup"><span data-stu-id="d9c05-114">The country filter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c05-115">-DefaultProfile</span></span>
<span data-ttu-id="d9c05-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9c05-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c05-117">CommonParameters</span></span>
<span data-ttu-id="d9c05-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c05-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c05-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9c05-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c05-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9c05-120">INPUTS</span></span>

### <span data-ttu-id="d9c05-121">Brak</span><span class="sxs-lookup"><span data-stu-id="d9c05-121">None</span></span>

## <span data-ttu-id="d9c05-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9c05-122">OUTPUTS</span></span>

### <span data-ttu-id="d9c05-123">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="d9c05-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="d9c05-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9c05-124">NOTES</span></span>

## <span data-ttu-id="d9c05-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9c05-125">RELATED LINKS</span></span>
