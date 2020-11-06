---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 4dda510402b9395db24507f22d90da0f1fb6a44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524401"
---
# <span data-ttu-id="be51c-101">Remove-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="be51c-101">Remove-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="be51c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be51c-102">SYNOPSIS</span></span>
<span data-ttu-id="be51c-103">Usuwanie zasad WAF</span><span class="sxs-lookup"><span data-stu-id="be51c-103">Remove WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be51c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be51c-104">SYNTAX</span></span>

### <span data-ttu-id="be51c-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="be51c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be51c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be51c-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be51c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be51c-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be51c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="be51c-108">DESCRIPTION</span></span>
<span data-ttu-id="be51c-109">Polecenie cmdlet **Remove-AzureRmFrontDoor** usuwa zasadę WAF w ramach bieżącego abonamentu</span><span class="sxs-lookup"><span data-stu-id="be51c-109">The **Remove-AzureRmFrontDoor** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="be51c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be51c-110">EXAMPLES</span></span>

### <span data-ttu-id="be51c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="be51c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup
```

<span data-ttu-id="be51c-112">Usuń zasady WAF o nazwie $name w $resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="be51c-112">Remove the WAF policy called $name in $resourceGroup.</span></span>

### <span data-ttu-id="be51c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="be51c-113">Example 2</span></span>
```powershell
PS C:\> Get--AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Remove-AzureRmFrontDoorFireWallPolicy
```

<span data-ttu-id="be51c-114">Usuń wszystkie zasady WAF w $resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="be51c-114">Remove all WAF policy in $resourceGroup.</span></span>

## <span data-ttu-id="be51c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be51c-115">PARAMETERS</span></span>

### <span data-ttu-id="be51c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be51c-116">-DefaultProfile</span></span>
<span data-ttu-id="be51c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="be51c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be51c-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="be51c-118">-InputObject</span></span>
<span data-ttu-id="be51c-119">Obiekt zasady WAF, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="be51c-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="be51c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be51c-120">-Name</span></span>
<span data-ttu-id="be51c-121">Nazwa zasad WAF, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="be51c-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="be51c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be51c-122">-PassThru</span></span>
<span data-ttu-id="be51c-123">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="be51c-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="be51c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be51c-124">-ResourceGroupName</span></span>
<span data-ttu-id="be51c-125">Grupa zasobów, do której należy zasada WAF.</span><span class="sxs-lookup"><span data-stu-id="be51c-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="be51c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be51c-126">-ResourceId</span></span>
<span data-ttu-id="be51c-127">Identyfikator zasobu zasady WAF do usunięcia</span><span class="sxs-lookup"><span data-stu-id="be51c-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="be51c-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be51c-128">-Confirm</span></span>
<span data-ttu-id="be51c-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be51c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be51c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be51c-130">-WhatIf</span></span>
<span data-ttu-id="be51c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be51c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be51c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="be51c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be51c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be51c-133">CommonParameters</span></span>
<span data-ttu-id="be51c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be51c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be51c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be51c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be51c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be51c-136">INPUTS</span></span>

### <span data-ttu-id="be51c-137">Microsoft. Azure. Commands. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="be51c-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="be51c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="be51c-138">System.String</span></span>

### <span data-ttu-id="be51c-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="be51c-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="be51c-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be51c-140">OUTPUTS</span></span>

### <span data-ttu-id="be51c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="be51c-141">System.Boolean</span></span>

## <span data-ttu-id="be51c-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be51c-142">NOTES</span></span>

## <span data-ttu-id="be51c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be51c-143">RELATED LINKS</span></span>

<span data-ttu-id="be51c-144">[Nowe — AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="be51c-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span></span>
