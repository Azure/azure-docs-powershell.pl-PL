---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 633173a0ce8814ee2af9300be5b1cfc19bdf9a5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975633"
---
# <span data-ttu-id="6ca29-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="6ca29-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="6ca29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ca29-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca29-103">Zatrzymaj podkołowy SSH Kubectl utworzony w tablicy Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="6ca29-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="6ca29-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6ca29-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ca29-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6ca29-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca29-106">Zatrzymaj podkołowy SSH Kubectl utworzony w tablicy Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="6ca29-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="6ca29-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6ca29-107">EXAMPLES</span></span>

### <span data-ttu-id="6ca29-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ca29-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="6ca29-109">Zatrzymuje istniejącą konfigurację schowka typu SSH, wykonując proces Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="6ca29-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="6ca29-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ca29-110">PARAMETERS</span></span>

### <span data-ttu-id="6ca29-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca29-111">-DefaultProfile</span></span>
<span data-ttu-id="6ca29-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca29-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ca29-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ca29-113">-PassThru</span></span>
<span data-ttu-id="6ca29-114">Zwraca wartość true, jeśli podkołowy SSH jest zamknięty.</span><span class="sxs-lookup"><span data-stu-id="6ca29-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="6ca29-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca29-115">CommonParameters</span></span>
<span data-ttu-id="6ca29-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca29-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca29-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ca29-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca29-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ca29-118">INPUTS</span></span>

### <span data-ttu-id="6ca29-119">Brak</span><span class="sxs-lookup"><span data-stu-id="6ca29-119">None</span></span>

## <span data-ttu-id="6ca29-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ca29-120">OUTPUTS</span></span>

### <span data-ttu-id="6ca29-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6ca29-121">System.Boolean</span></span>

## <span data-ttu-id="6ca29-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6ca29-122">NOTES</span></span>

## <span data-ttu-id="6ca29-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ca29-123">RELATED LINKS</span></span>
