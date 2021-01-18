---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 8319a5bc0251e744ee898658b0a0a541f0ce86ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501964"
---
# <span data-ttu-id="75529-101">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="75529-101">Add-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="75529-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75529-102">SYNOPSIS</span></span>
<span data-ttu-id="75529-103">Dodaje profil puli agenta usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="75529-103">Adds a container service agent pool profile.</span></span>

## <span data-ttu-id="75529-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75529-104">SYNTAX</span></span>

```
Add-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75529-105">Opis</span><span class="sxs-lookup"><span data-stu-id="75529-105">DESCRIPTION</span></span>
<span data-ttu-id="75529-106">Polecenie cmdlet **Add-AzContainerServiceAgentPoolProfile** umożliwia dodanie profilu puli agenta usługi kontenera do obiektu usługi kontenera lokalnego.</span><span class="sxs-lookup"><span data-stu-id="75529-106">The **Add-AzContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="75529-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75529-107">EXAMPLES</span></span>

### <span data-ttu-id="75529-108">Przykład 1. Dodaj profil</span><span class="sxs-lookup"><span data-stu-id="75529-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="75529-109">To polecenie dodaje profil puli agenta usługi kontenera do obiektu usługi kontenera lokalnego.</span><span class="sxs-lookup"><span data-stu-id="75529-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="75529-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75529-110">PARAMETERS</span></span>

### <span data-ttu-id="75529-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="75529-111">-ContainerService</span></span>
<span data-ttu-id="75529-112">Określa obiekt usługi kontenera, do którego ten aplet polecenia dodaje profil puli agentów.</span><span class="sxs-lookup"><span data-stu-id="75529-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="75529-113">Aby uzyskać obiekt **ContainerService** , użyj polecenia cmdlet [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="75529-113">To obtain a **ContainerService** object, use the [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75529-114">-Count</span><span class="sxs-lookup"><span data-stu-id="75529-114">-Count</span></span>
<span data-ttu-id="75529-115">Określa liczbę agentów obsługujących kontenery hosta.</span><span class="sxs-lookup"><span data-stu-id="75529-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="75529-116">Dopuszczalne wartości tego parametru to: liczba całkowita z zakresu od 1 do 100.</span><span class="sxs-lookup"><span data-stu-id="75529-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="75529-117">Wartością domyślną jest 1.</span><span class="sxs-lookup"><span data-stu-id="75529-117">The default value is 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75529-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75529-118">-DefaultProfile</span></span>
<span data-ttu-id="75529-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="75529-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75529-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="75529-120">-DnsPrefix</span></span>
<span data-ttu-id="75529-121">Określa prefiks DNS, którego używa polecenie cmdlet do utworzenia w pełni kwalifikowanej nazwy domeny dla tej puli agentów.</span><span class="sxs-lookup"><span data-stu-id="75529-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75529-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="75529-122">-Name</span></span>
<span data-ttu-id="75529-123">Określa nazwę profilu puli agentów.</span><span class="sxs-lookup"><span data-stu-id="75529-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="75529-124">Ta wartość musi być unikatowa w kontekście subskrypcji i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="75529-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75529-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="75529-125">-VmSize</span></span>
<span data-ttu-id="75529-126">Określa rozmiar maszyn wirtualnych dla agentów.</span><span class="sxs-lookup"><span data-stu-id="75529-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75529-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="75529-127">-Confirm</span></span>
<span data-ttu-id="75529-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75529-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75529-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75529-129">-WhatIf</span></span>
<span data-ttu-id="75529-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75529-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75529-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="75529-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75529-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75529-132">CommonParameters</span></span>
<span data-ttu-id="75529-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75529-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75529-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75529-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75529-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75529-135">INPUTS</span></span>

### <span data-ttu-id="75529-136">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="75529-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="75529-137">System. String</span><span class="sxs-lookup"><span data-stu-id="75529-137">System.String</span></span>

### <span data-ttu-id="75529-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="75529-138">System.Int32</span></span>

## <span data-ttu-id="75529-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75529-139">OUTPUTS</span></span>

### <span data-ttu-id="75529-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="75529-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="75529-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75529-141">NOTES</span></span>

## <span data-ttu-id="75529-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75529-142">RELATED LINKS</span></span>

[<span data-ttu-id="75529-143">Nowe — AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="75529-143">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="75529-144">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="75529-144">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)
