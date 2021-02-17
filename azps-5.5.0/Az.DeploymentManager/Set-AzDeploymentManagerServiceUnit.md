---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 7d2a7916e73b20e4c4e7a3602dc23bc10a67c744
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196490"
---
# <span data-ttu-id="8f19a-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="8f19a-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="8f19a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f19a-102">SYNOPSIS</span></span>
<span data-ttu-id="8f19a-103">Aktualizuje jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="8f19a-103">Updates the service unit.</span></span>

## <span data-ttu-id="8f19a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8f19a-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f19a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8f19a-105">DESCRIPTION</span></span>
<span data-ttu-id="8f19a-106">Polecenie **cmdlet Set-AzDeploymentManagerServiceUnit** aktualizuje jednostkę usługi za pomocą określonego obiektu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="8f19a-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="8f19a-107">Polecenie cmdlet zwraca zaktualizowany obiekt jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="8f19a-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="8f19a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8f19a-108">EXAMPLES</span></span>

### <span data-ttu-id="8f19a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8f19a-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="8f19a-110">To polecenie aktualizuje jednostkę usługi, której nazwa, nazwa usługi, nazwa topologii usługi i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa Usługi), ServiceTopologyName (Nazwa_usługi) i ResourceGroupName (Nazwa Grupy Zasobów) $serviceUnitObject grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8f19a-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="8f19a-111">To polecenie zwraca zaktualizowany obiekt jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="8f19a-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="8f19a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f19a-112">PARAMETERS</span></span>

### <span data-ttu-id="8f19a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f19a-113">-DefaultProfile</span></span>
<span data-ttu-id="8f19a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f19a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f19a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f19a-115">-InputObject</span></span>
<span data-ttu-id="8f19a-116">Obiekt jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="8f19a-116">The service unit object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f19a-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f19a-117">-Confirm</span></span>
<span data-ttu-id="8f19a-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8f19a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f19a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f19a-119">-WhatIf</span></span>
<span data-ttu-id="8f19a-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f19a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f19a-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8f19a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f19a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f19a-122">CommonParameters</span></span>
<span data-ttu-id="8f19a-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f19a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f19a-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f19a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f19a-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f19a-125">INPUTS</span></span>

### <span data-ttu-id="8f19a-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="8f19a-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="8f19a-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f19a-127">OUTPUTS</span></span>

### <span data-ttu-id="8f19a-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="8f19a-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="8f19a-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8f19a-129">NOTES</span></span>

## <span data-ttu-id="8f19a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f19a-130">RELATED LINKS</span></span>
