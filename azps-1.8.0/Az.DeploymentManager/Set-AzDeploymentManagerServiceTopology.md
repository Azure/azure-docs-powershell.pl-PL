---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: ff3cdb549835ceb4689ee5be8569b61ffa89538d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709934"
---
# <span data-ttu-id="4dff0-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="4dff0-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="4dff0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4dff0-102">SYNOPSIS</span></span>
<span data-ttu-id="4dff0-103">Aktualizuje topologię usług.</span><span class="sxs-lookup"><span data-stu-id="4dff0-103">Updates the service topology.</span></span>

## <span data-ttu-id="4dff0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4dff0-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dff0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4dff0-105">DESCRIPTION</span></span>
<span data-ttu-id="4dff0-106">Polecenie cmdlet **Set-AzDeploymentManagerServiceTopology** aktualizuje topologię usługi za pomocą określonego obiektu typu topologia usług.</span><span class="sxs-lookup"><span data-stu-id="4dff0-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="4dff0-107">Polecenie cmdlet zwraca zaktualizowany obiekt topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="4dff0-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="4dff0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4dff0-108">EXAMPLES</span></span>

### <span data-ttu-id="4dff0-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4dff0-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="4dff0-110">To polecenie aktualizuje topologię usługi, której nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="4dff0-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="4dff0-111">Polecenie zwraca zaktualizowany obiekt topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="4dff0-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="4dff0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4dff0-112">PARAMETERS</span></span>

### <span data-ttu-id="4dff0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dff0-113">-DefaultProfile</span></span>
<span data-ttu-id="4dff0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4dff0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dff0-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4dff0-115">-InputObject</span></span>
<span data-ttu-id="4dff0-116">Obiekt Topology (topologia usług).</span><span class="sxs-lookup"><span data-stu-id="4dff0-116">The service topology object.</span></span>

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

### <span data-ttu-id="4dff0-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4dff0-117">-Confirm</span></span>
<span data-ttu-id="4dff0-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dff0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dff0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dff0-119">-WhatIf</span></span>
<span data-ttu-id="4dff0-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dff0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dff0-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4dff0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dff0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dff0-122">CommonParameters</span></span>
<span data-ttu-id="4dff0-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dff0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dff0-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dff0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dff0-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4dff0-125">INPUTS</span></span>

### <span data-ttu-id="4dff0-126">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="4dff0-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="4dff0-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4dff0-127">OUTPUTS</span></span>

### <span data-ttu-id="4dff0-128">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="4dff0-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="4dff0-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4dff0-129">NOTES</span></span>

## <span data-ttu-id="4dff0-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4dff0-130">RELATED LINKS</span></span>