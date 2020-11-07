---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: e8fe8fb59ee56e457c49d959c07db08cad62bb5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868420"
---
# <span data-ttu-id="55b7f-101">Get-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="55b7f-101">Get-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="55b7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="55b7f-103">Pobierz zasady WAF</span><span class="sxs-lookup"><span data-stu-id="55b7f-103">Get WAF policy</span></span>

## <span data-ttu-id="55b7f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55b7f-104">SYNTAX</span></span>

```
Get-AzFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55b7f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="55b7f-105">DESCRIPTION</span></span>
<span data-ttu-id="55b7f-106">**AzFrontDoorFireWallPolicy** cmdletGet pobiera zasady WAF w grupie zasobów w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="55b7f-106">The **Get-AzFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="55b7f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55b7f-107">EXAMPLES</span></span>

### <span data-ttu-id="55b7f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="55b7f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="55b7f-109">Uzyskaj zasady WAF o nazwie $policyName w $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b7f-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="55b7f-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="55b7f-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="55b7f-111">Pobierz wszystkie zasady WAF w $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b7f-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="55b7f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55b7f-112">PARAMETERS</span></span>

### <span data-ttu-id="55b7f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b7f-113">-DefaultProfile</span></span>
<span data-ttu-id="55b7f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55b7f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55b7f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="55b7f-115">-Name</span></span>
<span data-ttu-id="55b7f-116">Nazwa FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="55b7f-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="55b7f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b7f-117">-ResourceGroupName</span></span>
<span data-ttu-id="55b7f-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="55b7f-118">The resource group name.</span></span>

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

### <span data-ttu-id="55b7f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b7f-119">CommonParameters</span></span>
<span data-ttu-id="55b7f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55b7f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b7f-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55b7f-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b7f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55b7f-122">INPUTS</span></span>

### <span data-ttu-id="55b7f-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="55b7f-123">None</span></span>

## <span data-ttu-id="55b7f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55b7f-124">OUTPUTS</span></span>

### <span data-ttu-id="55b7f-125">Microsoft. Azure. Commands. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="55b7f-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="55b7f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55b7f-126">NOTES</span></span>

## <span data-ttu-id="55b7f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55b7f-127">RELATED LINKS</span></span>

<span data-ttu-id="55b7f-128">[Nowe — AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="55b7f-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)</span></span>
