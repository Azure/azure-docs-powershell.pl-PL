---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 6e31353724528c4c9096f9475c7093c338ed270f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971098"
---
# <span data-ttu-id="5b98d-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="5b98d-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="5b98d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b98d-102">SYNOPSIS</span></span>
<span data-ttu-id="5b98d-103">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowej do pomocniczej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="5b98d-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="5b98d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5b98d-104">SYNTAX</span></span>

### <span data-ttu-id="5b98d-105">GeoDRParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5b98d-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b98d-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5b98d-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b98d-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b98d-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b98d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5b98d-108">DESCRIPTION</span></span>
<span data-ttu-id="5b98d-109">Polecenie **cmdlet Set-AzEventHubGeoDRConfigurationBreakPair** wyłącza odzyskiwanie po awarii i przestaje replikować zmiany z podstawowych do pomocniczych przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="5b98d-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="5b98d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5b98d-110">EXAMPLES</span></span>

### <span data-ttu-id="5b98d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5b98d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="5b98d-112">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowej do pomocniczej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="5b98d-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="5b98d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b98d-113">PARAMETERS</span></span>

### <span data-ttu-id="5b98d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b98d-114">-DefaultProfile</span></span>
<span data-ttu-id="5b98d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b98d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b98d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b98d-116">-InputObject</span></span>
<span data-ttu-id="5b98d-117">Obiekt konfiguracji GeoDR aplikacji Eventhub</span><span class="sxs-lookup"><span data-stu-id="5b98d-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b98d-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5b98d-118">-Name</span></span>
<span data-ttu-id="5b98d-119">Nazwa konfiguracji dr</span><span class="sxs-lookup"><span data-stu-id="5b98d-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b98d-120">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="5b98d-120">-Namespace</span></span>
<span data-ttu-id="5b98d-121">Nazwa przestrzeni nazw — podstawowa przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="5b98d-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b98d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b98d-122">-PassThru</span></span>
<span data-ttu-id="5b98d-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="5b98d-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5b98d-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5b98d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5b98d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b98d-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b98d-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5b98d-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b98d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b98d-127">-ResourceId</span></span>
<span data-ttu-id="5b98d-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b98d-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="5b98d-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5b98d-129">-Confirm</span></span>
<span data-ttu-id="5b98d-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5b98d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b98d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b98d-131">-WhatIf</span></span>
<span data-ttu-id="5b98d-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b98d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b98d-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5b98d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b98d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b98d-134">CommonParameters</span></span>
<span data-ttu-id="5b98d-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b98d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b98d-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b98d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b98d-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b98d-137">INPUTS</span></span>

### <span data-ttu-id="5b98d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5b98d-138">System.String</span></span>

### <span data-ttu-id="5b98d-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="5b98d-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="5b98d-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b98d-140">OUTPUTS</span></span>

### <span data-ttu-id="5b98d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b98d-141">System.Boolean</span></span>

## <span data-ttu-id="5b98d-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5b98d-142">NOTES</span></span>

## <span data-ttu-id="5b98d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b98d-143">RELATED LINKS</span></span>
