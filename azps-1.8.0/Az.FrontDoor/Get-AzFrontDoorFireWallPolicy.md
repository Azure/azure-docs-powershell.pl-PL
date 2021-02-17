---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 5933d860ca2badce2d9576409dd1553153bb1e84
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401508"
---
# <span data-ttu-id="78cb7-101">Get-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="78cb7-101">Get-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="78cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="78cb7-103">Pobierz zasady dotyczące plików WAF</span><span class="sxs-lookup"><span data-stu-id="78cb7-103">Get WAF policy</span></span>

## <span data-ttu-id="78cb7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="78cb7-104">SYNTAX</span></span>

```
Get-AzFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78cb7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="78cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="78cb7-106">Polecenie **cmdlet Get-AzFrontDoorFireWallPolicy** pobiera zasady WAF w grupie zasobów w ramach bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="78cb7-106">The **Get-AzFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="78cb7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="78cb7-107">EXAMPLES</span></span>

### <span data-ttu-id="78cb7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="78cb7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="78cb7-109">Uzyskiwanie zasad WAF nazywanych $policyName w $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78cb7-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="78cb7-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="78cb7-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="78cb7-111">Pobierz wszystkie zasady WAF w programie $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78cb7-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="78cb7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78cb7-112">PARAMETERS</span></span>

### <span data-ttu-id="78cb7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78cb7-113">-DefaultProfile</span></span>
<span data-ttu-id="78cb7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="78cb7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78cb7-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="78cb7-115">-Name</span></span>
<span data-ttu-id="78cb7-116">Nazwa FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="78cb7-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="78cb7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78cb7-117">-ResourceGroupName</span></span>
<span data-ttu-id="78cb7-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78cb7-118">The resource group name.</span></span>

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

### <span data-ttu-id="78cb7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78cb7-119">CommonParameters</span></span>
<span data-ttu-id="78cb7-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78cb7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78cb7-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78cb7-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78cb7-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78cb7-122">INPUTS</span></span>

### <span data-ttu-id="78cb7-123">Brak</span><span class="sxs-lookup"><span data-stu-id="78cb7-123">None</span></span>

## <span data-ttu-id="78cb7-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78cb7-124">OUTPUTS</span></span>

### <span data-ttu-id="78cb7-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="78cb7-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="78cb7-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="78cb7-126">NOTES</span></span>

## <span data-ttu-id="78cb7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78cb7-127">RELATED LINKS</span></span>

<span data-ttu-id="78cb7-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="78cb7-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span></span>
