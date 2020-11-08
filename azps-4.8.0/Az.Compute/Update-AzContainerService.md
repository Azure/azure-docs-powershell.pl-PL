---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 199b61bc8ef075aabc09870cde436a0e49598ee8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221363"
---
# <span data-ttu-id="865bc-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="865bc-101">Update-AzContainerService</span></span>

## <span data-ttu-id="865bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="865bc-102">SYNOPSIS</span></span>
<span data-ttu-id="865bc-103">Umożliwia zaktualizowanie stanu usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="865bc-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="865bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="865bc-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="865bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="865bc-105">DESCRIPTION</span></span>
<span data-ttu-id="865bc-106">Polecenie cmdlet **Update-AzContainerService** aktualizuje stan usługi kontenera, aby pasował do lokalnego wystąpienia usługi.</span><span class="sxs-lookup"><span data-stu-id="865bc-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="865bc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="865bc-107">EXAMPLES</span></span>

### <span data-ttu-id="865bc-108">Przykład 1: aktualizowanie usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="865bc-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="865bc-109">To polecenie pobiera usługę kontenera o nazwie CSResourceGroup17 przy użyciu polecenia cmdlet Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="865bc-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="865bc-110">Polecenie przekazuje ten obiekt do polecenia cmdlet Remove-AzContainerServiceAgentPoolProfile przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="865bc-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="865bc-111">**Remove-AzContainerServiceAgentPoolProfile** usuwa profil o nazwie AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="865bc-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="865bc-112">Polecenie przekazuje wynik do polecenia cmdlet Add-AzContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="865bc-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="865bc-113">Polecenie **Add-AzContainerServiceAgentPoolProfile** dodaje profil o nazwie AgentPool01 i ma określone właściwości.</span><span class="sxs-lookup"><span data-stu-id="865bc-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="865bc-114">Polecenie przekazuje wynik do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="865bc-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="865bc-115">Bieżące polecenie cmdlet powoduje zaktualizowanie usługi kontenera w celu odzwierciedlenia zmian wprowadzonych w tym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="865bc-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="865bc-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="865bc-116">PARAMETERS</span></span>

### <span data-ttu-id="865bc-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="865bc-117">-AsJob</span></span>
<span data-ttu-id="865bc-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="865bc-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="865bc-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="865bc-119">-ContainerService</span></span>
<span data-ttu-id="865bc-120">Określa lokalny obiekt **ContainerService** , który zawiera zmiany.</span><span class="sxs-lookup"><span data-stu-id="865bc-120">Specifies a local **ContainerService** object that contains changes.</span></span>

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

### <span data-ttu-id="865bc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="865bc-121">-DefaultProfile</span></span>
<span data-ttu-id="865bc-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="865bc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="865bc-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="865bc-123">-Name</span></span>
<span data-ttu-id="865bc-124">Określa nazwę usługi kontenera, która jest aktualizowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="865bc-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="865bc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="865bc-125">-ResourceGroupName</span></span>
<span data-ttu-id="865bc-126">Określa grupę zasobów usługi kontenera, które są aktualizowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="865bc-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="865bc-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="865bc-127">-Confirm</span></span>
<span data-ttu-id="865bc-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="865bc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="865bc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="865bc-129">-WhatIf</span></span>
<span data-ttu-id="865bc-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="865bc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="865bc-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="865bc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="865bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="865bc-132">CommonParameters</span></span>
<span data-ttu-id="865bc-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="865bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="865bc-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="865bc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="865bc-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="865bc-135">INPUTS</span></span>

### <span data-ttu-id="865bc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="865bc-136">System.String</span></span>

### <span data-ttu-id="865bc-137">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="865bc-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="865bc-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="865bc-138">OUTPUTS</span></span>

### <span data-ttu-id="865bc-139">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="865bc-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="865bc-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="865bc-140">NOTES</span></span>

## <span data-ttu-id="865bc-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="865bc-141">RELATED LINKS</span></span>

[<span data-ttu-id="865bc-142">Dodaj-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="865bc-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="865bc-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="865bc-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="865bc-144">Nowe — AzContainerService</span><span class="sxs-lookup"><span data-stu-id="865bc-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="865bc-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="865bc-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="865bc-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="865bc-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


