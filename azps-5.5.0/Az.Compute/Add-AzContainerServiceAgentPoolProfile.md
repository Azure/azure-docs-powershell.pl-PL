---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 8319a5bc0251e744ee898658b0a0a541f0ce86ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177786"
---
# <span data-ttu-id="61c39-101">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="61c39-101">Add-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="61c39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61c39-102">SYNOPSIS</span></span>
<span data-ttu-id="61c39-103">Dodaje profil puli agenta usługi kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="61c39-103">Adds a container service agent pool profile.</span></span>

## <span data-ttu-id="61c39-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="61c39-104">SYNTAX</span></span>

```
Add-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61c39-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="61c39-105">DESCRIPTION</span></span>
<span data-ttu-id="61c39-106">Polecenie **cmdlet Add-AzContainerServiceAgentPoolProfile** dodaje profil agenta usługi kontenerowej do obiektu usługi kontenera lokalnego.</span><span class="sxs-lookup"><span data-stu-id="61c39-106">The **Add-AzContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="61c39-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="61c39-107">EXAMPLES</span></span>

### <span data-ttu-id="61c39-108">Przykład 1. Dodawanie profilu</span><span class="sxs-lookup"><span data-stu-id="61c39-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="61c39-109">To polecenie dodaje profil puli agenta usługi kontenerów do obiektu usługi kontenera lokalnego.</span><span class="sxs-lookup"><span data-stu-id="61c39-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="61c39-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61c39-110">PARAMETERS</span></span>

### <span data-ttu-id="61c39-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="61c39-111">-ContainerService</span></span>
<span data-ttu-id="61c39-112">Określa obiekt usługi kontenerów, do którego to polecenie cmdlet dodaje profil puli agenta.</span><span class="sxs-lookup"><span data-stu-id="61c39-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="61c39-113">Aby uzyskać obiekt **ContainerService,** użyj polecenia cmdlet [New-AzContainerServiceConfig.](./New-AzContainerServiceConfig.md)</span><span class="sxs-lookup"><span data-stu-id="61c39-113">To obtain a **ContainerService** object, use the [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="61c39-114">— Liczba</span><span class="sxs-lookup"><span data-stu-id="61c39-114">-Count</span></span>
<span data-ttu-id="61c39-115">Określa liczbę agentów hostujących kontenery.</span><span class="sxs-lookup"><span data-stu-id="61c39-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="61c39-116">Dopuszczalne wartości dla tego parametru to liczby całkowite z od 1 do 100.</span><span class="sxs-lookup"><span data-stu-id="61c39-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="61c39-117">Wartość domyślna to 1.</span><span class="sxs-lookup"><span data-stu-id="61c39-117">The default value is 1.</span></span>

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

### <span data-ttu-id="61c39-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c39-118">-DefaultProfile</span></span>
<span data-ttu-id="61c39-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="61c39-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61c39-120">- DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="61c39-120">-DnsPrefix</span></span>
<span data-ttu-id="61c39-121">Określa prefiks DNS używany przez to polecenie cmdlet do utworzenia w pełni kwalifikowanej nazwy domeny dla tej puli agentów.</span><span class="sxs-lookup"><span data-stu-id="61c39-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="61c39-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="61c39-122">-Name</span></span>
<span data-ttu-id="61c39-123">Określa nazwę profilu puli agenta.</span><span class="sxs-lookup"><span data-stu-id="61c39-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="61c39-124">Ta wartość musi być unikatowa w kontekście grupy subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="61c39-124">This value must be unique in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="61c39-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="61c39-125">-VmSize</span></span>
<span data-ttu-id="61c39-126">Określa rozmiar maszyn wirtualnych dla agentów.</span><span class="sxs-lookup"><span data-stu-id="61c39-126">Specifies the size of the virtual machines for the agents.</span></span>

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

### <span data-ttu-id="61c39-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61c39-127">-Confirm</span></span>
<span data-ttu-id="61c39-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="61c39-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61c39-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61c39-129">-WhatIf</span></span>
<span data-ttu-id="61c39-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61c39-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61c39-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="61c39-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61c39-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c39-132">CommonParameters</span></span>
<span data-ttu-id="61c39-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61c39-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c39-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61c39-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c39-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61c39-135">INPUTS</span></span>

### <span data-ttu-id="61c39-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="61c39-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="61c39-137">System.String</span><span class="sxs-lookup"><span data-stu-id="61c39-137">System.String</span></span>

### <span data-ttu-id="61c39-138">System.Int32</span><span class="sxs-lookup"><span data-stu-id="61c39-138">System.Int32</span></span>

## <span data-ttu-id="61c39-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61c39-139">OUTPUTS</span></span>

### <span data-ttu-id="61c39-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="61c39-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="61c39-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="61c39-141">NOTES</span></span>

## <span data-ttu-id="61c39-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61c39-142">RELATED LINKS</span></span>

[<span data-ttu-id="61c39-143">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="61c39-143">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="61c39-144">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="61c39-144">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)
