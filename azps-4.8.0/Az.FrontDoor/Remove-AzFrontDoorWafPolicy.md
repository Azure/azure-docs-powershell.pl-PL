---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062218"
---
# <span data-ttu-id="deafc-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="deafc-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="deafc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="deafc-102">SYNOPSIS</span></span>
<span data-ttu-id="deafc-103">Usuwanie zasad WAF</span><span class="sxs-lookup"><span data-stu-id="deafc-103">Remove WAF policy</span></span>

## <span data-ttu-id="deafc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="deafc-104">SYNTAX</span></span>

### <span data-ttu-id="deafc-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="deafc-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deafc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="deafc-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deafc-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="deafc-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deafc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="deafc-108">DESCRIPTION</span></span>
<span data-ttu-id="deafc-109">Polecenie cmdlet **Remove-AzFrontDoorWafPolicy** usuwa zasadę WAF w ramach bieżącego abonamentu</span><span class="sxs-lookup"><span data-stu-id="deafc-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="deafc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="deafc-110">EXAMPLES</span></span>

### <span data-ttu-id="deafc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="deafc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="deafc-112">Usuń zasady WAF o nazwie $policyName w $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="deafc-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="deafc-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="deafc-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="deafc-114">Usuń wszystkie zasady WAF w $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="deafc-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="deafc-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="deafc-115">PARAMETERS</span></span>

### <span data-ttu-id="deafc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deafc-116">-DefaultProfile</span></span>
<span data-ttu-id="deafc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="deafc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deafc-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="deafc-118">-InputObject</span></span>
<span data-ttu-id="deafc-119">Obiekt zasady WAF, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="deafc-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="deafc-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="deafc-120">-Name</span></span>
<span data-ttu-id="deafc-121">Nazwa zasad WAF, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="deafc-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="deafc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="deafc-122">-PassThru</span></span>
<span data-ttu-id="deafc-123">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="deafc-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="deafc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deafc-124">-ResourceGroupName</span></span>
<span data-ttu-id="deafc-125">Grupa zasobów, do której należy zasada WAF.</span><span class="sxs-lookup"><span data-stu-id="deafc-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="deafc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="deafc-126">-ResourceId</span></span>
<span data-ttu-id="deafc-127">Identyfikator zasobu zasady WAF do usunięcia</span><span class="sxs-lookup"><span data-stu-id="deafc-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="deafc-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="deafc-128">-Confirm</span></span>
<span data-ttu-id="deafc-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deafc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deafc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deafc-130">-WhatIf</span></span>
<span data-ttu-id="deafc-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deafc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deafc-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="deafc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deafc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deafc-133">CommonParameters</span></span>
<span data-ttu-id="deafc-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deafc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deafc-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="deafc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deafc-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="deafc-136">INPUTS</span></span>

### <span data-ttu-id="deafc-137">Microsoft. Azure. Commands. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="deafc-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="deafc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="deafc-138">System.String</span></span>

## <span data-ttu-id="deafc-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="deafc-139">OUTPUTS</span></span>

### <span data-ttu-id="deafc-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="deafc-140">System.Boolean</span></span>

## <span data-ttu-id="deafc-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="deafc-141">NOTES</span></span>

## <span data-ttu-id="deafc-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="deafc-142">RELATED LINKS</span></span>

<span data-ttu-id="deafc-143">[Nowe — AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="deafc-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
