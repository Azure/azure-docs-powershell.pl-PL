---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: bacc9366292225e07fd07ac65726018f1d1879e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526225"
---
# <span data-ttu-id="9efeb-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9efeb-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="9efeb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9efeb-102">SYNOPSIS</span></span>
<span data-ttu-id="9efeb-103">Umożliwia zaktualizowanie stanu usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="9efeb-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9efeb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9efeb-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9efeb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9efeb-105">DESCRIPTION</span></span>
<span data-ttu-id="9efeb-106">Polecenie cmdlet **Update-AzureRmContainerService** aktualizuje stan usługi kontenera, aby pasował do lokalnego wystąpienia usługi.</span><span class="sxs-lookup"><span data-stu-id="9efeb-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="9efeb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9efeb-107">EXAMPLES</span></span>

### <span data-ttu-id="9efeb-108">Przykład 1: aktualizowanie usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="9efeb-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="9efeb-109">To polecenie pobiera usługę kontenera o nazwie CSResourceGroup17 przy użyciu polecenia cmdlet Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="9efeb-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="9efeb-110">Polecenie przekazuje ten obiekt do polecenia cmdlet Remove-AzureRmContainerServiceAgentPoolProfile przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="9efeb-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9efeb-111">**Remove-AzureRmContainerServiceAgentPoolProfile** usuwa profil o nazwie AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="9efeb-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="9efeb-112">Polecenie przekazuje wynik do polecenia cmdlet Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="9efeb-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="9efeb-113">Polecenie **Add-AzureRmContainerServiceAgentPoolProfile** dodaje profil o nazwie AgentPool01 i ma określone właściwości.</span><span class="sxs-lookup"><span data-stu-id="9efeb-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="9efeb-114">Polecenie przekazuje wynik do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9efeb-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="9efeb-115">Bieżące polecenie cmdlet powoduje zaktualizowanie usługi kontenera w celu odzwierciedlenia zmian wprowadzonych w tym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="9efeb-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="9efeb-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9efeb-116">PARAMETERS</span></span>

### <span data-ttu-id="9efeb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9efeb-117">-AsJob</span></span>
<span data-ttu-id="9efeb-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9efeb-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9efeb-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="9efeb-119">-ContainerService</span></span>
<span data-ttu-id="9efeb-120">Określa lokalny obiekt **ContainerService** , który zawiera zmiany.</span><span class="sxs-lookup"><span data-stu-id="9efeb-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9efeb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9efeb-121">-DefaultProfile</span></span>
<span data-ttu-id="9efeb-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9efeb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9efeb-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9efeb-123">-Name</span></span>
<span data-ttu-id="9efeb-124">Określa nazwę usługi kontenera, która jest aktualizowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9efeb-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efeb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9efeb-125">-ResourceGroupName</span></span>
<span data-ttu-id="9efeb-126">Określa grupę zasobów usługi kontenera, które są aktualizowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9efeb-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="9efeb-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9efeb-127">-Confirm</span></span>
<span data-ttu-id="9efeb-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9efeb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9efeb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9efeb-129">-WhatIf</span></span>
<span data-ttu-id="9efeb-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9efeb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9efeb-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9efeb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9efeb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9efeb-132">CommonParameters</span></span>
<span data-ttu-id="9efeb-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9efeb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9efeb-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9efeb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9efeb-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9efeb-135">INPUTS</span></span>

### <span data-ttu-id="9efeb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9efeb-136">System.String</span></span>

### <span data-ttu-id="9efeb-137">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="9efeb-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>
<span data-ttu-id="9efeb-138">Parametry: ContainerService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9efeb-138">Parameters: ContainerService (ByValue)</span></span>

## <span data-ttu-id="9efeb-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9efeb-139">OUTPUTS</span></span>

### <span data-ttu-id="9efeb-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="9efeb-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="9efeb-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9efeb-141">NOTES</span></span>

## <span data-ttu-id="9efeb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9efeb-142">RELATED LINKS</span></span>

[<span data-ttu-id="9efeb-143">Dodaj-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="9efeb-143">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="9efeb-144">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9efeb-144">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="9efeb-145">Nowe — AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9efeb-145">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="9efeb-146">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9efeb-146">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="9efeb-147">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="9efeb-147">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


