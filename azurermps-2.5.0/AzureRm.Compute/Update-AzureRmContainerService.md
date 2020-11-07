---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 9a199a0aa0e31cf8bc57585d4825a33e10b5bfc1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899352"
---
# <span data-ttu-id="2b2b6-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2b2b6-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="2b2b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b2b6-102">SYNOPSIS</span></span>
<span data-ttu-id="2b2b6-103">Umożliwia zaktualizowanie stanu usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b2b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b2b6-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b2b6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b2b6-105">DESCRIPTION</span></span>
<span data-ttu-id="2b2b6-106">Polecenie cmdlet **Update-AzureRmContainerService** aktualizuje stan usługi kontenera, aby pasował do lokalnego wystąpienia usługi.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="2b2b6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b2b6-107">EXAMPLES</span></span>

### <span data-ttu-id="2b2b6-108">Przykład 1: aktualizowanie usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="2b2b6-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="2b2b6-109">To polecenie pobiera usługę kontenera o nazwie CSResourceGroup17 przy użyciu polecenia cmdlet Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="2b2b6-110">Polecenie przekazuje ten obiekt do polecenia cmdlet Remove-AzureRmContainerServiceAgentPoolProfile przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="2b2b6-111">**Remove-AzureRmContainerServiceAgentPoolProfile** usuwa profil o nazwie AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="2b2b6-112">Polecenie przekazuje wynik do polecenia cmdlet Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="2b2b6-113">Polecenie **Add-AzureRmContainerServiceAgentPoolProfile** dodaje profil o nazwie AgentPool01 i ma określone właściwości.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="2b2b6-114">Polecenie przekazuje wynik do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="2b2b6-115">Bieżące polecenie cmdlet powoduje zaktualizowanie usługi kontenera w celu odzwierciedlenia zmian wprowadzonych w tym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="2b2b6-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b2b6-116">PARAMETERS</span></span>

### <span data-ttu-id="2b2b6-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b2b6-117">-AsJob</span></span>
<span data-ttu-id="2b2b6-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2b2b6-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b2b6-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="2b2b6-119">-ContainerService</span></span>
<span data-ttu-id="2b2b6-120">Określa lokalny obiekt **ContainerService** , który zawiera zmiany.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-120">Specifies a local **ContainerService** object that contains changes.</span></span>

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

### <span data-ttu-id="2b2b6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b2b6-121">-DefaultProfile</span></span>
<span data-ttu-id="2b2b6-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b2b6-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b2b6-123">-Name</span></span>
<span data-ttu-id="2b2b6-124">Określa nazwę usługi kontenera, która jest aktualizowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="2b2b6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b2b6-125">-ResourceGroupName</span></span>
<span data-ttu-id="2b2b6-126">Określa grupę zasobów usługi kontenera, które są aktualizowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="2b2b6-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b2b6-127">-Confirm</span></span>
<span data-ttu-id="2b2b6-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b2b6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b2b6-129">-WhatIf</span></span>
<span data-ttu-id="2b2b6-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2b2b6-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b2b6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b2b6-132">CommonParameters</span></span>
<span data-ttu-id="2b2b6-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b2b6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b2b6-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b2b6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b2b6-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b2b6-135">INPUTS</span></span>

### <span data-ttu-id="2b2b6-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="2b2b6-136">ContainerService</span></span>
<span data-ttu-id="2b2b6-137">Parametr "ContainerService" akceptuje wartość typu "ContainerService" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="2b2b6-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="2b2b6-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b2b6-138">OUTPUTS</span></span>

### <span data-ttu-id="2b2b6-139">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="2b2b6-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="2b2b6-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b2b6-140">NOTES</span></span>

## <span data-ttu-id="2b2b6-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b2b6-141">RELATED LINKS</span></span>

[<span data-ttu-id="2b2b6-142">Dodaj-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="2b2b6-142">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="2b2b6-143">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2b2b6-143">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="2b2b6-144">Nowe — AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2b2b6-144">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="2b2b6-145">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2b2b6-145">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="2b2b6-146">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="2b2b6-146">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


