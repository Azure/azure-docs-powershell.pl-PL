---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: e401755786c8f1aaf967417f526c8a976b333048
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050444"
---
# <span data-ttu-id="b60aa-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="b60aa-101">New-AzContainerService</span></span>

## <span data-ttu-id="b60aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b60aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b60aa-103">Tworzy usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="b60aa-103">Creates a container service.</span></span>

## <span data-ttu-id="b60aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b60aa-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-ContainerService] <PSContainerService>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b60aa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b60aa-105">DESCRIPTION</span></span>
<span data-ttu-id="b60aa-106">Polecenie cmdlet **New-AzContainerService** tworzy usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="b60aa-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="b60aa-107">Określ obiekt usługi kontenera, który możesz utworzyć przy użyciu New-AzContainerServiceConfig polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b60aa-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="b60aa-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b60aa-108">EXAMPLES</span></span>

### <span data-ttu-id="b60aa-109">Przykład 1: Tworzenie usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="b60aa-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "East US" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "East US" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "acslinuxadmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="b60aa-110">Pierwsze polecenie tworzy grupę zasobów o nazwie ResourceGroup17 w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b60aa-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="b60aa-111">Aby uzyskać więcej informacji, zobacz polecenie cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b60aa-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="b60aa-112">Drugie polecenie tworzy kontener, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="b60aa-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="b60aa-113">Aby uzyskać więcej informacji, zobacz polecenie cmdlet New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="b60aa-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="b60aa-114">Polecenie ostatnie tworzy usługę kontenera dla kontenera przechowywanego w $Container.</span><span class="sxs-lookup"><span data-stu-id="b60aa-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="b60aa-115">Usługa ma nazwę csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="b60aa-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="b60aa-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b60aa-116">PARAMETERS</span></span>

### <span data-ttu-id="b60aa-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b60aa-117">-AsJob</span></span>
<span data-ttu-id="b60aa-118">RRun polecenia cmdlet w tle i zwracają zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="b60aa-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b60aa-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="b60aa-119">-ContainerService</span></span>
<span data-ttu-id="b60aa-120">Określa obiekt usługi kontenera, który zawiera właściwości nowej usługi.</span><span class="sxs-lookup"><span data-stu-id="b60aa-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="b60aa-121">Aby uzyskać obiekt **ContainerService** , użyj polecenia cmdlet New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="b60aa-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="b60aa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60aa-122">-DefaultProfile</span></span>
<span data-ttu-id="b60aa-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b60aa-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b60aa-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b60aa-124">-Name</span></span>
<span data-ttu-id="b60aa-125">Określa nazwę usługi kontenera, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b60aa-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b60aa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b60aa-126">-ResourceGroupName</span></span>
<span data-ttu-id="b60aa-127">Określa grupę zasobów, w której to polecenie cmdlet wdraża usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="b60aa-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="b60aa-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b60aa-128">-Confirm</span></span>
<span data-ttu-id="b60aa-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b60aa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b60aa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b60aa-130">-WhatIf</span></span>
<span data-ttu-id="b60aa-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b60aa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b60aa-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b60aa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b60aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60aa-133">CommonParameters</span></span>
<span data-ttu-id="b60aa-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b60aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60aa-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b60aa-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60aa-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b60aa-136">INPUTS</span></span>

### <span data-ttu-id="b60aa-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b60aa-137">System.String</span></span>

### <span data-ttu-id="b60aa-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="b60aa-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="b60aa-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b60aa-139">OUTPUTS</span></span>

### <span data-ttu-id="b60aa-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="b60aa-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="b60aa-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b60aa-141">NOTES</span></span>

## <span data-ttu-id="b60aa-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b60aa-142">RELATED LINKS</span></span>

[<span data-ttu-id="b60aa-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="b60aa-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="b60aa-144">Nowe — AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="b60aa-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="b60aa-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="b60aa-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="b60aa-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="b60aa-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


