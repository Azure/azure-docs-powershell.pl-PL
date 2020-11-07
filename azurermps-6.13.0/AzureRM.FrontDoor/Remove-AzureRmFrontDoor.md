---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
ms.openlocfilehash: 8eae5034080bd1035cfe7e8331ca015820688e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716439"
---
# <span data-ttu-id="43f90-101">Remove-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="43f90-101">Remove-AzureRmFrontDoor</span></span>

## <span data-ttu-id="43f90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43f90-102">SYNOPSIS</span></span>
<span data-ttu-id="43f90-103">Usuwanie czołowego modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="43f90-103">Remove Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43f90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43f90-104">SYNTAX</span></span>

### <span data-ttu-id="43f90-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="43f90-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43f90-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43f90-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43f90-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43f90-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43f90-108">Opis</span><span class="sxs-lookup"><span data-stu-id="43f90-108">DESCRIPTION</span></span>
<span data-ttu-id="43f90-109">Polecenie cmdlet **Remove-AzureRmFrontDoor** usuwa przednią stację równoważenia obciążenia pod bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="43f90-109">The **Remove-AzureRmFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="43f90-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43f90-110">EXAMPLES</span></span>

### <span data-ttu-id="43f90-111">Przykład 1: usunięcie "frontdoor1" w grupie zasobów "RG1" w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="43f90-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="43f90-112">Usuń "frontdoor1" w grupie zasobów "RG1" pod bieżącym abonamentem.</span><span class="sxs-lookup"><span data-stu-id="43f90-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="43f90-113">Przykład 2: usunięcie wszystkich FrontDoors w grupie zasobów "RG1" w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="43f90-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="43f90-114">Usuń wszystkie FrontDoors w grupie zasobów "RG1" pod bieżącym abonamentem.</span><span class="sxs-lookup"><span data-stu-id="43f90-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="43f90-115">Przykład 3: usunięcie wszystkich FrontDoors w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="43f90-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor | Remove-AzureRmFrontDoor
```

<span data-ttu-id="43f90-116">Usuń wszystkie FrontDoors w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="43f90-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="43f90-117">Przykład 4: Usuwanie wszystkich FrontDoors o nazwie "frontdoor1" w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="43f90-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="43f90-118">Usuń wszystkie FrontDoors o nazwie "frontdoor1" w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="43f90-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="43f90-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43f90-119">PARAMETERS</span></span>

### <span data-ttu-id="43f90-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f90-120">-DefaultProfile</span></span>
<span data-ttu-id="43f90-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43f90-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43f90-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43f90-122">-InputObject</span></span>
<span data-ttu-id="43f90-123">Obiekt z przodu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="43f90-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="43f90-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43f90-124">-Name</span></span>
<span data-ttu-id="43f90-125">Nazwa przednich drzwi, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="43f90-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="43f90-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43f90-126">-PassThru</span></span>
<span data-ttu-id="43f90-127">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="43f90-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="43f90-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43f90-128">-ResourceGroupName</span></span>
<span data-ttu-id="43f90-129">Grupa zasobów, do której należą przednia drzwi.</span><span class="sxs-lookup"><span data-stu-id="43f90-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="43f90-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43f90-130">-ResourceId</span></span>
<span data-ttu-id="43f90-131">Identyfikator zasobu czołowych drzwi do usunięcia</span><span class="sxs-lookup"><span data-stu-id="43f90-131">Resource Id of the Front Door to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f90-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43f90-132">-Confirm</span></span>
<span data-ttu-id="43f90-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43f90-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43f90-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f90-134">-WhatIf</span></span>
<span data-ttu-id="43f90-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43f90-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43f90-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="43f90-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43f90-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f90-137">CommonParameters</span></span>
<span data-ttu-id="43f90-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43f90-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f90-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f90-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f90-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43f90-140">INPUTS</span></span>

### <span data-ttu-id="43f90-141">Microsoft. Azure. Commands. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="43f90-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="43f90-142">System. String</span><span class="sxs-lookup"><span data-stu-id="43f90-142">System.String</span></span>

### <span data-ttu-id="43f90-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="43f90-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="43f90-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43f90-144">OUTPUTS</span></span>

### <span data-ttu-id="43f90-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43f90-145">System.Boolean</span></span>

## <span data-ttu-id="43f90-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43f90-146">NOTES</span></span>

## <span data-ttu-id="43f90-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43f90-147">RELATED LINKS</span></span>

<span data-ttu-id="43f90-148">[Nowe — AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="43f90-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span></span>
