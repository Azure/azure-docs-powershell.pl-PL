---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4ee96fbe20fca3f0af1f0bb9604f178b912d0ea2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489757"
---
# <span data-ttu-id="15edf-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="15edf-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="15edf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15edf-102">SYNOPSIS</span></span>
<span data-ttu-id="15edf-103">Wywołuje tryb failover w trybie GEO DR i ponownie skonfiguruje alias tak, aby wskazywał pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="15edf-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="15edf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15edf-104">SYNTAX</span></span>

### <span data-ttu-id="15edf-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="15edf-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15edf-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="15edf-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15edf-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15edf-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15edf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="15edf-108">DESCRIPTION</span></span>
<span data-ttu-id="15edf-109">Polecenie cmdlet **Set-AzEventHubGeoDRConfigurationFailOver** umożliwia przełączenie do trybu failover w trybie Geo i ponowne skonfigurowanie aliasu tak, aby wskazywał pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="15edf-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="15edf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15edf-110">EXAMPLES</span></span>

### <span data-ttu-id="15edf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="15edf-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="15edf-112">Wywołuje tryb failover na aliasie "SampleDRConfigName", ponownie konfiguruje i wskazuje pomocniczy obszar nazw "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="15edf-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="15edf-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15edf-113">PARAMETERS</span></span>

### <span data-ttu-id="15edf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15edf-114">-DefaultProfile</span></span>
<span data-ttu-id="15edf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15edf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15edf-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="15edf-116">-InputObject</span></span>
<span data-ttu-id="15edf-117">Obiekt konfiguracji GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="15edf-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="15edf-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="15edf-118">-Name</span></span>
<span data-ttu-id="15edf-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="15edf-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="15edf-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="15edf-120">-Namespace</span></span>
<span data-ttu-id="15edf-121">Nazwa przestrzeni nazw — pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="15edf-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="15edf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15edf-122">-PassThru</span></span>
<span data-ttu-id="15edf-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="15edf-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="15edf-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="15edf-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="15edf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15edf-125">-ResourceGroupName</span></span>
<span data-ttu-id="15edf-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="15edf-126">Resource Group Name</span></span>

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

### <span data-ttu-id="15edf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15edf-127">-ResourceId</span></span>
<span data-ttu-id="15edf-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="15edf-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="15edf-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15edf-129">-Confirm</span></span>
<span data-ttu-id="15edf-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15edf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15edf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15edf-131">-WhatIf</span></span>
<span data-ttu-id="15edf-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15edf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15edf-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="15edf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15edf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15edf-134">CommonParameters</span></span>
<span data-ttu-id="15edf-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15edf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15edf-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15edf-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15edf-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15edf-137">INPUTS</span></span>

### <span data-ttu-id="15edf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="15edf-138">System.String</span></span>

### <span data-ttu-id="15edf-139">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="15edf-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="15edf-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15edf-140">OUTPUTS</span></span>

### <span data-ttu-id="15edf-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15edf-141">System.Boolean</span></span>

## <span data-ttu-id="15edf-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15edf-142">NOTES</span></span>

## <span data-ttu-id="15edf-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15edf-143">RELATED LINKS</span></span>
