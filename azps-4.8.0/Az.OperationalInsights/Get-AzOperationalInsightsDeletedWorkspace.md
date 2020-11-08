---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223006"
---
# <span data-ttu-id="dd545-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="dd545-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="dd545-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd545-102">SYNOPSIS</span></span>
<span data-ttu-id="dd545-103">Wyświetlanie listy usuniętych obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="dd545-103">List deleted workspaces.</span></span>

## <span data-ttu-id="dd545-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd545-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd545-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dd545-105">DESCRIPTION</span></span>
<span data-ttu-id="dd545-106">Wyświetlanie listy usuniętych obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="dd545-106">List deleted workspaces.</span></span>

## <span data-ttu-id="dd545-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd545-107">EXAMPLES</span></span>

### <span data-ttu-id="dd545-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dd545-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="dd545-109">Wyświetlanie listy usuniętych obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="dd545-109">List deleted workspaces.</span></span>

## <span data-ttu-id="dd545-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd545-110">PARAMETERS</span></span>

### <span data-ttu-id="dd545-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd545-111">-DefaultProfile</span></span>
<span data-ttu-id="dd545-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd545-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd545-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd545-113">-ResourceGroupName</span></span>
<span data-ttu-id="dd545-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd545-114">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd545-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd545-115">CommonParameters</span></span>
<span data-ttu-id="dd545-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd545-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd545-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd545-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd545-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd545-118">INPUTS</span></span>

### <span data-ttu-id="dd545-119">System. String</span><span class="sxs-lookup"><span data-stu-id="dd545-119">System.String</span></span>

## <span data-ttu-id="dd545-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd545-120">OUTPUTS</span></span>

### <span data-ttu-id="dd545-121">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="dd545-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="dd545-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd545-122">NOTES</span></span>

## <span data-ttu-id="dd545-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd545-123">RELATED LINKS</span></span>
