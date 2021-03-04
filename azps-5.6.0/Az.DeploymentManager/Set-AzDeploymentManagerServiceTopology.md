---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7e3ed99abe5fb7a679506571d7d734cad02084d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966250"
---
# <span data-ttu-id="4b67a-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="4b67a-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="4b67a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b67a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b67a-103">Aktualizuje topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="4b67a-103">Updates the service topology.</span></span>

## <span data-ttu-id="4b67a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4b67a-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b67a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4b67a-105">DESCRIPTION</span></span>
<span data-ttu-id="4b67a-106">Polecenie **cmdlet Set-AzDeploymentManagerServiceTopology** aktualizuje topologię usługi przy użyciu określonego obiektu topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="4b67a-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="4b67a-107">Polecenie cmdlet zwraca obiekt topologii zaktualizowanej usługi.</span><span class="sxs-lookup"><span data-stu-id="4b67a-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="4b67a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4b67a-108">EXAMPLES</span></span>

### <span data-ttu-id="4b67a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4b67a-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="4b67a-110">To polecenie aktualizuje topologię usługi, której nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $serviceTopologyObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="4b67a-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="4b67a-111">To polecenie zwraca obiekt zaktualizowanej topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="4b67a-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="4b67a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b67a-112">PARAMETERS</span></span>

### <span data-ttu-id="4b67a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b67a-113">-DefaultProfile</span></span>
<span data-ttu-id="4b67a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b67a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b67a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b67a-115">-InputObject</span></span>
<span data-ttu-id="4b67a-116">Obiekt topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="4b67a-116">The service topology object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b67a-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4b67a-117">-Confirm</span></span>
<span data-ttu-id="4b67a-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4b67a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b67a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b67a-119">-WhatIf</span></span>
<span data-ttu-id="4b67a-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b67a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b67a-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4b67a-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b67a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b67a-122">CommonParameters</span></span>
<span data-ttu-id="4b67a-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b67a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b67a-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b67a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b67a-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b67a-125">INPUTS</span></span>

### <span data-ttu-id="4b67a-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="4b67a-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="4b67a-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b67a-127">OUTPUTS</span></span>

### <span data-ttu-id="4b67a-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="4b67a-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="4b67a-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4b67a-129">NOTES</span></span>

## <span data-ttu-id="4b67a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b67a-130">RELATED LINKS</span></span>
