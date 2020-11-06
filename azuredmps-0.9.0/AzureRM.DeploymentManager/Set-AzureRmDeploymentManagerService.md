---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 2f4cab266cf63e1c33c35c051e9cc2b838f5b066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523041"
---
# <span data-ttu-id="e5239-101">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="e5239-101">Set-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="e5239-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5239-102">SYNOPSIS</span></span>
<span data-ttu-id="e5239-103">Aktualizuje usługę w topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="e5239-103">Updates a service in service topology.</span></span>

## <span data-ttu-id="e5239-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5239-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5239-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e5239-105">DESCRIPTION</span></span>
<span data-ttu-id="e5239-106">Polecenie cmdlet **Set-AzureRmDeploymentManagerService** aktualizuje usługę z określonym obiektem usługi.</span><span class="sxs-lookup"><span data-stu-id="e5239-106">The **Set-AzureRmDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="e5239-107">Polecenie cmdlet zwraca zaktualizowany obiekt usługi.</span><span class="sxs-lookup"><span data-stu-id="e5239-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="e5239-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5239-108">EXAMPLES</span></span>

### <span data-ttu-id="e5239-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5239-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="e5239-110">To polecenie aktualizuje usługę, której nazwa, nazwa topologii usługi i element Resources są zgodne z właściwościami Name, servicetopologyname i ResourceGroupName w $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="e5239-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="e5239-111">Usługa zostanie zaktualizowana do właściwości ustawionych w $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="e5239-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="e5239-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5239-112">PARAMETERS</span></span>

### <span data-ttu-id="e5239-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5239-113">-DefaultProfile</span></span>
<span data-ttu-id="e5239-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5239-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5239-115">-Service</span><span class="sxs-lookup"><span data-stu-id="e5239-115">-Service</span></span>
<span data-ttu-id="e5239-116">Obiekt usługi.</span><span class="sxs-lookup"><span data-stu-id="e5239-116">The service object.</span></span>

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

### <span data-ttu-id="e5239-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5239-117">-Confirm</span></span>
<span data-ttu-id="e5239-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5239-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5239-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5239-119">-WhatIf</span></span>
<span data-ttu-id="e5239-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5239-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5239-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e5239-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5239-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5239-122">CommonParameters</span></span>
<span data-ttu-id="e5239-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5239-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5239-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5239-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5239-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5239-125">INPUTS</span></span>

### <span data-ttu-id="e5239-126">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="e5239-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="e5239-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5239-127">OUTPUTS</span></span>

### <span data-ttu-id="e5239-128">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="e5239-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="e5239-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5239-129">NOTES</span></span>

## <span data-ttu-id="e5239-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5239-130">RELATED LINKS</span></span>

[<span data-ttu-id="e5239-131">Nowe — AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="e5239-131">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="e5239-132">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="e5239-132">Get-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="e5239-133">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="e5239-133">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)