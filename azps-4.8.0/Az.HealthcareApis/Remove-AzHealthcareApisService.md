---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 12db158089473c5f0cfb01e24b762ecf192f8991
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222341"
---
# <span data-ttu-id="4a04e-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="4a04e-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="4a04e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a04e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a04e-103">Usuwa wystąpienie usługi.</span><span class="sxs-lookup"><span data-stu-id="4a04e-103">Deletes a service instance.</span></span>

## <span data-ttu-id="4a04e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a04e-104">SYNTAX</span></span>

### <span data-ttu-id="4a04e-105">ServiceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4a04e-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a04e-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a04e-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a04e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a04e-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a04e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4a04e-108">DESCRIPTION</span></span>
<span data-ttu-id="4a04e-109">Usuwa wystąpienie usługi.</span><span class="sxs-lookup"><span data-stu-id="4a04e-109">Deletes a service instance.</span></span>

## <span data-ttu-id="4a04e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a04e-110">EXAMPLES</span></span>

### <span data-ttu-id="4a04e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4a04e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="4a04e-112">Usuwa istniejącą usługę HealthcareApis o podanej nazwie w podanej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="4a04e-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="4a04e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4a04e-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="4a04e-114">Usuwa istniejącą usługę HealthcareApis z podanym identyfikatorem ResourceId.</span><span class="sxs-lookup"><span data-stu-id="4a04e-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="4a04e-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4a04e-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="4a04e-116">Usuwa podany obiekt usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="4a04e-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="4a04e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a04e-117">PARAMETERS</span></span>

### <span data-ttu-id="4a04e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a04e-118">-AsJob</span></span>
<span data-ttu-id="4a04e-119">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="4a04e-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="4a04e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a04e-120">-DefaultProfile</span></span>
<span data-ttu-id="4a04e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a04e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a04e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4a04e-122">-InputObject</span></span>
<span data-ttu-id="4a04e-123">Obiekt usługi HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4a04e-123">HealthcareApis service object</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a04e-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4a04e-124">-Name</span></span>
<span data-ttu-id="4a04e-125">Nazwa usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="4a04e-125">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a04e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a04e-126">-PassThru</span></span>
<span data-ttu-id="4a04e-127">Jeśli ta funkcja jest podana, zwraca wartość PRAWDA, jeśli operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="4a04e-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="4a04e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a04e-128">-ResourceGroupName</span></span>
<span data-ttu-id="4a04e-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4a04e-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a04e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a04e-130">-ResourceId</span></span>
<span data-ttu-id="4a04e-131">Identyfikator zasobu usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="4a04e-131">HealthcareApis Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a04e-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a04e-132">-Confirm</span></span>
<span data-ttu-id="4a04e-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a04e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a04e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a04e-134">-WhatIf</span></span>
<span data-ttu-id="4a04e-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a04e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a04e-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4a04e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a04e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a04e-137">CommonParameters</span></span>
<span data-ttu-id="4a04e-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a04e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a04e-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a04e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a04e-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a04e-140">INPUTS</span></span>

### <span data-ttu-id="4a04e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4a04e-141">System.String</span></span>

### <span data-ttu-id="4a04e-142">Microsoft. Azure. Commands. HealthcareApisService. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="4a04e-142">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="4a04e-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a04e-143">OUTPUTS</span></span>

### <span data-ttu-id="4a04e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a04e-144">System.Boolean</span></span>

## <span data-ttu-id="4a04e-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a04e-145">NOTES</span></span>

## <span data-ttu-id="4a04e-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a04e-146">RELATED LINKS</span></span>
