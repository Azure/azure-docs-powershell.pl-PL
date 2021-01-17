---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371352"
---
# <span data-ttu-id="adc20-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="adc20-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="adc20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="adc20-102">SYNOPSIS</span></span>
<span data-ttu-id="adc20-103">Usuwanie zasad WAF</span><span class="sxs-lookup"><span data-stu-id="adc20-103">Remove WAF policy</span></span>

## <span data-ttu-id="adc20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="adc20-104">SYNTAX</span></span>

### <span data-ttu-id="adc20-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="adc20-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adc20-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adc20-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adc20-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="adc20-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adc20-108">Opis</span><span class="sxs-lookup"><span data-stu-id="adc20-108">DESCRIPTION</span></span>
<span data-ttu-id="adc20-109">Polecenie cmdlet **Remove-AzFrontDoorWafPolicy** usuwa zasadę WAF w ramach bieżącego abonamentu</span><span class="sxs-lookup"><span data-stu-id="adc20-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="adc20-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="adc20-110">EXAMPLES</span></span>

### <span data-ttu-id="adc20-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="adc20-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="adc20-112">Usuń zasady WAF o nazwie $policyName w $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="adc20-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="adc20-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="adc20-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="adc20-114">Usuń wszystkie zasady WAF w $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="adc20-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="adc20-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="adc20-115">PARAMETERS</span></span>

### <span data-ttu-id="adc20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc20-116">-DefaultProfile</span></span>
<span data-ttu-id="adc20-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="adc20-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adc20-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="adc20-118">-InputObject</span></span>
<span data-ttu-id="adc20-119">Obiekt zasady WAF, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="adc20-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adc20-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="adc20-120">-Name</span></span>
<span data-ttu-id="adc20-121">Nazwa zasad WAF, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="adc20-121">The name of the WAF policy to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc20-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adc20-122">-PassThru</span></span>
<span data-ttu-id="adc20-123">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="adc20-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="adc20-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc20-124">-ResourceGroupName</span></span>
<span data-ttu-id="adc20-125">Grupa zasobów, do której należy zasada WAF.</span><span class="sxs-lookup"><span data-stu-id="adc20-125">The resource group to which the WAF policy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc20-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adc20-126">-ResourceId</span></span>
<span data-ttu-id="adc20-127">Identyfikator zasobu zasady WAF do usunięcia</span><span class="sxs-lookup"><span data-stu-id="adc20-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc20-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="adc20-128">-Confirm</span></span>
<span data-ttu-id="adc20-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adc20-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adc20-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adc20-130">-WhatIf</span></span>
<span data-ttu-id="adc20-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adc20-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adc20-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="adc20-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adc20-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc20-133">CommonParameters</span></span>
<span data-ttu-id="adc20-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adc20-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc20-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adc20-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc20-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adc20-136">INPUTS</span></span>

### <span data-ttu-id="adc20-137">Microsoft. Azure. Commands. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="adc20-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="adc20-138">System. String</span><span class="sxs-lookup"><span data-stu-id="adc20-138">System.String</span></span>

## <span data-ttu-id="adc20-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="adc20-139">OUTPUTS</span></span>

### <span data-ttu-id="adc20-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="adc20-140">System.Boolean</span></span>

## <span data-ttu-id="adc20-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="adc20-141">NOTES</span></span>

## <span data-ttu-id="adc20-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="adc20-142">RELATED LINKS</span></span>

<span data-ttu-id="adc20-143">[Nowe — AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="adc20-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
