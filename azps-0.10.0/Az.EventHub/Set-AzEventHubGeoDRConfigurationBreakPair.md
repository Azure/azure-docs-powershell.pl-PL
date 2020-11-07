---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 76bb062105567303baac72f0b27f14f36bdb120d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891413"
---
# <span data-ttu-id="6dca4-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="6dca4-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="6dca4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6dca4-102">SYNOPSIS</span></span>
<span data-ttu-id="6dca4-103">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowych na pomocnicze obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="6dca4-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="6dca4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6dca4-104">SYNTAX</span></span>

### <span data-ttu-id="6dca4-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6dca4-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dca4-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6dca4-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dca4-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dca4-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dca4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6dca4-108">DESCRIPTION</span></span>
<span data-ttu-id="6dca4-109">Polecenie cmdlet **Set-AzEventHubGeoDRConfigurationBreakPair** wyłącza odzyskiwanie po awarii i zatrzymuje Replikowanie zmian z podstawowych do pomocniczych obszarów nazw</span><span class="sxs-lookup"><span data-stu-id="6dca4-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="6dca4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6dca4-110">EXAMPLES</span></span>

### <span data-ttu-id="6dca4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6dca4-111">Example</span></span>
```
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="6dca4-112">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowych na pomocnicze obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="6dca4-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="6dca4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6dca4-113">PARAMETERS</span></span>

### <span data-ttu-id="6dca4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dca4-114">-DefaultProfile</span></span>
<span data-ttu-id="6dca4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6dca4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dca4-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6dca4-116">-InputObject</span></span>
<span data-ttu-id="6dca4-117">Obiekt konfiguracji GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="6dca4-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="6dca4-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6dca4-118">-Name</span></span>
<span data-ttu-id="6dca4-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="6dca4-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="6dca4-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6dca4-120">-Namespace</span></span>
<span data-ttu-id="6dca4-121">Nazwa obszaru nazw — podstawowy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="6dca4-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="6dca4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dca4-122">-PassThru</span></span>
<span data-ttu-id="6dca4-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="6dca4-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6dca4-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="6dca4-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6dca4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dca4-125">-ResourceGroupName</span></span>
<span data-ttu-id="6dca4-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6dca4-126">Resource Group Name</span></span>

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

### <span data-ttu-id="6dca4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dca4-127">-ResourceId</span></span>
<span data-ttu-id="6dca4-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dca4-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="6dca4-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6dca4-129">-Confirm</span></span>
<span data-ttu-id="6dca4-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dca4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dca4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dca4-131">-WhatIf</span></span>
<span data-ttu-id="6dca4-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dca4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dca4-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6dca4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dca4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dca4-134">CommonParameters</span></span>
<span data-ttu-id="6dca4-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dca4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dca4-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dca4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dca4-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6dca4-137">INPUTS</span></span>

### <span data-ttu-id="6dca4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6dca4-138">System.String</span></span>

### <span data-ttu-id="6dca4-139">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="6dca4-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="6dca4-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6dca4-140">OUTPUTS</span></span>

### <span data-ttu-id="6dca4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6dca4-141">System.Boolean</span></span>

## <span data-ttu-id="6dca4-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6dca4-142">NOTES</span></span>

## <span data-ttu-id="6dca4-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6dca4-143">RELATED LINKS</span></span>
