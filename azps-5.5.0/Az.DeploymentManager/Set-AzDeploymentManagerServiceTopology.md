---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196499"
---
# <span data-ttu-id="4a005-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="4a005-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="4a005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a005-102">SYNOPSIS</span></span>
<span data-ttu-id="4a005-103">Aktualizuje topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="4a005-103">Updates the service topology.</span></span>

## <span data-ttu-id="4a005-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4a005-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a005-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4a005-105">DESCRIPTION</span></span>
<span data-ttu-id="4a005-106">Polecenie **cmdlet Set-AzDeploymentManagerServiceTopology** aktualizuje topologię usługi przy użyciu określonego obiektu topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="4a005-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="4a005-107">Polecenie cmdlet zwraca obiekt topologii zaktualizowanej usługi.</span><span class="sxs-lookup"><span data-stu-id="4a005-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="4a005-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4a005-108">EXAMPLES</span></span>

### <span data-ttu-id="4a005-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4a005-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="4a005-110">To polecenie aktualizuje topologię usługi, której nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $serviceTopologyObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="4a005-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="4a005-111">To polecenie zwraca obiekt topologii zaktualizowanej usługi.</span><span class="sxs-lookup"><span data-stu-id="4a005-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="4a005-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a005-112">PARAMETERS</span></span>

### <span data-ttu-id="4a005-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a005-113">-DefaultProfile</span></span>
<span data-ttu-id="4a005-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a005-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a005-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a005-115">-InputObject</span></span>
<span data-ttu-id="4a005-116">Obiekt topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="4a005-116">The service topology object.</span></span>

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

### <span data-ttu-id="4a005-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a005-117">-Confirm</span></span>
<span data-ttu-id="4a005-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4a005-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a005-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a005-119">-WhatIf</span></span>
<span data-ttu-id="4a005-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a005-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a005-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4a005-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a005-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a005-122">CommonParameters</span></span>
<span data-ttu-id="4a005-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a005-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a005-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a005-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a005-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a005-125">INPUTS</span></span>

### <span data-ttu-id="4a005-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="4a005-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="4a005-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a005-127">OUTPUTS</span></span>

### <span data-ttu-id="4a005-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="4a005-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="4a005-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4a005-129">NOTES</span></span>

## <span data-ttu-id="4a005-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a005-130">RELATED LINKS</span></span>
