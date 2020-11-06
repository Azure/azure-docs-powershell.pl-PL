---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: a5ce087e8ebf768b63d09a4002c3aaf38ddd9f84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554000"
---
# <span data-ttu-id="c3e04-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="c3e04-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="c3e04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3e04-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e04-103">Dodaje profil puli agenta usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="c3e04-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3e04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3e04-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3e04-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c3e04-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e04-106">Polecenie cmdlet **Add-AzureRmContainerServiceAgentPoolProfile** umożliwia dodanie profilu puli agenta usługi kontenera do obiektu usługi kontenera lokalnego.</span><span class="sxs-lookup"><span data-stu-id="c3e04-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="c3e04-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3e04-107">EXAMPLES</span></span>

### <span data-ttu-id="c3e04-108">Przykład 1. Dodaj profil</span><span class="sxs-lookup"><span data-stu-id="c3e04-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="c3e04-109">To polecenie dodaje profil puli agenta usługi kontenera do obiektu usługi kontenera lokalnego.</span><span class="sxs-lookup"><span data-stu-id="c3e04-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="c3e04-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3e04-110">PARAMETERS</span></span>

### <span data-ttu-id="c3e04-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="c3e04-111">-ContainerService</span></span>
<span data-ttu-id="c3e04-112">Określa obiekt usługi kontenera, do którego ten aplet polecenia dodaje profil puli agentów.</span><span class="sxs-lookup"><span data-stu-id="c3e04-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="c3e04-113">Aby uzyskać obiekt **ContainerService** , użyj polecenia cmdlet [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="c3e04-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="c3e04-114">-Count</span><span class="sxs-lookup"><span data-stu-id="c3e04-114">-Count</span></span>
<span data-ttu-id="c3e04-115">Określa liczbę agentów obsługujących kontenery hosta.</span><span class="sxs-lookup"><span data-stu-id="c3e04-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="c3e04-116">Dopuszczalne wartości tego parametru to: liczba całkowita z zakresu od 1 do 100.</span><span class="sxs-lookup"><span data-stu-id="c3e04-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="c3e04-117">Wartością domyślną jest 1.</span><span class="sxs-lookup"><span data-stu-id="c3e04-117">The default value is 1.</span></span>

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

### <span data-ttu-id="c3e04-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e04-118">-DefaultProfile</span></span>
<span data-ttu-id="c3e04-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e04-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3e04-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="c3e04-120">-DnsPrefix</span></span>
<span data-ttu-id="c3e04-121">Określa prefiks DNS, którego używa polecenie cmdlet do utworzenia w pełni kwalifikowanej nazwy domeny dla tej puli agentów.</span><span class="sxs-lookup"><span data-stu-id="c3e04-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="c3e04-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c3e04-122">-Name</span></span>
<span data-ttu-id="c3e04-123">Określa nazwę profilu puli agentów.</span><span class="sxs-lookup"><span data-stu-id="c3e04-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="c3e04-124">Ta wartość musi być unikatowa w kontekście subskrypcji i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c3e04-124">This value must be unique in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="c3e04-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="c3e04-125">-VmSize</span></span>
<span data-ttu-id="c3e04-126">Określa rozmiar maszyn wirtualnych dla agentów.</span><span class="sxs-lookup"><span data-stu-id="c3e04-126">Specifies the size of the virtual machines for the agents.</span></span>

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

### <span data-ttu-id="c3e04-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3e04-127">-Confirm</span></span>
<span data-ttu-id="c3e04-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3e04-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3e04-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e04-129">-WhatIf</span></span>
<span data-ttu-id="c3e04-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3e04-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3e04-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c3e04-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3e04-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e04-132">CommonParameters</span></span>
<span data-ttu-id="c3e04-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e04-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e04-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e04-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e04-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3e04-135">INPUTS</span></span>

## <span data-ttu-id="c3e04-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3e04-136">OUTPUTS</span></span>

## <span data-ttu-id="c3e04-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3e04-137">NOTES</span></span>

## <span data-ttu-id="c3e04-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3e04-138">RELATED LINKS</span></span>

[<span data-ttu-id="c3e04-139">Nowe — AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="c3e04-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="c3e04-140">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="c3e04-140">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
