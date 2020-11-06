---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: 6387e5a2938bdef99e4aea5e93248a0ecf8e8da7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524185"
---
# <span data-ttu-id="42c07-101">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="42c07-101">Set-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="42c07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42c07-102">SYNOPSIS</span></span>
<span data-ttu-id="42c07-103">Aktualizuje topologię usług.</span><span class="sxs-lookup"><span data-stu-id="42c07-103">Updates the service topology.</span></span>

## <span data-ttu-id="42c07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42c07-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42c07-105">Opis</span><span class="sxs-lookup"><span data-stu-id="42c07-105">DESCRIPTION</span></span>
<span data-ttu-id="42c07-106">Polecenie cmdlet **Set-AzureRmDeploymentManagerServiceTopology** aktualizuje topologię usługi za pomocą określonego obiektu typu topologia usług.</span><span class="sxs-lookup"><span data-stu-id="42c07-106">The **Set-AzureRmDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="42c07-107">Polecenie cmdlet zwraca zaktualizowany obiekt topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="42c07-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="42c07-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42c07-108">EXAMPLES</span></span>

### <span data-ttu-id="42c07-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="42c07-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="42c07-110">To polecenie aktualizuje topologię usługi, której nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="42c07-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="42c07-111">Polecenie zwraca zaktualizowany obiekt topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="42c07-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="42c07-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42c07-112">PARAMETERS</span></span>

### <span data-ttu-id="42c07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c07-113">-DefaultProfile</span></span>
<span data-ttu-id="42c07-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42c07-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c07-115">-Servicetopology</span><span class="sxs-lookup"><span data-stu-id="42c07-115">-ServiceTopology</span></span>
<span data-ttu-id="42c07-116">Obiekt Topology (topologia usług).</span><span class="sxs-lookup"><span data-stu-id="42c07-116">The service topology object.</span></span>

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

### <span data-ttu-id="42c07-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42c07-117">-Confirm</span></span>
<span data-ttu-id="42c07-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42c07-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42c07-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42c07-119">-WhatIf</span></span>
<span data-ttu-id="42c07-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42c07-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42c07-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42c07-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42c07-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c07-122">CommonParameters</span></span>
<span data-ttu-id="42c07-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42c07-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c07-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42c07-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c07-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42c07-125">INPUTS</span></span>

### <span data-ttu-id="42c07-126">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="42c07-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="42c07-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42c07-127">OUTPUTS</span></span>

### <span data-ttu-id="42c07-128">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="42c07-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="42c07-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42c07-129">NOTES</span></span>

## <span data-ttu-id="42c07-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42c07-130">RELATED LINKS</span></span>

[<span data-ttu-id="42c07-131">Nowe — AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="42c07-131">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="42c07-132">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="42c07-132">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="42c07-133">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="42c07-133">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)