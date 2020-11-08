---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221197"
---
# <span data-ttu-id="a4a31-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="a4a31-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="a4a31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4a31-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a31-103">Usuwanie czołowego modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="a4a31-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="a4a31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4a31-104">SYNTAX</span></span>

### <span data-ttu-id="a4a31-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a4a31-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4a31-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4a31-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4a31-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4a31-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4a31-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a4a31-108">DESCRIPTION</span></span>
<span data-ttu-id="a4a31-109">Polecenie cmdlet **Remove-AzFrontDoor** usuwa przednią stację równoważenia obciążenia pod bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="a4a31-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="a4a31-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4a31-110">EXAMPLES</span></span>

### <span data-ttu-id="a4a31-111">Przykład 1: usunięcie "frontdoor1" w grupie zasobów "RG1" w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a4a31-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="a4a31-112">Usuń "frontdoor1" w grupie zasobów "RG1" pod bieżącym abonamentem.</span><span class="sxs-lookup"><span data-stu-id="a4a31-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="a4a31-113">Przykład 2: usunięcie wszystkich FrontDoors w grupie zasobów "RG1" w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a4a31-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="a4a31-114">Usuń wszystkie FrontDoors w grupie zasobów "RG1" pod bieżącym abonamentem.</span><span class="sxs-lookup"><span data-stu-id="a4a31-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="a4a31-115">Przykład 3: usunięcie wszystkich FrontDoors w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a4a31-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="a4a31-116">Usuń wszystkie FrontDoors w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a4a31-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="a4a31-117">Przykład 4: Usuwanie wszystkich FrontDoors o nazwie "frontdoor1" w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a4a31-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="a4a31-118">Usuń wszystkie FrontDoors o nazwie "frontdoor1" w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a4a31-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="a4a31-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4a31-119">PARAMETERS</span></span>

### <span data-ttu-id="a4a31-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a31-120">-DefaultProfile</span></span>
<span data-ttu-id="a4a31-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a31-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4a31-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a4a31-122">-InputObject</span></span>
<span data-ttu-id="a4a31-123">Obiekt z przodu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="a4a31-123">The Front Door object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4a31-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4a31-124">-Name</span></span>
<span data-ttu-id="a4a31-125">Nazwa przednich drzwi, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="a4a31-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="a4a31-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4a31-126">-PassThru</span></span>
<span data-ttu-id="a4a31-127">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="a4a31-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="a4a31-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4a31-128">-ResourceGroupName</span></span>
<span data-ttu-id="a4a31-129">Grupa zasobów, do której należą przednia drzwi.</span><span class="sxs-lookup"><span data-stu-id="a4a31-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="a4a31-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4a31-130">-ResourceId</span></span>
<span data-ttu-id="a4a31-131">Identyfikator zasobu czołowych drzwi do usunięcia</span><span class="sxs-lookup"><span data-stu-id="a4a31-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="a4a31-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4a31-132">-Confirm</span></span>
<span data-ttu-id="a4a31-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4a31-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4a31-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4a31-134">-WhatIf</span></span>
<span data-ttu-id="a4a31-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4a31-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4a31-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4a31-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4a31-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a31-137">CommonParameters</span></span>
<span data-ttu-id="a4a31-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a31-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a31-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4a31-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a31-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4a31-140">INPUTS</span></span>

### <span data-ttu-id="a4a31-141">Microsoft. Azure. Commands. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="a4a31-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="a4a31-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a4a31-142">System.String</span></span>

## <span data-ttu-id="a4a31-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4a31-143">OUTPUTS</span></span>

### <span data-ttu-id="a4a31-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4a31-144">System.Boolean</span></span>

## <span data-ttu-id="a4a31-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4a31-145">NOTES</span></span>

## <span data-ttu-id="a4a31-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4a31-146">RELATED LINKS</span></span>

<span data-ttu-id="a4a31-147">[Nowe — AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="a4a31-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>