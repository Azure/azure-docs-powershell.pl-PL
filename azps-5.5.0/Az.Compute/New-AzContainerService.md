---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: e401755786c8f1aaf967417f526c8a976b333048
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199266"
---
# <span data-ttu-id="0418f-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0418f-101">New-AzContainerService</span></span>

## <span data-ttu-id="0418f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0418f-102">SYNOPSIS</span></span>
<span data-ttu-id="0418f-103">Tworzy usługę kontenerową.</span><span class="sxs-lookup"><span data-stu-id="0418f-103">Creates a container service.</span></span>

## <span data-ttu-id="0418f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0418f-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-ContainerService] <PSContainerService>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0418f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0418f-105">DESCRIPTION</span></span>
<span data-ttu-id="0418f-106">Polecenie **cmdlet New-AzContainerService** tworzy usługę kontenerową.</span><span class="sxs-lookup"><span data-stu-id="0418f-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="0418f-107">Określ obiekt usługi kontenera, który można utworzyć za pomocą New-AzContainerServiceConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0418f-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="0418f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0418f-108">EXAMPLES</span></span>

### <span data-ttu-id="0418f-109">Przykład 1. Tworzenie usługi kontenerowej</span><span class="sxs-lookup"><span data-stu-id="0418f-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "East US" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "East US" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "acslinuxadmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="0418f-110">Pierwsze polecenie tworzy grupę zasobów o nazwie Grupa Zasobów17 w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0418f-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="0418f-111">Aby uzyskać więcej informacji, zobacz New-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0418f-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="0418f-112">Drugie polecenie tworzy kontener, a następnie przechowuje go w $Container danych.</span><span class="sxs-lookup"><span data-stu-id="0418f-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="0418f-113">Aby uzyskać więcej informacji, zobacz New-AzContainerServiceConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0418f-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="0418f-114">Końcowe polecenie tworzy usługę kontenera dla kontenera przechowywanego w $Container.</span><span class="sxs-lookup"><span data-stu-id="0418f-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="0418f-115">Usługa nosi nazwę csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="0418f-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="0418f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0418f-116">PARAMETERS</span></span>

### <span data-ttu-id="0418f-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0418f-117">-AsJob</span></span>
<span data-ttu-id="0418f-118">Polecenie cmdlet RRun w tle i zwraca zadanie do śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="0418f-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0418f-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="0418f-119">-ContainerService</span></span>
<span data-ttu-id="0418f-120">Określa obiekt usługi kontenera zawierający właściwości nowej usługi.</span><span class="sxs-lookup"><span data-stu-id="0418f-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="0418f-121">Aby uzyskać obiekt **ContainerService,** użyj New-AzContainerServiceConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0418f-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0418f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0418f-122">-DefaultProfile</span></span>
<span data-ttu-id="0418f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0418f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0418f-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0418f-124">-Name</span></span>
<span data-ttu-id="0418f-125">Określa nazwę usługi kontenera, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0418f-125">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0418f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0418f-126">-ResourceGroupName</span></span>
<span data-ttu-id="0418f-127">Określa grupę zasobów, w której to polecenie cmdlet wdraża usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="0418f-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0418f-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0418f-128">-Confirm</span></span>
<span data-ttu-id="0418f-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0418f-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0418f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0418f-130">-WhatIf</span></span>
<span data-ttu-id="0418f-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0418f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0418f-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0418f-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0418f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0418f-133">CommonParameters</span></span>
<span data-ttu-id="0418f-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0418f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0418f-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0418f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0418f-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0418f-136">INPUTS</span></span>

### <span data-ttu-id="0418f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0418f-137">System.String</span></span>

### <span data-ttu-id="0418f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="0418f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="0418f-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0418f-139">OUTPUTS</span></span>

### <span data-ttu-id="0418f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="0418f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="0418f-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0418f-141">NOTES</span></span>

## <span data-ttu-id="0418f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0418f-142">RELATED LINKS</span></span>

[<span data-ttu-id="0418f-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0418f-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="0418f-144">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="0418f-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="0418f-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0418f-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="0418f-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0418f-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


