---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: aaf0a476601db720674c4422f7e16edfaf0fa2ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872387"
---
# <span data-ttu-id="54426-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="54426-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="54426-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54426-102">SYNOPSIS</span></span>
<span data-ttu-id="54426-103">Pobiera listę lokalizacji usług równorzędnych oferowanych przez firmę Microsoft.</span><span class="sxs-lookup"><span data-stu-id="54426-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="54426-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54426-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54426-105">Opis</span><span class="sxs-lookup"><span data-stu-id="54426-105">DESCRIPTION</span></span>
<span data-ttu-id="54426-106">Wyświetlanie listy lokalizacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="54426-106">List peering locations.</span></span>

## <span data-ttu-id="54426-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54426-107">EXAMPLES</span></span>

### <span data-ttu-id="54426-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="54426-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="54426-109">Pobiera lokalizacje równorzędne dla Waszyngton.</span><span class="sxs-lookup"><span data-stu-id="54426-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="54426-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="54426-110">Example 2</span></span>
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

<span data-ttu-id="54426-111">Pobiera lokalizacje równorzędne dla Waszyngton.</span><span class="sxs-lookup"><span data-stu-id="54426-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="54426-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54426-112">PARAMETERS</span></span>

### <span data-ttu-id="54426-113">-Country</span><span class="sxs-lookup"><span data-stu-id="54426-113">-Country</span></span>
<span data-ttu-id="54426-114">Filtr kraju</span><span class="sxs-lookup"><span data-stu-id="54426-114">The country filter</span></span>

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

### <span data-ttu-id="54426-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54426-115">-DefaultProfile</span></span>
<span data-ttu-id="54426-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="54426-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54426-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54426-117">CommonParameters</span></span>
<span data-ttu-id="54426-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54426-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54426-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54426-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54426-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54426-120">INPUTS</span></span>

### <span data-ttu-id="54426-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="54426-121">None</span></span>

## <span data-ttu-id="54426-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54426-122">OUTPUTS</span></span>

### <span data-ttu-id="54426-123">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="54426-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="54426-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54426-124">NOTES</span></span>

## <span data-ttu-id="54426-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54426-125">RELATED LINKS</span></span>
