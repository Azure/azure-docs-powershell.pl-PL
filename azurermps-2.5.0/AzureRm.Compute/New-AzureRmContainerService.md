---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 6d1a891dbef40a6556e3a8f2ca122f2c3b46cb28
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897685"
---
# <span data-ttu-id="45938-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="45938-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="45938-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45938-102">SYNOPSIS</span></span>
<span data-ttu-id="45938-103">Tworzy usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="45938-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45938-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45938-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45938-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45938-105">DESCRIPTION</span></span>
<span data-ttu-id="45938-106">Polecenie cmdlet **New-AzureRmContainerService** tworzy usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="45938-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="45938-107">Określ obiekt usługi kontenera, który możesz utworzyć przy użyciu New-AzureRmContainerServiceConfig polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45938-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="45938-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45938-108">EXAMPLES</span></span>

### <span data-ttu-id="45938-109">Przykład 1: Tworzenie usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="45938-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="45938-110">Pierwsze polecenie tworzy grupę zasobów o nazwie ResourceGroup17 w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="45938-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="45938-111">Aby uzyskać więcej informacji, zobacz polecenie cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="45938-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="45938-112">Drugie polecenie tworzy kontener, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="45938-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="45938-113">Aby uzyskać więcej informacji, zobacz polecenie cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="45938-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="45938-114">Polecenie ostatnie tworzy usługę kontenera dla kontenera przechowywanego w $Container.</span><span class="sxs-lookup"><span data-stu-id="45938-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="45938-115">Usługa ma nazwę csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="45938-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="45938-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45938-116">PARAMETERS</span></span>

### <span data-ttu-id="45938-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45938-117">-AsJob</span></span>
<span data-ttu-id="45938-118">RRun polecenia cmdlet w tle i zwracają zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="45938-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45938-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="45938-119">-ContainerService</span></span>
<span data-ttu-id="45938-120">Określa obiekt usługi kontenera, który zawiera właściwości nowej usługi.</span><span class="sxs-lookup"><span data-stu-id="45938-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="45938-121">Aby uzyskać obiekt **ContainerService** , użyj polecenia cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="45938-121">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45938-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45938-122">-DefaultProfile</span></span>
<span data-ttu-id="45938-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45938-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45938-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45938-124">-Name</span></span>
<span data-ttu-id="45938-125">Określa nazwę usługi kontenera, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45938-125">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45938-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45938-126">-ResourceGroupName</span></span>
<span data-ttu-id="45938-127">Określa grupę zasobów, w której to polecenie cmdlet wdraża usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="45938-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45938-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45938-128">-Confirm</span></span>
<span data-ttu-id="45938-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45938-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45938-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45938-130">-WhatIf</span></span>
<span data-ttu-id="45938-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45938-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="45938-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45938-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45938-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45938-133">CommonParameters</span></span>
<span data-ttu-id="45938-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45938-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45938-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45938-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45938-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45938-136">INPUTS</span></span>

### <span data-ttu-id="45938-137">ContainerService</span><span class="sxs-lookup"><span data-stu-id="45938-137">ContainerService</span></span>
<span data-ttu-id="45938-138">Parametr "ContainerService" akceptuje wartość typu "ContainerService" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="45938-138">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="45938-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45938-139">OUTPUTS</span></span>

### <span data-ttu-id="45938-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="45938-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="45938-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45938-141">NOTES</span></span>

## <span data-ttu-id="45938-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45938-142">RELATED LINKS</span></span>

[<span data-ttu-id="45938-143">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="45938-143">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="45938-144">Nowe — AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="45938-144">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="45938-145">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="45938-145">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="45938-146">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="45938-146">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


