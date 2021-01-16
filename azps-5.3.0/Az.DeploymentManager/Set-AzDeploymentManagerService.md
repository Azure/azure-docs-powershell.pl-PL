---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501121"
---
# <span data-ttu-id="034fa-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="034fa-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="034fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="034fa-102">SYNOPSIS</span></span>
<span data-ttu-id="034fa-103">Aktualizuje usługę.</span><span class="sxs-lookup"><span data-stu-id="034fa-103">Updates the service.</span></span>

## <span data-ttu-id="034fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="034fa-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="034fa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="034fa-105">DESCRIPTION</span></span>
<span data-ttu-id="034fa-106">Polecenie cmdlet **Set-AzDeploymentManagerService** aktualizuje usługę z określonym obiektem usługi.</span><span class="sxs-lookup"><span data-stu-id="034fa-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="034fa-107">Polecenie cmdlet zwraca zaktualizowany obiekt usługi.</span><span class="sxs-lookup"><span data-stu-id="034fa-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="034fa-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="034fa-108">EXAMPLES</span></span>

### <span data-ttu-id="034fa-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="034fa-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="034fa-110">To polecenie aktualizuje usługę, której nazwa, nazwa topologii usługi i element Resources są zgodne z właściwościami Name, servicetopologyname i ResourceGroupName w $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="034fa-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="034fa-111">Usługa zostanie zaktualizowana do właściwości ustawionych w $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="034fa-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="034fa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="034fa-112">PARAMETERS</span></span>

### <span data-ttu-id="034fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034fa-113">-DefaultProfile</span></span>
<span data-ttu-id="034fa-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="034fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="034fa-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="034fa-115">-InputObject</span></span>
<span data-ttu-id="034fa-116">Obiekt usługi.</span><span class="sxs-lookup"><span data-stu-id="034fa-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="034fa-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="034fa-117">-Confirm</span></span>
<span data-ttu-id="034fa-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="034fa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="034fa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="034fa-119">-WhatIf</span></span>
<span data-ttu-id="034fa-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="034fa-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="034fa-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="034fa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="034fa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034fa-122">CommonParameters</span></span>
<span data-ttu-id="034fa-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="034fa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034fa-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="034fa-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034fa-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="034fa-125">INPUTS</span></span>

### <span data-ttu-id="034fa-126">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="034fa-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="034fa-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="034fa-127">OUTPUTS</span></span>

### <span data-ttu-id="034fa-128">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="034fa-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="034fa-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="034fa-129">NOTES</span></span>

## <span data-ttu-id="034fa-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="034fa-130">RELATED LINKS</span></span>
