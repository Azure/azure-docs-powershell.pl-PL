---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192642"
---
# <span data-ttu-id="fc825-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="fc825-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="fc825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc825-102">SYNOPSIS</span></span>
<span data-ttu-id="fc825-103">Zatrzymaj podkołowy SSH Kubectl utworzone w tablicy Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="fc825-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="fc825-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fc825-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc825-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fc825-105">DESCRIPTION</span></span>
<span data-ttu-id="fc825-106">Zatrzymaj podkołowy SSH Kubectl utworzone w tablicy Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="fc825-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="fc825-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fc825-107">EXAMPLES</span></span>

### <span data-ttu-id="fc825-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fc825-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="fc825-109">Zatrzymuje istniejącą konfigurację schowka SSH, wykonując proces Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="fc825-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="fc825-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc825-110">PARAMETERS</span></span>

### <span data-ttu-id="fc825-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc825-111">-DefaultProfile</span></span>
<span data-ttu-id="fc825-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc825-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc825-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc825-113">-PassThru</span></span>
<span data-ttu-id="fc825-114">Zwraca wartość true, jeśli podkołowy SSH jest zamknięty.</span><span class="sxs-lookup"><span data-stu-id="fc825-114">Returns true if SSH tunnel is closed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc825-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc825-115">CommonParameters</span></span>
<span data-ttu-id="fc825-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc825-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc825-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc825-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc825-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc825-118">INPUTS</span></span>

### <span data-ttu-id="fc825-119">Brak</span><span class="sxs-lookup"><span data-stu-id="fc825-119">None</span></span>

## <span data-ttu-id="fc825-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc825-120">OUTPUTS</span></span>

### <span data-ttu-id="fc825-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fc825-121">System.Boolean</span></span>

## <span data-ttu-id="fc825-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fc825-122">NOTES</span></span>

## <span data-ttu-id="fc825-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc825-123">RELATED LINKS</span></span>
