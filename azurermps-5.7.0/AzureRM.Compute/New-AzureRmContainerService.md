---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: ff337ae0f5d0da86b035905bf83d2719edf1f4f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525322"
---
# <span data-ttu-id="df7cd-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="df7cd-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="df7cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="df7cd-103">Tworzy usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="df7cd-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df7cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df7cd-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <ContainerService> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df7cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="df7cd-105">DESCRIPTION</span></span>
<span data-ttu-id="df7cd-106">Polecenie cmdlet **New-AzureRmContainerService** tworzy usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="df7cd-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="df7cd-107">Określ obiekt usługi kontenera, który możesz utworzyć przy użyciu New-AzureRmContainerServiceConfig polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df7cd-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="df7cd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df7cd-108">EXAMPLES</span></span>

### <span data-ttu-id="df7cd-109">Przykład 1: Tworzenie usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="df7cd-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="df7cd-110">Pierwsze polecenie tworzy grupę zasobów o nazwie ResourceGroup17 w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="df7cd-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="df7cd-111">Aby uzyskać więcej informacji, zobacz polecenie cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="df7cd-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="df7cd-112">Drugie polecenie tworzy kontener, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="df7cd-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="df7cd-113">Aby uzyskać więcej informacji, zobacz polecenie cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="df7cd-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="df7cd-114">Polecenie ostatnie tworzy usługę kontenera dla kontenera przechowywanego w $Container.</span><span class="sxs-lookup"><span data-stu-id="df7cd-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="df7cd-115">Usługa ma nazwę csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="df7cd-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="df7cd-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df7cd-116">PARAMETERS</span></span>

### <span data-ttu-id="df7cd-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="df7cd-117">-ContainerService</span></span>
<span data-ttu-id="df7cd-118">Określa obiekt usługi kontenera, który zawiera właściwości nowej usługi.</span><span class="sxs-lookup"><span data-stu-id="df7cd-118">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="df7cd-119">Aby uzyskać obiekt **ContainerService** , użyj polecenia cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="df7cd-119">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df7cd-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df7cd-120">-Name</span></span>
<span data-ttu-id="df7cd-121">Określa nazwę usługi kontenera, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df7cd-121">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="df7cd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df7cd-122">-ResourceGroupName</span></span>
<span data-ttu-id="df7cd-123">Określa grupę zasobów, w której to polecenie cmdlet wdraża usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="df7cd-123">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="df7cd-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df7cd-124">-Confirm</span></span>
<span data-ttu-id="df7cd-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df7cd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df7cd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df7cd-126">-WhatIf</span></span>
<span data-ttu-id="df7cd-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df7cd-127">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="df7cd-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="df7cd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df7cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7cd-129">CommonParameters</span></span>
<span data-ttu-id="df7cd-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df7cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7cd-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df7cd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7cd-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df7cd-132">INPUTS</span></span>

### <span data-ttu-id="df7cd-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="df7cd-133">None</span></span>
<span data-ttu-id="df7cd-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="df7cd-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df7cd-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df7cd-135">OUTPUTS</span></span>

## <span data-ttu-id="df7cd-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df7cd-136">NOTES</span></span>

## <span data-ttu-id="df7cd-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df7cd-137">RELATED LINKS</span></span>

[<span data-ttu-id="df7cd-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="df7cd-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="df7cd-139">Nowe — AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="df7cd-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="df7cd-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="df7cd-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="df7cd-141">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="df7cd-141">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


