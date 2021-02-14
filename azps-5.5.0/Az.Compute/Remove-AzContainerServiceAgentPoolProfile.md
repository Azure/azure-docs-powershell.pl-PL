---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: b887110ecb0cd941af9c91417218ec2ca297be1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244091"
---
# <span data-ttu-id="978a5-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="978a5-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="978a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="978a5-102">SYNOPSIS</span></span>
<span data-ttu-id="978a5-103">Usuwa profil puli agenta z usługi kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="978a5-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="978a5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="978a5-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="978a5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="978a5-105">DESCRIPTION</span></span>
<span data-ttu-id="978a5-106">Polecenie **cmdlet Remove-AzContainerServiceAgentPoolProfile** usuwa profil puli agenta z usługi kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="978a5-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="978a5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="978a5-107">EXAMPLES</span></span>

### <span data-ttu-id="978a5-108">Przykład 1. Usuwanie profilu z usługi kontenerowej</span><span class="sxs-lookup"><span data-stu-id="978a5-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="978a5-109">Pierwsze polecenie pobiera usługę kontenera o nazwie CSResourceGroup17 przy użyciu Get-AzContainerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="978a5-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="978a5-110">Polecenie przechowuje usługę w $Container zmienną.</span><span class="sxs-lookup"><span data-stu-id="978a5-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="978a5-111">Drugie polecenie usuwa profil o nazwie AgentPool01 z usługi kontenerów w $Container.</span><span class="sxs-lookup"><span data-stu-id="978a5-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="978a5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="978a5-112">PARAMETERS</span></span>

### <span data-ttu-id="978a5-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="978a5-113">-ContainerService</span></span>
<span data-ttu-id="978a5-114">Określa obiekt usługi kontener, z którego to polecenie cmdlet usuwa profil puli agenta.</span><span class="sxs-lookup"><span data-stu-id="978a5-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="978a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978a5-115">-DefaultProfile</span></span>
<span data-ttu-id="978a5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="978a5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="978a5-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="978a5-117">-Name</span></span>
<span data-ttu-id="978a5-118">Określa nazwę profilu puli agenta, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="978a5-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="978a5-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="978a5-119">-Confirm</span></span>
<span data-ttu-id="978a5-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="978a5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="978a5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="978a5-121">-WhatIf</span></span>
<span data-ttu-id="978a5-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="978a5-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="978a5-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="978a5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="978a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978a5-124">CommonParameters</span></span>
<span data-ttu-id="978a5-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="978a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978a5-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="978a5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978a5-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="978a5-127">INPUTS</span></span>

### <span data-ttu-id="978a5-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="978a5-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="978a5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="978a5-129">System.String</span></span>

## <span data-ttu-id="978a5-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="978a5-130">OUTPUTS</span></span>

### <span data-ttu-id="978a5-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="978a5-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="978a5-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="978a5-132">NOTES</span></span>

## <span data-ttu-id="978a5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="978a5-133">RELATED LINKS</span></span>

[<span data-ttu-id="978a5-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="978a5-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="978a5-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="978a5-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


