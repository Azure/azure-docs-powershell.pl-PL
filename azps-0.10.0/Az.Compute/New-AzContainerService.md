---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: b8f453200f2365272461373214ec92580212c4b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893666"
---
# <span data-ttu-id="1c2f3-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="1c2f3-101">New-AzContainerService</span></span>

## <span data-ttu-id="1c2f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2f3-103">Tworzy usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-103">Creates a container service.</span></span>

## <span data-ttu-id="1c2f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c2f3-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c2f3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1c2f3-105">DESCRIPTION</span></span>
<span data-ttu-id="1c2f3-106">Polecenie cmdlet **New-AzContainerService** tworzy usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="1c2f3-107">Określ obiekt usługi kontenera, który możesz utworzyć przy użyciu New-AzContainerServiceConfig polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="1c2f3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c2f3-108">EXAMPLES</span></span>

### <span data-ttu-id="1c2f3-109">Przykład 1: Tworzenie usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="1c2f3-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="1c2f3-110">Pierwsze polecenie tworzy grupę zasobów o nazwie ResourceGroup17 w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="1c2f3-111">Aby uzyskać więcej informacji, zobacz polecenie cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="1c2f3-112">Drugie polecenie tworzy kontener, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="1c2f3-113">Aby uzyskać więcej informacji, zobacz polecenie cmdlet New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="1c2f3-114">Polecenie ostatnie tworzy usługę kontenera dla kontenera przechowywanego w $Container.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="1c2f3-115">Usługa ma nazwę csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="1c2f3-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c2f3-116">PARAMETERS</span></span>

### <span data-ttu-id="1c2f3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c2f3-117">-AsJob</span></span>
<span data-ttu-id="1c2f3-118">RRun polecenia cmdlet w tle i zwracają zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1c2f3-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="1c2f3-119">-ContainerService</span></span>
<span data-ttu-id="1c2f3-120">Określa obiekt usługi kontenera, który zawiera właściwości nowej usługi.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="1c2f3-121">Aby uzyskać obiekt **ContainerService** , użyj polecenia cmdlet New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="1c2f3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2f3-122">-DefaultProfile</span></span>
<span data-ttu-id="1c2f3-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c2f3-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1c2f3-124">-Name</span></span>
<span data-ttu-id="1c2f3-125">Określa nazwę usługi kontenera, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1c2f3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c2f3-126">-ResourceGroupName</span></span>
<span data-ttu-id="1c2f3-127">Określa grupę zasobów, w której to polecenie cmdlet wdraża usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="1c2f3-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c2f3-128">-Confirm</span></span>
<span data-ttu-id="1c2f3-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c2f3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c2f3-130">-WhatIf</span></span>
<span data-ttu-id="1c2f3-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1c2f3-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c2f3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2f3-133">CommonParameters</span></span>
<span data-ttu-id="1c2f3-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c2f3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c2f3-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c2f3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2f3-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c2f3-136">INPUTS</span></span>

### <span data-ttu-id="1c2f3-137">ContainerService</span><span class="sxs-lookup"><span data-stu-id="1c2f3-137">ContainerService</span></span>
<span data-ttu-id="1c2f3-138">Parametr "ContainerService" akceptuje wartość typu "ContainerService" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="1c2f3-138">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="1c2f3-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c2f3-139">OUTPUTS</span></span>

### <span data-ttu-id="1c2f3-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="1c2f3-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="1c2f3-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c2f3-141">NOTES</span></span>

## <span data-ttu-id="1c2f3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c2f3-142">RELATED LINKS</span></span>

[<span data-ttu-id="1c2f3-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="1c2f3-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="1c2f3-144">Nowe — AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="1c2f3-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="1c2f3-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="1c2f3-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="1c2f3-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="1c2f3-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


