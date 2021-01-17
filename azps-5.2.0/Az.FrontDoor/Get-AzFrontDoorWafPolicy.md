---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ea1ace189271c96bbf4bda0bc67385c678ef3c40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350233"
---
# <span data-ttu-id="972e1-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="972e1-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="972e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="972e1-102">SYNOPSIS</span></span>
<span data-ttu-id="972e1-103">Pobierz zasady WAF</span><span class="sxs-lookup"><span data-stu-id="972e1-103">Get WAF policy</span></span>

## <span data-ttu-id="972e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="972e1-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="972e1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="972e1-105">DESCRIPTION</span></span>
<span data-ttu-id="972e1-106">**AzFrontDoorWafPolicy** cmdletGet pobiera zasady WAF w grupie zasobów w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="972e1-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="972e1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="972e1-107">EXAMPLES</span></span>

### <span data-ttu-id="972e1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="972e1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="972e1-109">Uzyskaj zasady WAF o nazwie $policyName w $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="972e1-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="972e1-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="972e1-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="972e1-111">Pobierz wszystkie zasady WAF w $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="972e1-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="972e1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="972e1-112">PARAMETERS</span></span>

### <span data-ttu-id="972e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="972e1-113">-DefaultProfile</span></span>
<span data-ttu-id="972e1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="972e1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="972e1-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="972e1-115">-Name</span></span>
<span data-ttu-id="972e1-116">Nazwa FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="972e1-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="972e1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="972e1-117">-ResourceGroupName</span></span>
<span data-ttu-id="972e1-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="972e1-118">The resource group name.</span></span>

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

### <span data-ttu-id="972e1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="972e1-119">CommonParameters</span></span>
<span data-ttu-id="972e1-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="972e1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="972e1-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="972e1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="972e1-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="972e1-122">INPUTS</span></span>

### <span data-ttu-id="972e1-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="972e1-123">None</span></span>

## <span data-ttu-id="972e1-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="972e1-124">OUTPUTS</span></span>

### <span data-ttu-id="972e1-125">Microsoft. Azure. Commands. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="972e1-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="972e1-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="972e1-126">NOTES</span></span>

## <span data-ttu-id="972e1-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="972e1-127">RELATED LINKS</span></span>

<span data-ttu-id="972e1-128">[Nowe — AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="972e1-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
