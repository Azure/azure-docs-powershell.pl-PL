---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 3509212801aaeda9926b7f441e0aae7e17f8cbb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709935"
---
# <span data-ttu-id="bd458-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="bd458-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="bd458-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd458-102">SYNOPSIS</span></span>
<span data-ttu-id="bd458-103">Umożliwia zaktualizowanie jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="bd458-103">Updates the service unit.</span></span>

## <span data-ttu-id="bd458-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd458-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd458-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bd458-105">DESCRIPTION</span></span>
<span data-ttu-id="bd458-106">Polecenie cmdlet **Set-AzDeploymentManagerServiceUnit** aktualizuje jednostkę usługi za pomocą określonego obiektu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="bd458-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="bd458-107">Polecenie cmdlet zwraca zaktualizowany obiekt jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="bd458-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="bd458-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd458-108">EXAMPLES</span></span>

### <span data-ttu-id="bd458-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bd458-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="bd458-110">To polecenie aktualizuje jednostkę usługi, której nazwa, nazwa usługi, nazwa topologii usługi i przydziały zasobów są odpowiednio zgodne z właściwościami Name, ServiceName, servicetopologyname i ResourceGroupName w $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="bd458-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="bd458-111">Polecenie zwraca zaktualizowany obiekt jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="bd458-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="bd458-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd458-112">PARAMETERS</span></span>

### <span data-ttu-id="bd458-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd458-113">-DefaultProfile</span></span>
<span data-ttu-id="bd458-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd458-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd458-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bd458-115">-InputObject</span></span>
<span data-ttu-id="bd458-116">Obiekt jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="bd458-116">The service unit object.</span></span>

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

### <span data-ttu-id="bd458-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd458-117">-Confirm</span></span>
<span data-ttu-id="bd458-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd458-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd458-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd458-119">-WhatIf</span></span>
<span data-ttu-id="bd458-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd458-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd458-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd458-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd458-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd458-122">CommonParameters</span></span>
<span data-ttu-id="bd458-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd458-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd458-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd458-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd458-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd458-125">INPUTS</span></span>

### <span data-ttu-id="bd458-126">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="bd458-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="bd458-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd458-127">OUTPUTS</span></span>

### <span data-ttu-id="bd458-128">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="bd458-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="bd458-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd458-129">NOTES</span></span>

## <span data-ttu-id="bd458-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd458-130">RELATED LINKS</span></span>
