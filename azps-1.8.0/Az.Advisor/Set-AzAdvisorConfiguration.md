---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: 4c3a3fd8f80bf1f8a18f65a8dc5c9d0bf26b6d9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704723"
---
# <span data-ttu-id="da6ca-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="da6ca-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="da6ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da6ca-102">SYNOPSIS</span></span>
<span data-ttu-id="da6ca-103">Aktualizuje lub tworzy konfigurację usługi Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="da6ca-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="da6ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da6ca-104">SYNTAX</span></span>

### <span data-ttu-id="da6ca-105">InputObjectRgExcludeParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da6ca-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da6ca-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="da6ca-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da6ca-107">Opis</span><span class="sxs-lookup"><span data-stu-id="da6ca-107">DESCRIPTION</span></span>
<span data-ttu-id="da6ca-108">Służy do aktualizowania konfiguracji usługi Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="da6ca-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="da6ca-109">Dostępne są dwa typy konfiguracji: Konfiguracja poziomu abonamentu i konfiguracja poziomu zasobów.</span><span class="sxs-lookup"><span data-stu-id="da6ca-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="da6ca-110">Konfiguracja poziomu abonamentu: dla tego typu subskrypcji może istnieć tylko jedna konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="da6ca-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="da6ca-111">Właściwości LowCpuThreshold i Exclude można aktualizować przy użyciu tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da6ca-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="da6ca-112">Konfiguracja poziomu zasobów źródłowych: dla każdego z nich może istnieć tylko jedna konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="da6ca-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="da6ca-113">Za pomocą tego polecenia cmdlet można aktualizować tylko Właściwość Exclude.</span><span class="sxs-lookup"><span data-stu-id="da6ca-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="da6ca-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da6ca-114">EXAMPLES</span></span>

###  <span data-ttu-id="da6ca-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da6ca-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="da6ca-116">Umożliwia zaktualizowanie konfiguracji (lowCpuThreshold) konfiguracji poziomu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="da6ca-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="da6ca-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="da6ca-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="da6ca-118">Umożliwia zaktualizowanie konfiguracji (lowCpuThreshold, wykluczanie) dla konfiguracji poziomu abonamentu i wyłączenie z generacji rekomendacji.</span><span class="sxs-lookup"><span data-stu-id="da6ca-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="da6ca-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="da6ca-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="da6ca-120">Umożliwia zaktualizowanie konfiguracji (Wyklucz) dla resourceGroupName1 w celu wykluczenia jej z generacji rekomendacji.</span><span class="sxs-lookup"><span data-stu-id="da6ca-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="da6ca-121">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="da6ca-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="da6ca-122">Aktualizuje konfigurację dla danego rekomendacja przekazana w potoku.</span><span class="sxs-lookup"><span data-stu-id="da6ca-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="da6ca-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da6ca-123">PARAMETERS</span></span>

### <span data-ttu-id="da6ca-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da6ca-124">-Confirm</span></span>
<span data-ttu-id="da6ca-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da6ca-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da6ca-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da6ca-126">-DefaultProfile</span></span>
<span data-ttu-id="da6ca-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da6ca-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da6ca-128">-Wyklucz</span><span class="sxs-lookup"><span data-stu-id="da6ca-128">-Exclude</span></span>
<span data-ttu-id="da6ca-129">Wyklucz z generacji rekomendacji.</span><span class="sxs-lookup"><span data-stu-id="da6ca-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="da6ca-130">Jeśli właściwość Exclude nie zostanie określona, zostanie ustawiona wartość FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="da6ca-130">If not specified exclude property will be set to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da6ca-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="da6ca-131">-InputObject</span></span>
<span data-ttu-id="da6ca-132">Typ obiektu programu PowerShell PsAzureAdvisorConfigurationData zwrócony przez połączenie Get-AzAdvisorConfiguration.</span><span class="sxs-lookup"><span data-stu-id="da6ca-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

```yaml
Type: PsAzureAdvisorConfigurationData
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da6ca-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="da6ca-133">-LowCpuThreshold</span></span>
<span data-ttu-id="da6ca-134">Wartość określająca niski próg procesora.</span><span class="sxs-lookup"><span data-stu-id="da6ca-134">Value for Low Cpu threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: InputObjectLowCpuExcludeParameterSet
Aliases:
Accepted values: 0, 5, 10, 15, 20

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da6ca-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da6ca-135">-ResourceGroupName</span></span>
<span data-ttu-id="da6ca-136">Nazwa grupy zasobów konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="da6ca-136">Resource Group name for the configuration.</span></span>

```yaml
Type: String
Parameter Sets: InputObjectRgExcludeParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da6ca-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da6ca-137">-WhatIf</span></span>
<span data-ttu-id="da6ca-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da6ca-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da6ca-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da6ca-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da6ca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da6ca-140">CommonParameters</span></span>
<span data-ttu-id="da6ca-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da6ca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="da6ca-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da6ca-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da6ca-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da6ca-143">INPUTS</span></span>

### <span data-ttu-id="da6ca-144">Microsoft. Azure. Commands. Advisor. cmdlet. models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="da6ca-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="da6ca-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da6ca-145">OUTPUTS</span></span>

### <span data-ttu-id="da6ca-146">Microsoft. Azure. Commands. Advisor. cmdlet. models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="da6ca-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="da6ca-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da6ca-147">NOTES</span></span>

## <span data-ttu-id="da6ca-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da6ca-148">RELATED LINKS</span></span>
