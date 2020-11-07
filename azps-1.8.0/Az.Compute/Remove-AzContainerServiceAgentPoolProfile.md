---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: dc1884d643bd2f3c58ae6cb68fe272a786bcde73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868991"
---
# <span data-ttu-id="c569f-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="c569f-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="c569f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c569f-102">SYNOPSIS</span></span>
<span data-ttu-id="c569f-103">Usuwa profil puli agentów z usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="c569f-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="c569f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c569f-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c569f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c569f-105">DESCRIPTION</span></span>
<span data-ttu-id="c569f-106">Polecenie cmdlet **Remove-AzContainerServiceAgentPoolProfile** usuwa profil puli agentów z usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="c569f-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="c569f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c569f-107">EXAMPLES</span></span>

### <span data-ttu-id="c569f-108">Przykład 1: Usuwanie profilu z usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="c569f-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="c569f-109">Pierwsze polecenie uzyskuje usługę kontenera o nazwie CSResourceGroup17 przy użyciu polecenia cmdlet Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="c569f-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="c569f-110">Polecenie zapisuje usługę w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="c569f-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="c569f-111">Drugie polecenie usuwa profil o nazwie AgentPool01 z usługi kontenera w $Container.</span><span class="sxs-lookup"><span data-stu-id="c569f-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="c569f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c569f-112">PARAMETERS</span></span>

### <span data-ttu-id="c569f-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="c569f-113">-ContainerService</span></span>
<span data-ttu-id="c569f-114">Określa obiekt usługi kontenera, z którego to polecenie cmdlet usuwa profil puli agentów.</span><span class="sxs-lookup"><span data-stu-id="c569f-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="c569f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c569f-115">-DefaultProfile</span></span>
<span data-ttu-id="c569f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c569f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c569f-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c569f-117">-Name</span></span>
<span data-ttu-id="c569f-118">Określa nazwę profilu puli agentów, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c569f-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c569f-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c569f-119">-Confirm</span></span>
<span data-ttu-id="c569f-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c569f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c569f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c569f-121">-WhatIf</span></span>
<span data-ttu-id="c569f-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c569f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c569f-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c569f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c569f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c569f-124">CommonParameters</span></span>
<span data-ttu-id="c569f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c569f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c569f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c569f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c569f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c569f-127">INPUTS</span></span>

### <span data-ttu-id="c569f-128">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="c569f-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="c569f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c569f-129">System.String</span></span>

## <span data-ttu-id="c569f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c569f-130">OUTPUTS</span></span>

### <span data-ttu-id="c569f-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="c569f-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="c569f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c569f-132">NOTES</span></span>

## <span data-ttu-id="c569f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c569f-133">RELATED LINKS</span></span>

[<span data-ttu-id="c569f-134">Dodaj-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="c569f-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="c569f-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="c569f-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


