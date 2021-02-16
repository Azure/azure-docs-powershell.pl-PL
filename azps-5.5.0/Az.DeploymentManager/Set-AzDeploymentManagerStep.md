---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 2cd73cad57f36130ed11e37ad6dc2147e6c081ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243819"
---
# <span data-ttu-id="265d8-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="265d8-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="265d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="265d8-102">SYNOPSIS</span></span>
<span data-ttu-id="265d8-103">Aktualizuje krok.</span><span class="sxs-lookup"><span data-stu-id="265d8-103">Updates the step.</span></span>

## <span data-ttu-id="265d8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="265d8-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="265d8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="265d8-105">DESCRIPTION</span></span>
<span data-ttu-id="265d8-106">Polecenie **cmdlet Set-AzDeploymentManagerStep** aktualizuje krok o określonym obiekcie kroku.</span><span class="sxs-lookup"><span data-stu-id="265d8-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="265d8-107">Polecenie cmdlet zwraca zaktualizowany obiekt kroku.</span><span class="sxs-lookup"><span data-stu-id="265d8-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="265d8-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="265d8-108">EXAMPLES</span></span>

### <span data-ttu-id="265d8-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="265d8-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="265d8-110">To polecenie aktualizuje krok, którego nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $stepObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="265d8-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="265d8-111">Krok zostanie zaktualizowany do właściwości określonych w $stepObject.</span><span class="sxs-lookup"><span data-stu-id="265d8-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="265d8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="265d8-112">PARAMETERS</span></span>

### <span data-ttu-id="265d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="265d8-113">-DefaultProfile</span></span>
<span data-ttu-id="265d8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="265d8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="265d8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="265d8-115">-InputObject</span></span>
<span data-ttu-id="265d8-116">Obiekt kroku.</span><span class="sxs-lookup"><span data-stu-id="265d8-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="265d8-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="265d8-117">-Confirm</span></span>
<span data-ttu-id="265d8-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="265d8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="265d8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="265d8-119">-WhatIf</span></span>
<span data-ttu-id="265d8-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="265d8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="265d8-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="265d8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="265d8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="265d8-122">CommonParameters</span></span>
<span data-ttu-id="265d8-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="265d8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="265d8-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="265d8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="265d8-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="265d8-125">INPUTS</span></span>

### <span data-ttu-id="265d8-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="265d8-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="265d8-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="265d8-127">OUTPUTS</span></span>

### <span data-ttu-id="265d8-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="265d8-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="265d8-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="265d8-129">NOTES</span></span>

## <span data-ttu-id="265d8-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="265d8-130">RELATED LINKS</span></span>
