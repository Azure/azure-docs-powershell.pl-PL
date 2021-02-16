---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179178"
---
# <span data-ttu-id="913a6-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="913a6-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="913a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="913a6-102">SYNOPSIS</span></span>
<span data-ttu-id="913a6-103">Pobiera listę lokalizacji usługi komunikacji równorzędnej oferowanych przez firmę Microsoft.</span><span class="sxs-lookup"><span data-stu-id="913a6-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="913a6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="913a6-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="913a6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="913a6-105">DESCRIPTION</span></span>
<span data-ttu-id="913a6-106">Lista lokalizacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="913a6-106">List peering locations.</span></span>

## <span data-ttu-id="913a6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="913a6-107">EXAMPLES</span></span>

### <span data-ttu-id="913a6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="913a6-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="913a6-109">Pobiera lokalizacje komunikacji równorzędnej dla elementu washington.</span><span class="sxs-lookup"><span data-stu-id="913a6-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="913a6-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="913a6-110">Example 2</span></span>
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

<span data-ttu-id="913a6-111">Pobiera lokalizacje komunikacji równorzędnej dla elementu washington.</span><span class="sxs-lookup"><span data-stu-id="913a6-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="913a6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="913a6-112">PARAMETERS</span></span>

### <span data-ttu-id="913a6-113">— Kraj</span><span class="sxs-lookup"><span data-stu-id="913a6-113">-Country</span></span>
<span data-ttu-id="913a6-114">Filtr kraju</span><span class="sxs-lookup"><span data-stu-id="913a6-114">The country filter</span></span>

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

### <span data-ttu-id="913a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913a6-115">-DefaultProfile</span></span>
<span data-ttu-id="913a6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="913a6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="913a6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913a6-117">CommonParameters</span></span>
<span data-ttu-id="913a6-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="913a6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913a6-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="913a6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913a6-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="913a6-120">INPUTS</span></span>

### <span data-ttu-id="913a6-121">Brak</span><span class="sxs-lookup"><span data-stu-id="913a6-121">None</span></span>

## <span data-ttu-id="913a6-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="913a6-122">OUTPUTS</span></span>

### <span data-ttu-id="913a6-123">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="913a6-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="913a6-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="913a6-124">NOTES</span></span>

## <span data-ttu-id="913a6-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="913a6-125">RELATED LINKS</span></span>
