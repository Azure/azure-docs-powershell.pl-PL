---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 7d2a7916e73b20e4c4e7a3602dc23bc10a67c744
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223981"
---
# <span data-ttu-id="c001e-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="c001e-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="c001e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c001e-102">SYNOPSIS</span></span>
<span data-ttu-id="c001e-103">Umożliwia zaktualizowanie jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="c001e-103">Updates the service unit.</span></span>

## <span data-ttu-id="c001e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c001e-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c001e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c001e-105">DESCRIPTION</span></span>
<span data-ttu-id="c001e-106">Polecenie cmdlet **Set-AzDeploymentManagerServiceUnit** aktualizuje jednostkę usługi za pomocą określonego obiektu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="c001e-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="c001e-107">Polecenie cmdlet zwraca zaktualizowany obiekt jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="c001e-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="c001e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c001e-108">EXAMPLES</span></span>

### <span data-ttu-id="c001e-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c001e-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="c001e-110">To polecenie aktualizuje jednostkę usługi, której nazwa, nazwa usługi, nazwa topologii usługi i przydziały zasobów są odpowiednio zgodne z właściwościami Name, ServiceName, servicetopologyname i ResourceGroupName w $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="c001e-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="c001e-111">Polecenie zwraca zaktualizowany obiekt jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="c001e-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="c001e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c001e-112">PARAMETERS</span></span>

### <span data-ttu-id="c001e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c001e-113">-DefaultProfile</span></span>
<span data-ttu-id="c001e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c001e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c001e-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c001e-115">-InputObject</span></span>
<span data-ttu-id="c001e-116">Obiekt jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="c001e-116">The service unit object.</span></span>

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

### <span data-ttu-id="c001e-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c001e-117">-Confirm</span></span>
<span data-ttu-id="c001e-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c001e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c001e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c001e-119">-WhatIf</span></span>
<span data-ttu-id="c001e-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c001e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c001e-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c001e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c001e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c001e-122">CommonParameters</span></span>
<span data-ttu-id="c001e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c001e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c001e-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c001e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c001e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c001e-125">INPUTS</span></span>

### <span data-ttu-id="c001e-126">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="c001e-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="c001e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c001e-127">OUTPUTS</span></span>

### <span data-ttu-id="c001e-128">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="c001e-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="c001e-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c001e-129">NOTES</span></span>

## <span data-ttu-id="c001e-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c001e-130">RELATED LINKS</span></span>
