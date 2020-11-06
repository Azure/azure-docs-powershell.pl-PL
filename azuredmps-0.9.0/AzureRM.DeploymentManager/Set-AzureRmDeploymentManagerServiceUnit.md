---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: b04819f61f37b9bb47818a8b17e93db9a7cdb05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523510"
---
# <span data-ttu-id="20eb3-101">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="20eb3-101">Set-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="20eb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="20eb3-103">Aktualizuje jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="20eb3-103">Updates a service unit.</span></span>

## <span data-ttu-id="20eb3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20eb3-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20eb3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="20eb3-105">DESCRIPTION</span></span>
<span data-ttu-id="20eb3-106">Polecenie cmdlet **Set-AzureRmDeploymentManagerServiceUnit** aktualizuje jednostkę usługi za pomocą określonego obiektu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="20eb3-106">The **Set-AzureRmDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="20eb3-107">Polecenie cmdlet zwraca zaktualizowany obiekt jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="20eb3-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="20eb3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20eb3-108">EXAMPLES</span></span>

### <span data-ttu-id="20eb3-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="20eb3-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="20eb3-110">To polecenie aktualizuje jednostkę usługi, której nazwa, nazwa usługi, nazwa topologii usługi i przydziały zasobów są odpowiednio zgodne z właściwościami Name, ServiceName, servicetopologyname i ResourceGroupName w $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="20eb3-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="20eb3-111">Polecenie zwraca zaktualizowany obiekt jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="20eb3-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="20eb3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20eb3-112">PARAMETERS</span></span>

### <span data-ttu-id="20eb3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20eb3-113">-DefaultProfile</span></span>
<span data-ttu-id="20eb3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20eb3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20eb3-115">-Serviceunit</span><span class="sxs-lookup"><span data-stu-id="20eb3-115">-ServiceUnit</span></span>
<span data-ttu-id="20eb3-116">Obiekt jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="20eb3-116">The service unit object.</span></span>

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

### <span data-ttu-id="20eb3-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20eb3-117">-Confirm</span></span>
<span data-ttu-id="20eb3-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20eb3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20eb3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20eb3-119">-WhatIf</span></span>
<span data-ttu-id="20eb3-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20eb3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20eb3-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="20eb3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20eb3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20eb3-122">CommonParameters</span></span>
<span data-ttu-id="20eb3-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20eb3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20eb3-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20eb3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20eb3-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20eb3-125">INPUTS</span></span>

### <span data-ttu-id="20eb3-126">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="20eb3-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="20eb3-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20eb3-127">OUTPUTS</span></span>

### <span data-ttu-id="20eb3-128">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="20eb3-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="20eb3-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20eb3-129">NOTES</span></span>

## <span data-ttu-id="20eb3-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20eb3-130">RELATED LINKS</span></span>

[<span data-ttu-id="20eb3-131">Nowe — AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="20eb3-131">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="20eb3-132">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="20eb3-132">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="20eb3-133">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="20eb3-133">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)