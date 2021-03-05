---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 3fa1dd4c3f926e0c6011d8ffec3a510340a7eab3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999722"
---
# <span data-ttu-id="f6bac-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6bac-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="f6bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6bac-102">SYNOPSIS</span></span>
<span data-ttu-id="f6bac-103">Usuwa alias (konfigurację odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="f6bac-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f6bac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f6bac-104">SYNTAX</span></span>

### <span data-ttu-id="f6bac-105">GeoDRPropertiesSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f6bac-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6bac-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f6bac-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6bac-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6bac-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6bac-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f6bac-108">DESCRIPTION</span></span>
<span data-ttu-id="f6bac-109">Polecenie **cmdlet Remove-AzServiceBusGeoDRConfiguration** usuwa alias(konfigurację odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="f6bac-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f6bac-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f6bac-110">EXAMPLES</span></span>

### <span data-ttu-id="f6bac-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6bac-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="f6bac-112">Usuwa alias (konfigurację odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="f6bac-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f6bac-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6bac-113">PARAMETERS</span></span>

### <span data-ttu-id="f6bac-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f6bac-114">-AsJob</span></span>
<span data-ttu-id="f6bac-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f6bac-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6bac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6bac-116">-DefaultProfile</span></span>
<span data-ttu-id="f6bac-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6bac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6bac-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6bac-118">-InputObject</span></span>
<span data-ttu-id="f6bac-119">Obiekt konfiguracji geodru autobusu usługowego</span><span class="sxs-lookup"><span data-stu-id="f6bac-119">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6bac-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f6bac-120">-Name</span></span>
<span data-ttu-id="f6bac-121">Nazwa aliasu (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="f6bac-121">Alias (GeoDR) Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6bac-122">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="f6bac-122">-Namespace</span></span>
<span data-ttu-id="f6bac-123">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="f6bac-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6bac-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6bac-124">-PassThru</span></span>
<span data-ttu-id="f6bac-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f6bac-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f6bac-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f6bac-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f6bac-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6bac-127">-ResourceGroupName</span></span>
<span data-ttu-id="f6bac-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f6bac-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6bac-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6bac-129">-ResourceId</span></span>
<span data-ttu-id="f6bac-130">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6bac-130">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6bac-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f6bac-131">-Confirm</span></span>
<span data-ttu-id="f6bac-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f6bac-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6bac-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6bac-133">-WhatIf</span></span>
<span data-ttu-id="f6bac-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6bac-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6bac-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f6bac-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6bac-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6bac-136">CommonParameters</span></span>
<span data-ttu-id="f6bac-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6bac-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6bac-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6bac-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6bac-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6bac-139">INPUTS</span></span>

### <span data-ttu-id="f6bac-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f6bac-140">System.String</span></span>

### <span data-ttu-id="f6bac-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f6bac-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="f6bac-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6bac-142">OUTPUTS</span></span>

### <span data-ttu-id="f6bac-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f6bac-143">System.Boolean</span></span>

## <span data-ttu-id="f6bac-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f6bac-144">NOTES</span></span>

## <span data-ttu-id="f6bac-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6bac-145">RELATED LINKS</span></span>
